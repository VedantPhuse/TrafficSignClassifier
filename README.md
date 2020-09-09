# TrafficSignClassifier

Building a Traffic Sign Classifier using CNN.

For this, I am using the **GSTRB** - **German Traffic Sign Recognition Benchmark** dataset to build a Sign Classifier using CNN.

I am making the Project using Jupyter Notebooks in Google Colab for faster processing and ability to use GPU, also the superfast download speeds of dataset.

The dataset is available on Kaggle and the link to the same is: https://www.kaggle.com/meowmeowmeowmeowmeow/gtsrb-german-traffic-sign

I am importing the dataset directly from Kaggle into my CoLab runtime, using the API command `kaggle datasets download -d meowmeowmeowmeowmeow/gtsrb-german-traffic-sign` 
and then unzipping the download file in the runtime.

Then I used **[PIL](https://www.pythonware.com/products/pil/)** library to read the image data and make a dataset, in **[Numpy](https://numpy.org/)** array.

Then I imported **[scikit-learn](https://scikit-learn.org/stable/)**  to use the in-built `train_test_split`. 

 
I am implimenting the model in [Keras](https://keras.io/) first for quick building of the model and then in [PyTorch](https://pytorch.org/) for getting deep control of the same.

## Keras Implimentation

I one-hot encoded the labels using `to_categorical` because that's needed in Keras to train the model. 

Then I made a multi-layer sequential model in **CNN**, using ReLU activation function, dropout regularisation, and ADAM optimiser.

I compiled and then trained the model while using the `history` functionality of Keras, and fed into [matplotlib](https://matplotlib.org/), to generate the graphs of accuracy and loss. 

## PyTorch Implimentation

This time, I converted the data stored as Numpy arrays into torch.Tensor, and stored them as torch variables.

I am fitting the data into the model, but running into some errors, and will 
- update the readme file 
- commit the PyTorch code 
- add the demostration video and photos to the readme

as soon as I am done.
