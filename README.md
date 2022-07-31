# Neural Network Charity Analysis

## Overview
With my knowledge of machine learning and neural networks, I’ll use the features in the provided dataset to create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup.

From Alphabet Soup’s business team, I received a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years. Within this dataset are a number of columns that capture metadata about each organization. 

## Results
Using bulleted lists and images to support your answers, address the following questions.

### Data Preprocessing
* The IS_SUCCESSFUL variable was the target for the model. It denotes whether an organizaion was trustworthy to fund. 

* The variables below are considered to be the features for the model. 
<img width="755" alt="Screen Shot 2022-07-31 at 1 16 44 PM" src="https://user-images.githubusercontent.com/95447175/182043642-26f3a97a-607b-40ec-b017-5137bbc24d30.png">

* The variables "EIN" and "NAME" are neither targets nor features, and were removed from the input data
<img width="577" alt="Screen Shot 2022-07-31 at 1 17 57 PM" src="https://user-images.githubusercontent.com/95447175/182043695-20194e38-bd11-4ad6-9680-734782869073.png">

### Compiling, Training, and Evaluating the Model

The optimized model has three hidden layers; 15 neurons in the first hidden layer, 11 neurons in the second hidden layer and 5 neurons in the third hidden layer. All three hidden layers were done with the using the Rectified Linear Unit (ReLU) function, but the outer layer was done with a Sigmoid function. I chose 4 activation functions total. I chose the ReLu functionn for the three hidden layers because this function is extremely simple to compute and it is because of these features that it is the most popular choice of activation function for hidden layers.
I used a sigmoid function because it outputs a value between 0 and 1, making it useful for binary classification problems such as the one in this case study. 

<img width="574" alt="Screen Shot 2022-07-31 at 2 07 53 PM" src="https://user-images.githubusercontent.com/95447175/182045381-6c42a668-33e0-41b0-a502-4647f9bf8cb3.png">

The original model had 80 neurons in the first hidden layer and 30 in the second hidden layer. The activation functions were relu for the hidden layers and sigmoid for the outer layer. The model ran 50 epochs and produced around a 73% accuracy.

* Were you able to achieve the target model performance?

* What steps did you take to try and increase model performance?

## Summary: 
The deep learning model yielded 78% accuracy after 3 iterations. The inital accuracy percentage was 72, and the next two attemps yielded 73% accuracy with a slight difference in numbers (.7271137237548828 versus .726064145565033). 

In my opinion, the 78% accuracy is not ideal in this scenario because the Charity is potentially giving large sums of money to organizations, and if they take the money without fulfilling their obligations, the charity has less money to give to legitimate causes. Since this analyis was a clafficication (IS_SUCCESSFUL), I recommend that another analysis be made, this time using a supervised ML model using binary clasifiers. A random forest model would be worth a try. 
