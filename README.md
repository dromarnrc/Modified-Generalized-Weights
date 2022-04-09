# Modified-Generalized-Weights
A new method for modeling main effects and interactions of input variables in Artificial Neural Networks
This code is opened for any number of inputs. 

How to use this code :

Step #1: Create an Excel file containing data of input variables and 1 output (for example x1,x2,x3,x4,y).

![4-7-2022 8-32-08 PM](https://user-images.githubusercontent.com/95976623/162275612-d941eab0-1dc3-4737-a30b-79f8fb11f979.jpg)


Step #2: install the following libraries using the command 

install.packages("readxl")

install.packages("neuralnet")

install.packages("RSNNS") 

library(readxl) for reading Excel files;

library(neuralnet) for running neural network;

library(RSNNS) for normalizing data to be between 0 and 1

Step #3: Copy the code to R source window if you have installed R studio, or copy the code to R console if you have not installed R studio.

![4-7-2022 8-39-52 PM](https://user-images.githubusercontent.com/95976623/162273927-fdd4cea0-6958-4ec1-a5b8-dafd7514ee33.jpg)


Step #4: select all the code by right click  on R source window then choose select all, then hit the (run) button.You will be notified to choose your file. Once you have chose your file, you will see the results in R console as the following:

![4-7-2022 8-35-20 PM](https://user-images.githubusercontent.com/95976623/162274078-bc3a30f1-e36b-4dd0-9c5d-08b3a7d08731.jpg)

The results show the relative importance of each input based on R square and as a percent as well as both variance and the sum of the modified generalized weights.
The sign of the sum refers to direction of the effect. When the sign of the main effect is negative this means that when the iput increases the output decreases. If the sign of an interacton is negative this means that when an input increases the effect of the other input on the output decreases. Also, the results show the total main effects and the total interaction effects in the last two columns.


