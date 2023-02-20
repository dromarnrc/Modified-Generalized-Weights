# Modified-Generalized-Weights
A new method for modeling main effects and interactions of input variables in Artificial Neural Networks (ANNs). The method was published in a paper on 20 June 2022 at
https://link.springer.com/article/10.1134/S1064229322080051 under the title of "Modeling Main and Interactional Effects of Some Physiochemical Properties of Egyptian Soils on Cation Exchange Capacity Via Artificial Neural Networks". In addition, a package of the new method has been built at https://CRAN.R-project.org/package=FRI.
This code can be used for many inputs and one output with one hidden layer as interaction among inputs is assumed to occur in the first hidden layer. The method is restricted to the Sigmoid activation function and one hidden layer where ANNs with one hidden layer are suitable for regression problems, while ANNs with many hidden layers are suitable for classification problems as ANNs need to comprehend something extremely convoluted, relevant, or non-self-evident, like image recognition.
 
How to use this code :

Step #1: Create an Excel file containing data of input variables and 1 output (for example x1,x2,x3,x4,x5,y).

![5-7-2022 8-05-26 PM](https://user-images.githubusercontent.com/95976623/167266623-450e0b8c-4f4a-4c1d-b5c1-87e9bda65bae.jpg)


Step #2: install the following libraries using the following commands: 

install.packages("openxlsx") # for reading excel file

install.packages("neuralnet") # for running neural network

install.packages("BBmisc") # for normalizing data to be between 0 and 1 for sigmoid activation function.

install.packages("ggplot2") # to generate the figures

install.packages("forcats") # to keep the order of the variables the same in the figures



Step #3: Copy the code to R source window if you have installed R studio, or copy the code to R console if you have not installed R studio.

![2023-01-16_20-23-16](https://user-images.githubusercontent.com/95976623/212744631-8672f0c7-e5e3-4033-9fbb-20651505522e.jpg)


Step #4: select all the code by right click  on R source window then choose select all, then hit the (run) button.You will be notified to choose your file, once you have chosen your file, you will see the results in R console as the following:

![8-6-2022 10-40-18 AM](https://user-images.githubusercontent.com/95976623/183242063-8ad7cea5-4e22-4e4c-bc0a-687da57670db.jpg)

The results show the relative importance of main effects (direct effects) of each input and the two way interaction effects between each pair of the input variables. The results are displayed based on R square and recalculated based on 100% (values are sum to 1) for comparison. Also, the sum of the modified generalized weights is displayed, the sum indicates the direction of the effect. If the sum of the direct effect of an input is positive, this means that when this input increases the output increases and vice versa. If the sum of an interaction is positive, this means that when one input increases the effect of the other input on the output increases. If the sum of an interaction is negative, this means that when one input increases the effect of the other input on the output decreases. The results show also the standard error and generate the following figure:

![5-7-2022 8-08-34 PM](https://user-images.githubusercontent.com/95976623/167266661-cb16ded5-413e-4be1-bed7-ff0e4a96ac67.jpg)



