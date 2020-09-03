# Naive_Bayes


# MNIST Dataset

We will use a preprocessed variant of the MNIST digits dataset in this assignment. The task is to classify hand-written digits. There is one class for each digit (i.e., classes 0,1,2,...,9). The features represent a scanned image (28×28 pixels, values in {0,1,...,255}). The dataset contains both training data ($\approx$ 6000 images per class) and test data ($\approx$ 1000 images per class)

\begin{enumerate}
\item \textbf{Training}

Provide a function nb train that trains a Naive Bayes classifier for categorical data using a symmetric Dirichlet prior and MAP parameter estimates. A description of the parameters and expected result can be found in the Python file. For example, you may assume that all features take values in {0,1,...,K$-$1}, where K is the number of possible values.


The dataset contains 10 classes (C), 784 features(D) which can take up values between 0 to 255.

The logarithm of the prior probability of the class is evaluated by evaluating the relative frequency of each class. 
If N$_c$ is the number of instances of class C and N is the total number of samples, then the logarithm of prior probability, logprior is evaluated by

$$
logprior = \log(\frac{N_c + \alpha - 1}{N + (\alpha -1)C})
$$

The class conditional log-likelihood of value v in feature j given a class c is similarly calculated by taking the logarithm of the relative frequency of a feature value v of feature j in class c.
