# Bayesian feature weight selection using Markov Chains 
This project is about a model that generates alerts based on the score of 10 distinct features.
This implementation aims to find an efficient and elegant way to rank features based on their importance in creating relevant alerts. To do so, we will use an approach based on Bayesian probability and Markov Chain Simulations.

The rank defined by the Bayesian model can then be used to assign weights to each feature in order to improve the probability of generating alerts that are actually relevant, hence reducing the number of false positives.

The idea is to use a generative process like this: 

- Start from a small manually reviewed database where all the alerts are flagged as "Interesting" or "Not Interesting". (This is done in order to ensure that the model is actually trained on clean data.
- Set all the weights of the features to be equal.
- Define prior probabilities for each feature using a truncated normal distribution where the lower and upper limits are respectively 0 and 1.
- Use Markov Chains to simulate the distributions based on the prior probabilities.
- Compare the simulated distributions to the real data available.
- Update the weights.

From the results obtained, it is possible to use the mean of each feature to rank them based on their importance for the Interesting alerts.
Moreover, the standard deviation can be used to understand how confident is the estimation of the mean.

To conclude, given the rank of the feature it is possible to pick the weights for each variable based on our domain knowledge and the rank displayed, or by using indicators like the modal value and the mean itself.

Thanks :)

  
  



