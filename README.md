# pytorch_competition
the in-class competition of Zero-GANs Pytorch class

This project is based on a Kaggle competition task, using google figures to classify different types of flowers. 

Through this project, i learn how to start from scratch to build up a deep learning model to do the classification work.

There are three major procedures of the project:
1) Explore the dataset. I explore the labels of the flower classes, write code to draw histograms of flower classes distribution in the training dataset, and discuss how to encode flower classes. I found out that to mark 104 flower classes, using each node each class is less efficient. I decide to use Gray code to encode all the flower classes. In this way, instead of 104 nodes, we only need 8 nodes to do the task.
2) train a model. Just like the Assignment 4, we select one existing model resnet34 and one self-created cnn model, and use the existing helper functions in the course materials to train the model, trace the history, and compare the performances of the two models. I draw the scores, training error and validation errors of the two models together to immediately tell which model is better. 
3) Finally, use the better model, resnet34, to do the prediction based on the test data. There is no existing results for the testing data, so i just use the chosen model to do the prediction for each testing figure. 

Remaining questions: Although through this project, I got familar with the codes and procedures of such machine learning research, there are more things to learn.
1) the existing model's best performance within a small number of training epcohes is just around 60%. This is no use in reality. Then, how to improve the model performance. There are several ways, such as using other ways of encoding the flower classes, modifying the network structure, adding more preprocessing of the training data, adjusing the superparameters like num_epoch, learning rate, and batch size.
2) Gray code is efficient. However, in translating the raw prediction into Gray code, there are chances that the translated code is beyond the existing 104 classes. This occurs in the current study. This suggests that the coding scheme include the possibility of getting a result outside the training classes. This is an interesting issue that needs further discussion. In other words, though we set up the solution space, the evolved results may fall outside this space, leading to error or wrong results. 
3) From the figure of histogram of classes, some classes are much more frequent than the other. This biased distribution may also cause lower traning performances; for some classes, the model is over trained, for the other classes, the mode is less trained. 

Due to limit time, i have to stop here, hoping to use future time after the class to dig more into the above issues. Learning the model itself and the specific dataset are equally important.
