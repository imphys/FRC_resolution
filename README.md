# FRC_resolution
Measuring Image Resolution in Optical Nanoscopy


## FRCresolution software distribution

This software is distributed as accompanying software for the article Measuring Image Resolution in Optical Nanoscopy by R.J.P. Nieuewenhuizen, K.A. Lidke, M. Bates, D. Leyton Puig, D. Grunwald, S. Stallinga, B. Rieger, Nature Methods, 2013 doi:10.1038/nmeth.2448.
This distribution contains MATLAB software and an ImageJ plugin to run (part of) the algorithms described in the article. 
The MATLAB software is more extensive than the ImageJ plugin.

## MATLAB

The provided scripts use Matlab (http://www.mathworks.com). The example code uses functions from the DIPimage Toolbox, you must install it before you are able to run the provided examples. 
DIPimage is a freely available image processing toolbox for MATLAB: http://www.diplib.org 

An installer for Windows is available, archives are available for Linux and Mac. Furthermore, it is handy to have the curvefitting toolbox, but not required.

In the directory matlabfunctions all relevant matlab functionality is included. There are 4 examples that show different computations of 2D FRC resolution and curves example1.m, 2D anisotropic FLC example2.m, and 3D FPC example3.m. 
These examples compute (part of) the data shown in the Figures from the article.
The main interface functions are: imres ims and imres locs, which compute FRC resolution and associated things from two images or a localization list respectively. 
See example4.m for their uses.
The code makes use of the MATALB parameterization toolbox if available. To this end you must add the fullpath to the ImageResolutionFunctions directory to the MATLAB path, e.g. `addpath(’/home/bernd/ImageResolutionfunctions’)`. 
All data is loaded from a data directory and is stored as comma separate list (*.dat).
We hope that these examples are instructive enough to allow the interested user to apply our code. 
If you have any troubles please to not hesitate to contact us at the email address given below.

## ImageJ plugin

The ImageJ plugin is offering only basic functionality compared to the MATLAB functions. 
Just copy the plugin FRCres plugin.jar and commons-math-1.2.jar into your local plugin folder and you are all set. 
For example data please have a look at the two .txt files in the `ExampleData` directory. 
The input for the ImageJ plugin are list of coordinates. 
They can have the form `x` `y` or `t` `x` `y` or `x` `y` `t`. The different values must be whitespace delimited. For the dataset TestData02.txt the default setting are not appropriate but should be: 
Input data in CCD pixel size, with CCD pixel size = 107 nm and specific output image size 2560.

## Terms of use

Copyright (c) 2013
This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.
This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the
GNU General Public License for more details,
see www.gnu.org.

Quantitative Imaging Group
Faculty of Applied Sciences
Delft University of Technology
Lorentzweg 1, 2628 CJ Delft
The Netherlands
contact: Bernd Rieger, b.rieger@tudelft.nl