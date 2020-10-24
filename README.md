# Binary Image Classification with CNN using ImageDataGenerator to prevent Overfitting 

We will build a Cats vs Dogs classifier using a basic Convolutional Neural Network architecture. 
We will focus on the use of **ImageDataGenerator** for `Image Augmentation` to help build a more robust model, even with less training data and while also avoiding overfitting.  

The dataset is obtained from a subset of Kaggle dataset titled 'Dogs & Cats Images', which can be found at the following link: 
https://www.kaggle.com/chetankv/dogs-cats-images

Steps performed:

1. Load dataset from directory.
2. Create CNN based model.
3. Train the model with given data, and test its accuracy and loss.
    We observe that while our Training accuracy has increased, the validation accuracy stops increasing after a certain point. Also, the Training loss goes down, but the Validation loss starts going up. This demonstrates a clear case of overfitting.
4. We now use ImageDataGenerator to augment our dataset with modified images of our Training set itself. This includes (but not limited to) Rotating, Shearing, Height/Width shifting, Horizontal flipping etc.
5. We train our model again with the augmented data.
    We can now observe that the Validation accuracy keeps increasing consistently alongwith the Training accuracy, while the Validation loss decreases too!