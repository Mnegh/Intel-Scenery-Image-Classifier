Project Code 499: Scenery Image Classification

There are three main codes to use:

i- CNN and ANN code
ii- Pre-trained models code
iii- SVM code.

i- CNN and ANN code:

Run Code cell [1] to import essential libraries.
***Importing dataset from google drive***
Run Code cell [2] to mount google drive if the data is on gdrive.
Run Code cell [3] to unzip the dataset zipfile that is in the specified directory.
Run Code cell [4] to specify the dataset directory which should be '/Data/"folder that contains images" ' which is in this case "499 Project" .
***Data processing***
Run Code cell [5] to define the function that will be showing the images if needed.
Run Code cell [6] to define the function that will generate the train valid test loaders.
Run Code cell [7] to obtain train valid and test loaders. Augment should be True if CNN model is desired, False for ANN.
Run Code cell [8] and [9]  to see random test and train images and [10] to see the class distribution of the train split by default.
***Setting up the models***
Run Code cell [11] and [12] to setup the CNN and ANN models.
Run Code cell [13] if ANN model is desired, and cell [14] for CNN.
Run Code cell [15] if a summary of the model and the current used GPU is desired.
Run Code cell [16] and [17] to define the loss criterion, the optimizer used, and the loss and accuracy calculation function.
Run Code cell [18] to define the main training function.
Run Code cell [19] to start training selected model. both models are trained for 100 epochs and early stop after 10 epochs of no reduction in validation loss.
***Visualizing the Results***
Run Code cell [20] to plot the training and validation loss and save them to gdrive.
Run Code cell [21] to plot the training and validation accuracy and save them to gdrive.
Run Code cell [22] to save the training history of the model.
Run Code cell [23] to obtain the accuracy of the model on the test split.
Run Code cell [24] to obtain random images, their true label, and the probability of each class when identifying. 
Run Code cell [25] to obtain the misclassified images and their probabilities.
Run Code cell [26] to define the function that will plot the confusion matrix.
Run Code cell [27] to obtain the confusion matrix.
***Notable Mentions***
Code cell [28] is not necessary and may be used if training with augmented images and calculating loss and accuracy with non augmented images is desired.


ii- Pre-trained models:

Run Code cell [1] to import essential libraries.
Run Code cell [2] to mount google drive if the data is on gdrive. (zip file may be uploaded directly to the VM)
***Data Preprocessing***
Run Code cell [3] to unzip the dataset zip file that is in the specified directory.
Run Code cell [4] to specify the dataset directory which should be '/Data/"folder that contains images" ' which is in this case "499 Project" .
Run Code cell [5] to define the function that will be showing the images if needed.
Run Code cell [6] to define the function that will generate the train valid test loaders.
Run Code cell [7] to obtain train valid and test loaders.
Run Code cell [8] and [9]  to see images from the test and train images and [11] to see the class distribution of the train split by default.
***Setting up the Model***
Run Code cell [12] and [13] to setup the desired models from the selection, e.g. name = 'vgg16', name = 'resnet50', name = 'squeezenet' etc.
Run Code cell [14] to transfer the weights to CUDA memory and get the summary of the model, with what GPU is in use.
Run Code cell [15] to set up optimizer and criterion, Negative loss likelihood is used since the models have a LogSoftmax at the output.
Run Code cell [16] to set up validation function that will run during training
Run Code cell [17] to set up the training function, the parameters are: 1-model, 2-criterion, 3- optimizer, 4- train_loader, 5- valid_loader, 6- save_file, 7- early_stop_epochs, 8- epochs
Run Code cell [18] to set up a temporary save directory for the model, also the default option is to train on the non-augmented images, change to "train_loader" for training on augmented images.
***Visualizing the Results***
Run Code cell [19] to visualize the training and validation loss acquired from the history Dataframe during training and save it.
Run Code cell [20] to visualize the training and validation accuracy acquired from the history Dataframe during training save it.
Run Code cell [21] to save the history Dataframe to excel to the directory of your choice.
Run Code cell [22] to get the predictions of the model.
Run Code cell [23] to obtain the confusion matrix of the results
Run Code cell [24] check the predictions of the model with the plot of the probabilities
Run Code cell [25] check the misclassified images.
***Saving and Loading Models***
Run Code cell [26] to save the model name, classifier, optimizer, and the weights.
Run Code cell [27] to load the model and its weights.
***Ensemble Method***
Run Code cell [28] Load all models wanted for ensemble
Run Code cell [29] & [30] & [31] to get the probabilities of each model for the validation dataset
Run Code cell [32] to search for the optimal weights for the validation set
Run Code cell [33] & [34] to use the weights found in the test dataset
Run Code cell [35] & [37] to get the final test accuracy and confusion matrix 

iii - SVM Image Classifier
Warning: This instance needs at 25GB of RAM

Run Code cell [1] to import essential libraries.
Run Code cell [2] to mount google drive if the data is on gdrive. (zip file may be uploaded directly to the VM)
Run Code cell [3] to unzip the dataset zip file that is in the specified directory.
Run Code cell [4] to specify the dataset directory which should be '/Data/"folder that contains images" ' which is in this case "499 Project" .
Run Code cell [5] & [6] to load the images
Run Code cell [7] to plot an image for each class
Run Code cell [8] to visualize the HOG features
Run Code cell [9] to flatten the RGB pixels and add hog features
Run Code cell [10] to create a matrix of the features of each image
Run Code cell [11] to use standard scaler on the dataset
Run Code cell [13] to split the data into training and testing
Run Code cell [14] to train the model.
Run Code cell [16] to predict the testing data.
Run Code cell [17] to measure the score.
Run Code cell [19] to plot the confusion matrix
