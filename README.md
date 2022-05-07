# Modified-Generalized-Weights
A new method for modeling main effects and interactions of input variables in Artificial Neural Networks (ANNs).
This code can be used for many inputs and one output and one hidden layer as interaction among inputs is assumed to occur in the first hidden layer. ANNs with one hidden layer are suitable for regression problems. While ANNs with many hidden layers are suitable for classification problems as ANNs need to comprehend something extremely convoluted, relevant, or non-self-evident, like image recognition.
 
How to use this code :

Step #1: Create an Excel file containing data of input variables and 1 output (for example x1,x2,x3,x4,y).

![5-7-2022 8-05-26 PM](https://user-images.githubusercontent.com/95976623/167266623-450e0b8c-4f4a-4c1d-b5c1-87e9bda65bae.jpg)


Step #2: install the following libraries using the command 

install.packages("readxl")

install.packages("neuralnet")

install.packages("RSNNS") 

library(readxl) for reading Excel files;

library(neuralnet) for running neural network;

library(RSNNS) for normalizing data to be between 0 and 1

Step #3: Copy the code to R source window if you have installed R studio, or copy the code to R console if you have not installed R studio.

![4-7-2022 8-39-52 PM](https://user-images.githubusercontent.com/95976623/162273927-fdd4cea0-6958-4ec1-a5b8-dafd7514ee33.jpg)


Step #4: select all the code by right click  on R source window then choose select all, then hit the (run) button.You will be notified to choose your file. Once you have chosen your file, you will see the results in R console as the following:

![5-7-2022 8-07-32 PM](https://user-images.githubusercontent.com/95976623/167266651-dbe85500-dfa8-4c6f-b30b-1c7274a81d7e.jpg)


The results show the relative importance of main effects (direct effects) of each input and the two way interaction effects between each pair of the input variables. The results are displayed based on R square and recalculated based on 100% for comparison. Also, the variance and the sum of the modified generalized weights are calculated, the variance indicates the variation while the sum indicates the direction of the effect. If the sum of the direct effect of an input is positive, this means that when this input increases the output increases and vice versa. If the sum of an interaction is positive, this means that when one input increases the effect of the other input on the output increases. If the sum of an interaction is negative, this means that when one input increases the effect of the other input on the output decreases. Additionally, the results show the total main effects and the total interaction effects in the last two columns. You can run the code many times by using for loop function to calculate the mean and the standard error.

![5-7-2022 8-08-34 PM](https://user-images.githubusercontent.com/95976623/167266661-cb16ded5-413e-4be1-bed7-ff0e4a96ac67.jpg)



