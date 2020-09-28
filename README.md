# Face-Mask-Detection
This is the project on deep learning, it uses TensorFlow, OpenCV, and some other important libraries. This model detects the mask on your face.


    Face Mask Detection

This contains 3 sections - 1) Data Preprocessing 2) Training of Model 3) Final Prediction
Please first go through the code and download the dataset and other provided files to deploy this model.
The file which I attach with this article contains - dataset, data preprocessing code, training of data code, final prediction code, data.npy, target.npy, haarcascade_frontalface_default, model-017.model.
Please download this file, and then read the codes properly, try to understand them.




1) Data Preprocessing Process

In this process, we are preprocessing our data like- converting images to gray, dimensionality reduction, normalization.

Before doing this we first load the path of our dataset, there are two folders in the dataset folder- with mask, without mask.

We label out "with mask" folder as 0 and "without mask" as 1.


Then we use preprocessing steps and store our processed images in the data list and target values in target list.

And at last, convert them into an array and save them.




2) Training the data

Using convolutional layers performing neural operations on the layers.

Applying Conv2D, activation function-relu, and maxpooling methods. Then applying flatten, and dense on the layers.

Divide the data into train, cross validation and test sets.

Finally applying ModelCheckpoint, this will save your summed weights and other operations at the given checkpoints.In this function "model-{epoch:03d}.model" this is the path where this trained model will get saved.

Then using model.fit() function training of our model gets started.




3) Prediction Step

In this, we will use our trained model, run the live camera and start the prediction. 

This code is simple, just you need to make rectangles on the face of the person and if he's wearing the mask then write MASK there above the rectangle or else write WEAR YOUR MASK above the rectangles with different suitable colors.



