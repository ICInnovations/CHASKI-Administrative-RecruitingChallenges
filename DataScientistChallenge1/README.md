# Data-science Challenge - IC Innovations

## Context

In this challenge you will analyze datasets that contain the time evolution of the physiological variable Respiratory Rate (RR), measured in breaths per minute (bpm) through a ramp test. The respiratory rate of a ramptest can be modeled as a piecewise-linear (3-segment) trend with two breakpoints (VT1 & VT2). We are interested in determining the time instant and the RR where those breakpoints occur, as illustrated in the following image:

![alt text](example.png)


## Tasks

1. Dataset
* Dataset can be found [here](data). Dataset provided should be treated as confidential, and should not be distributed.
* Each .csv file corresponds to an individual ramp test.
* Each file contains one column with the respiratory rate 
* THe respiratory rate has a sample rate of 6 samples per minute.
* Each filename contains metadata information with the noise level of the signal, and the real VT1 & VT2 times & respiratory rate.

2. Model building: segmented regression analysis
* Implement a segmented regression model: datasets are approximated using a piecewise-linear (3-segment) trend. To this end, you have to write a function that solves the 3-segment regression. For more info about segmented regression, see this [link](https://en.wikipedia.org/wiki/Segmented_regression) 
* Your function should return the fitted model parameters $VT_1 [s],RR_{VT_1}[bpm],VT_2 [s],RR_{VT_2}[bpm]$ and the three correlation coefficients $R_1^2,R_2^2,R_3^2$. 
  
3. Model validation: performance assessment
* For each noise level, compute the bias, precision, accuracy, and Pearson coefficients of the predicted parameters $VT_1 [s],RR_{VT_1}[bpm],VT_2 [s],RR_{VT_2}[bpm]$. For a definition of these performance metrics, you may consult this [paper](https://ieeexplore.ieee.org/abstract/document/9296762)

4. Present your results
* Choosing the best and worst cases for each noise level, plot RR [bpm] vs time
* Plot histograms for RR_{VT_1} and RR_{VT_2}, indicating in the plot the mean, median, and standard devation for the sample group 
* Report in a plot the $R_1^2,R_2^2,R_3^2$ for each subject (x-data: subject number, y-data: correlation coefficients)
* For each parameter, construct a single plot with bias, precision, and accuracy vs noise level. 
* Be thoughful about visual aspects of the plots such as choice of colors, font size, title and axis lables (always include units!), legends, etc. Do not include redundant information, be clear and concise. 
* Comment and conclude on your results


## Deliverables
* Codes: all code developments must be written in Python language using Jupyter Notebooks, with the requested results clearly reported. you can use a separate .py file for libraries, if you consider it necessary, but the main code should be in a Jupyter notebook. Please send your Jupyter notebook and .py files by e-mail - do not commit them to this repo. Don't forget to comment your codes/notebook
* Presentation: Prepare a PowerPoint/Google Slides presentation that briefly presents the methods for analysis, results, and conclusions. Your audience is the Chief Science Officer of the company. The presentation should contain at most 8 slides, should be written in English (you can present in Spanish), and should be sent by e-mail when you are done with the challenge
