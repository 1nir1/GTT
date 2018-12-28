# GTT
# What is GTT?
GTT is acronym for Graph To Table. The purpose of the program is to convert
handwritten graph from an image to a set of coordinates. The program is written in
Python3. The input is a simple handwritten graph with numbers alongside the axes -
those numbers represents the maximum point in the graph​.
The output is an excel/csv file with the (X, Y) values of the graph.

# Requirements
python 3.6+​ and the following packages:

numpy, PILLOW, KERAS, opencv-python, tensorflow, openpyxl, matplotlib, h5py==2.8.0rc1

# How to use?
GTT is very simple to use - in order to run it open a command line at the extracted
folder location (where you have downloaded all GTT files), and type the following
command:

	GTT.py --source=img_path [--log_level=logLevel] [--scale=scaleLevel] [--x_y_max X_max Y_MAX]
	
	[] - represents an optional parameter.
	In addition to this paper, you may ask for help with the following command:
	GTT.py --help
	
	Argument list:
		● source - This is the image path. You can use any format you want (png, jpg, jpeg and so on).
		● log_level - We have 5 log levels in GTT, default log level is 0.
		To fully understand the log logic you can visit chapter 5 ("Log level information") at "docs/User Manual.pdf".
		● scale - Scale is the frequency rate of the X axis. The default value is 1.
		The scale value must be a natural number bigger than 1. For example, let’s look at all the natural numbers from 0 to 10.
			○ Scale rate 1 will produce an output that has all the numbers of 0 to 10.
			○ Scale rate 2, will produce all the even numbers from 0 to 10 (0, 2, 4, 6, 8,10)
			○ Scale rate 10, will produce only 0 and 10.
		● x_y_max - Sometimes, the digit recognizer might recognize different numbers from the user’s intention.
		To help with this case we added the following configuration. With this configuration you can enter manually your numbers.
		The given point will be the maximum point in the graph line - the format shall be (x,y).
		If this parameter is provided, the numbers detection library will not be called.
		
More about the project and how to use it can be found at "docs/User Manual.pdf" and "docs/Developer Manual.pdf".
