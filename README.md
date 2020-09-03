# Naive_Bayes

## Training
The dataset contains 10 classes (C), 784 features(D) which can take up values between 0 to 255.
The logarithm of the prior probability of the class is evaluated by evaluating the relative frequency of each class. If Nc is the number of instances of class C and N
is the total number of samples, then the logarithm of prior probability, logprior is evaluated by

logprior = log( (Nc + α − 1)/(N + (α − 1)C))

The class conditional log-likelihood of value v in feature j given a class c is similarly calculated by taking the logarithm of the relative frequency of a feature value v of feature j in class c.


## Prediction 
The unnormalized log joint probability for each class given an input Xi is evaluating by adding the log probability of each feature taking a feature value given by the new input. Thus obtained log probability is then added with the prior class probability to get the joint probability of each class given an input.
The joint probability is then normalized to obtain the most probable class and its corresponding probability(again log-ed).
