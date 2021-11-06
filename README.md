# PCAR
#### Path-connected aggregate recognition of diffraction-limited images

The software is provided as a one executable file `DiffLimAnalyseFolder.exe`. To run it you need to install the Windows version of the MATLAB Runtime for R2020b from https://www.mathworks.com/products/compiler/mcr/index.html. If you already have MATLAB R2020b installed, you can run the executable file `DiffLimAnalyseFolder.exe` right away.

The software works in the following way.
1. Save log file with a name `Log.txt`.
2. Create `Default` folder and save default parameters in this folder.
3. Create a dialog box to initialize parameters:
a. Crop window (choose new pixel size): if you need to crop the image, select this parameter smaller than the number of pixels of your image. The center of a new square is selected automatically based on backgroud value.
