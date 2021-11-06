# PCAR
#### Path-connected aggregate recognition of diffraction-limited images

The software is provided as a one executable file `DiffLimAnalyseFolder.exe`. To run it you need to install the Windows version of the MATLAB Runtime for R2020b from https://www.mathworks.com/products/compiler/mcr/index.html. If you already have MATLAB R2020b installed, you can run the executable file `DiffLimAnalyseFolder.exe` right away.

The software works in the following way.
1. Save log file with a name `Log.txt`.
2. Create `Default` folder and save default parameters in this folder.
3. Create a dialog box to initialize parameters.
   - *Crop window (choose new pixel size)*. If you need to crop the image, select this parameter smaller than the number of pixels of your image. The center of a new square is selected automatically and is located in the pixel with maximum backgroud intensity.
   - *Crop ... pixels from left and top*. If you need to crop the image from left and top, set this value to non-zero value.
   - *Crop ... first images from the stack*. If you need to remove several first slides from the image stack, set this value to non-zero value.
   - *Laser wavelength (nm)*. If your experiment is done for one laser wavelength, this value can be a scalar. Otherwise, this value must be a vector (for example, [488; 641]).
   - *Factor for the threshold*. If the software detect aggregates that are rather noise than real aggregates, set this value to 2 to select stricter threshold.
   - *Peak sensitivity for cluster analysis*. The factor F for clustering (separating aggregates). Two clusters with peak intensities I_1 and I_2 are considered different if they cannot be connected with a path intensity along which is always higher than F∙min⁡(I_1,I_2).

