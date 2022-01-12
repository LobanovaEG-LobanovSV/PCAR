# PCAR
## Path-connected aggregate recognition of diffraction-limited single-molecule images

The PCAR tool is designed for simultaneous analysis of diffraction-limited single-molecule images containing single aggregates in one click.

#### **Good features of PCAR:**
1. recognises aggregates of various size and shape ranging from spots to long fibrils and complex shaped aggregates
2. works equally well with low and high aggregate density present in one dataset and analysed altogether 
3. provide broader applications from detecting picomolar concentrations of aggregates in CSF and cell media to analysis of concentrated samples such as serum, cell lysates, brain homogenates and etc.
4. user-friendly with just 2 intuitive parameters for analysis that take only several values
5. good funcionality (1) Aggregate Counts, (2) Aggregate Brightness and (3) Aggregate Area automatically saved in an Excel file + PowerPont presentation.


The software is provided as a one executable file `DiffLimAnalyseFolder.exe`. To run it you need to install the Windows version of the MATLAB Runtime for R2020b from https://www.mathworks.com/products/compiler/mcr/index.html. If you already have MATLAB R2020b installed, you can run the executable file `DiffLimAnalyseFolder.exe` straight away.

The software works in the following way.
1. Save log file with a name `Log.txt`.
2. Create `Default` folder and save default parameters in this folder.
3. Create a dialog box to initialize parameters.
   - *Crop window (choose a new number of pixels)*. If you need to crop the image, select this parameter smaller than the number of pixels in your image. The center of a new square is selected automatically and is located in the pixel with maximum backgroud intensity.
   - *Crop ... pixels from left and top*. If you need to crop the image from left and top, set this value to non-zero value.
   - *Crop ... first images from the stack*. If you need to remove several first slides from the image stack, set this value to non-zero value.
   - *Laser wavelength (nm)*. If your experiment is done for one laser wavelength, this value can be a scalar. Otherwise, this value must be a vector (for example, [488; 641]).
   - *Factor for the threshold*. If the software detect aggregates that are rather noise (normally appear as dim spots) than real aggregates, set this value to 2 to select stricter threshold. The default value is 1.
   - *Peak sensitivity for cluster analysis*. The factor F for clustering (separating aggregates). Two clusters with peak intensities I_1 and I_2 are considered different if they cannot be connected with a path intensity along which is always higher than F∙min⁡(I_1,I_2). The default value is 0.5.

<br/><br/>

This work is licensed under the Creative Commons Attribution-NonCommercial-NoDerivatives 4.0 International License. To view a copy of this license, visit http://creativecommons.org/licenses/by-nc-nd/4.0/ or send a letter to Creative Commons, PO Box 1866, Mountain View, CA 94042, USA.

Copyright (c) 2021, by Evgeniia Lobanova and Sergey Lobanov
