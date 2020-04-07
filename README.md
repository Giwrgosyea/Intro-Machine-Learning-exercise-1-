# Intro-Machine-Learning-exercise-1-

I use the wine-red data. I download them from the internet istead of open it from my local files.

a) Using the decision tree function I calculate the decision tree with max_depth 5 to avoid overfit , with feature_importances_ I find the 2 most prominent features. Those are alcohol and sulphates. 

b)
Before solving:
Why stohastic gradient descent instead of gradient descent?
In both gradient descent and stohastic you update a set of parameters in an iterative manner to minize an error function. While in GD, you have to run through all the samples in your training set to do a single update for a parameter in a particular iteration, in SGD, on the other hand, you use only one of training sample from your training set to do the update for a parameter in a particular iteration. Thus, if the number of training samples are large, in fact very large, then using gradient descent may take too long because in every iteration when you are updating the values of the parameters, you are running through the complete training set. On the other hand, using SGD will be faster because you use only one training sample and it starts improving itself right away from the first sample.
SGD often converges much faster compared to GD but the error function is not as well minimized as in the case of GD. 

Using the SGDClassifier with constructor  learning_rate='invscaling' , loss='squared_loss' according to scikit learn documentation for 100 epochs. And plot the loss function , calculated with means square error , with the epochs. As you see from the plot diagram the loss declines for each epoch. By changing alpha I plot 3 diagrams as you see the diagrams are different to each other due to changed alpha.From the produced diagramms the smaller the alpha the smaller the loss.


How scalling/normalize affect the model:
By scaling/normalize the data using the SGD the domination of one or several feature others is avoided.

Cost function of each one prominent:
With the best alpha.For each prominent(sulphates,alcohol) I plot bias,coefficient, loss for each epoch. According to my calculation the model declines so as the epoch passes the model declines to a very small price in order to find the local minimum.



c) I use SGDclassifier for logistic regression but with loss=’log’ according to the documentation is for logistic regression. Mean square and loss log is calculate to compare the 2 diagramms.
