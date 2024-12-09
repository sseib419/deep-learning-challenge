# deep-learning-challenge

In order to create a model to assist Alphabet soup in selecting who they should fund, first the charity data csv was read into a pandas dataframe, with the EIN and NAME columns dropped. A value count was done on the Application Type column to see if there were values that did not appear often, with the least appearing values put into a bin named Other. The same thing was done to the Classification column. The dataframe was put through the get dummies function to convert the columns with words into integers. The new dataframe was split into features and target arrays, and then split into the training and testing dataset. Using standard scaler, the feature data was scaled.

The purpose of this analysis is to create a tool that can assist Alphabet Soup in choosing the applicants they should fund, and this was done by creating and training a deep learning model that hopefully has a high enough accuracy in predicting good applicants. 

Variable targets 
• Is Successful column

Variable features
• Application Type
• Affiliation
• Classification
• Use Case
• Organization
• income amount
• special considerations
• ask amount

Variables that are neither targets or features
• status

• Originally a number of 2 hidden layers were used, with the 1st layer having 10 neurons and using the tanh activation function, and the 2nd layer having 5 neurons using the relu activation function. 100 epochs was used to train the model. I chose using the tanh activation function because it looks like the data is well balanced between applicants that are successful and those that are not. The number of neurons for each hidden layer was chosen so that there were enough to increase learning capacity and be better at approximating the data. My first attempt was not able to achieve target performance of 75%, so in my next attempts I changed the activation function, dropped additional columns, changed the number of neurons used, and the number of epochs used as well.

• Overall, after multiple optimization attempts, hopes of getting to 75% accuracy was not achieved, with the highest accuracy obtained being just under 73%. When trying to optimize the model further, increasing the number of hidden layers could be a possible solution which could lead to better learning of the data. Trying a different combination of activation functions for the hidden layers that are better suited for this kind of data could help accuracy as well.
