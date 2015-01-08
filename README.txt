This repository contains contains GPU code that runs a number of self-organization models

Running the codes requires an OpenCL-compatible graphics card and OpenCL drivers installed. On a Mac, this is natively done when Xcode has been installed, and the current code has been developed in Xcode using a Macbook pro 2012 edition. You can also compile and run the codes from the command line on a Mac. I run it using the cmake package (www.cmake.org) that handles the generation of a suitable makefile. See further explanation below.

If you run under Windows with a computer that has an Nvidia card, you have to install CUDA (which has OpenCL integrated) including SDK and the OpenCL samples within Visual Studio, and integrate the code files within a Visual studio project. The simplest way to do that is to copy one of the code samples into a new folder within the samples folder, and use an existing sample project file by replacing the code files. I cannot help you with this as I am a Mac user (I actually switched to Mac to avoid the visual studio headache, so be warned).

For Mac or Linux users: Presuming that cmake is installed, you have to download the FindOpenCL.cmake file and put it two folders down from the current code (e.g., in a general, common folder to be used for all repository codes). If you don't want to put it in that location, than change the following line in each of the CMakeLists.txt files:
set(CMAKE_MODULE_PATH "${CMAKE_SOURCE_DIR}/../..")
So that it points to the right folder.

Then, unzip the file somewhere, and open a command window in the build folder within the unzipped code folder. Now, run:

cmake ..
clear; make
clear; make run

If you want to clear the build, type
clear; make destroy

The code itself does not show anything except for a counter. To view the results, you have to use the PlotMussel.r R-project file (using R and RStudio I advice) or PlotMussel.m within Matlab. Note to set the folder settings correctly and to install the “fields” package within R (install.package(“fields”);)

Both scripts can make a movie. The R script is best for that, but you have to install the ffmpeg program, which you can find here: https://www.ffmpeg.org/ 

I hope the code it useful for you. Please drop me an email if you like to tell whether it worked for you or not.

