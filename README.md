# Neural Network Charity Analysis
## Overview
The purpose of this analysis was to use a machine learning model to find if the funds allocated from Alphabet Soup are being used properly by the recipients. Specifically, we used our knowledge of machine learning and neural networks to find which of the companies would be successful if they received funding through Alphabet Soup.
## Results
- What variable(s) are considered the target(s) for your model?
  - The column "IS_SUCCESSFUL" if considered the target for this model.
- What variable(s) are considered to be the features for your model?
  - The model uses all other columns in the encoded_application_df to be the features of the model
- What variable(s) are neither targets nor features, and should be removed from the input data?
  - The columns "EIN" and "NAME" were removed from the initial applications data frame as they were neither targets or variables
- How many neurons, layers, and activation functions did you select for your neural network model, and why?
  - For this model, I chose to have 2 hidden layers, both using the ReLU activation functions to simply the output. In the first layer I used 80 neurons and 30 in the second. This follows the general rule of thumb suggested in the module to have 2-3 times the amount of neurons as inputs. I used the Sigmoid Function as the output activation function to create a clean binary output for the module to use to determine if the applicant would use their funds successfully.
- Were you able to achieve the target model performance?
![Original Output](https://github.com/AnnieShaffer/Neural_Network_Charity_Analysis/blob/main/Challenge/Images/AlphabetSoupCharityResults.png)
  - I was not able to achieve the target model performace with the original model or any of the optimized models.
- What steps did you take to try and increase model performance?
![Optimized Results 1](https://github.com/AnnieShaffer/Neural_Network_Charity_Analysis/blob/main/Challenge/Images/OptimizedAlphabetSoupCharityResults1.png)
  - In my first optimization attempt, I added neurons to the hidden layers. This did not increase the models performace, however, it did decrease the loss significantly. 
![Optimized Results 2](https://github.com/AnnieShaffer/Neural_Network_Charity_Analysis/blob/main/Challenge/Images/OptimizedAlphabetSoupCharityResults2.png)
  - In my second attempt, I adjusted the inputs to remove unnecessary columns from the data frame. This actually decrease the performance of the model and created a larger loss.
![Optimized Results 3](https://github.com/AnnieShaffer/Neural_Network_Charity_Analysis/blob/main/Challenge/Images/OptimizedAlphabetSoupCharityResults3.png)
  - In my third attempt, I combined the models from attempts 1 and 2 and reduced the number of values in the bins. This model also suffered a week performance and heavy loss.

## Summary
The results of this model show that it is not an optimal model to use as it did not reach the target model performance we were looking for. In the future, I believe that we could look further into adding or reducing neurons. This could however lead to overfitting, which we would have to be careful of. Additionally, we could look further into reducing the number of unnecessary variables.