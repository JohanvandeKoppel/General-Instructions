This repository contains contains GPU code that runs a number of self-organization models

Running the code requires an Nvidia graphics card and the CUDA package installed. The code has been build and tested using a Macbook pro 2012 edition. I run it using the cmake package (www.cmake.org) that handles the generation of a suitable makefile.

If you run under Windows, you have to install CUDA including SDK and samples within Visual Studio, and integrate the code files within a Visual studio project. The simples way to do that is to use copy one of the code samples into a new folder within the samples folder, and use an existing sample project file by replacing the code files. I cannot help you with this as I am a Mac user (I actually switched to Mac to avoid the visual studio headache, so be warned).

Presuming that the Nvidia SDK and cmake are installed, unzip the file somewhere, and open a command window in the build folder within the unzipped code folder. Now, run:

cmake ..
clear; make
clear; make run

If you want to clear the build, type
clear; make destroy

The code itself does not show anything except for a counter. To view the results, you have to use the PlotMussel.r R-project file (using R and RStudio I advice) or PlotMussel.m within Matlab. Note to set the folder settings correctly and to install the “fields” package within R (install.package(“fields”);)

Both scripts can make a movie. The R script is best for that, but you have to install the ffmpeg program, which you can find here: https://www.ffmpeg.org/ 

I hope the code it useful for you. Please drop me an email if you like to tell whether it worked for you or not.

