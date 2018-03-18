# poker-hands-classification

## Introduction

Poker classification is one of the classification problem where we predict the poker hand given the details of the 5 cards. The order of the cards is important. The dataset was obtained from https://archive.ics.uci.edu/ml/datasets/Poker+Hand.
The attributes include

1) S1 "Suit of card #1" 
Ordinal (1-4) representing {Hearts, Spades, Diamonds, Clubs} 

2) C1 "Rank of card #1" 
Numerical (1-13) representing (Ace, 2, 3, ... , Queen, King) 

3) S2 "Suit of card #2" 
Ordinal (1-4) representing {Hearts, Spades, Diamonds, Clubs} 

4) C2 "Rank of card #2" 
Numerical (1-13) representing (Ace, 2, 3, ... , Queen, King) 

5) S3 "Suit of card #3" 
Ordinal (1-4) representing {Hearts, Spades, Diamonds, Clubs} 

6) C3 "Rank of card #3" 
Numerical (1-13) representing (Ace, 2, 3, ... , Queen, King) 

7) S4 "Suit of card #4" 
Ordinal (1-4) representing {Hearts, Spades, Diamonds, Clubs} 

8) C4 "Rank of card #4" 
Numerical (1-13) representing (Ace, 2, 3, ... , Queen, King) 

9) S5 "Suit of card #5" 
Ordinal (1-4) representing {Hearts, Spades, Diamonds, Clubs} 

10) C5 "Rank of card 5" 
Numerical (1-13) representing (Ace, 2, 3, ... , Queen, King) 

11) CLASS "Poker Hand" 
Ordinal (0-9) 


## Approach

This particular classification problem was tried with various algorithms and among them Neural networks showed more promise.
The various algorithms used in this case were Support vector machines (with linear and radial basis function kernel), DecisionTreeClassifier, RandomForestClassifier.
The accuracies obtained from these algorithms weren't promising enough(50-75% accuracy). Multilayer Perceptron which is class of neural networks was tested and the obtained accuracy was greater than 90%.
With further tweaks, like using an one hot encoder and having a total of 85 neurons for the input layer(5x4 + 5x13) and using multiple hidden layers(3 in this case) we were able to obtain an accuracy of around 96%.
Since a large neural network is more prone to overfitting, the regularization parameter(alpha) was added to fix the high variance problem. Adam optimizer was used which has the advantage of converging to the minima at a faster rate.
The activation function used here us the standard rectified linear unit(relu). 

