# Neural_Network_Charity_Analysis
## Overview of the Analysis
### Purpose

Alphabet Soup's business team is looking to predict where to make investments. With our knowledge of machine learning and neural networks, the purpose of this project is to use the provided dataset and help create a binary classifier capable of predicting whether applicants will be successful if funded by Alphabet Soup. The dataset contains 34,000 organizations that have received Alphabet Soup funding. First, for Deliverable 1, a dataframe was created and variables were considered for the target(s) of the model and variables were considered for the feature(s). Then, the data was preprocessed to remove unnecessary columns and determine which columns could benefit from "binning" by analyzing the unique values of the columns. Once the categorical variables were determined, they were encoded using one-hot encoding and placed in a new dataframe, which was then merged with the original dataframe. For Deliverable 2, the new dataframe was compiled, trained, and evaluated using machine learning and deep learning neural networks. Lastly, for Deliverable 3, the model was put through several optimization techniques to try and reach a higher level of accuracy. The results of the various techniques are discussed below. 

### Results

#### Data Processing

1) What variables are considered the target(s) for your model?

The variable that was used as the target was IS_SUCCESSFUL. We ultimately want to determine the model's accuracy of predicting successful applicants funded by Alphabet Soup.

2) What variables are considered to be the features of your model?

The variables that were considered to be the features of our model were: APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, INCOME_AMT, SPECIAL_CONSIDERATIONS.

3) What variables are neither the targets nor features, and should be removed from the input data?

Initially, EIN and NAME were removed from the input data as variables that would neither be considered targets nor features.
		
#### Compiling, Training, and Evaluating the Model

4) How many neurons, layers, and activation functions did you select for your neural network model and why?

Initially, I included 2 input layers with 10 neurons for the first layer and 5 neurons for the second layer. Relu was used as the activation function for the 2 input layers and sigmoid was used as the activation function for the output layer. I chose these initially because they were similar to those used in the training module. 

5) Were you able to achieve the target model performance?

The accuracy was around 72% - 73% which is below the target model performance of 75 %.

6) What steps did you take to try and increase the model performance?

I took several steps to try and increase the model performance. These included: 

1) Adjusting the input data to remove additional unnecessary variables.

![Delete Columns](https://user-images.githubusercontent.com/98500639/178120467-ff10bcc8-abb2-4f5e-955e-07fae5f36b7f.png)
![DELETE COLUMNS ACCURACY](https://user-images.githubusercontent.com/98500639/178120471-f31fe1a8-7d4c-4254-9630-f6c14600abd8.png)

2) Adding more neurons

![Increased nodes](https://user-images.githubusercontent.com/98500639/178120456-c9b4cbc3-8b72-4509-9c90-d65dffdde329.png)
![increased nodes accuracy](https://user-images.githubusercontent.com/98500639/178120458-b4c864dd-03b4-497b-a7e6-dc9737bdf9fb.png)

3) Adding more layers. 

![Increased hidden layers](https://user-images.githubusercontent.com/98500639/178120443-3f8d3898-efac-4f60-91a4-11233a5b76cf.png)
![Increased Hidden Layers to 4](https://user-images.githubusercontent.com/98500639/178120437-9d8501af-9cf8-4f73-90ba-b243faf2a777.png)

4) Changing the activation function.

![Increased nodes and tanh activation](https://user-images.githubusercontent.com/98500639/178120482-54f78ed9-45d4-4503-9bfb-9009df52c878.png)
![increased nodes and tanh activation accuracy](https://user-images.githubusercontent.com/98500639/178120490-3bb3c9ec-9cdc-4093-a811-0b5f8a54bf0f.png)

I actually tried many combinations of each of these, as well as those perhaps not listed. I have included an example of a final code in this repository that includes at least 3 attempted techniques at optimization. The file is called AlphabetSoupCharity_Optimization.ipynb and you can see the code here. (link). The evaluation results were similar to all attempts.

### Summary
Overall, I was unable to reach the desired performance of 75%, even when attempting several optimization techniques. In summary, I do not think this model can reach higher than 72%-73%. It seems as though the model is actually very overfitted. Perhaps a suggestion would be to use a Supervised machine learning technique instead. We have compared Random Forest technique to Deep Learning with favorable results leaning towards Random Forest, especially due to its speed. My suggestion would be to try a Random Forest model. 
