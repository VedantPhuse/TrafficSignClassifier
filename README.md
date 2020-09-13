# TrafficSignClassifier


![](https://i.imgur.com/QRRvaEk.png)

**Building a Traffic Sign Classifier using CNN.**

For this, I am using the **GSTRB** - **German Traffic Sign Recognition Benchmark** dataset to build a Traffic Sign Classifier using CNN.

I am making the Project using **Jupyter Notebooks** in **Google Colab** for faster processing and ability to use GPU, also the superfast download speeds of dataset.

The dataset is available on Kaggle and the link to the same is: https://www.kaggle.com/meowmeowmeowmeowmeow/gtsrb-german-traffic-sign

I am importing the dataset directly from Kaggle into my CoLab runtime, by uploading the API key for my account, and then using the API command `kaggle datasets download -d meowmeowmeowmeowmeow/gtsrb-german-traffic-sign` to download the dataset into runtime, and then unzipping the downloaded file using `!unzip gtsrb-german-traffic-sign.zip` command. [*I have cleared the output for this cell, as this command prints the name of each and every file inflated from the archive*.] 

Then I used **[PIL](https://www.pythonware.com/products/pil/)** library to read the image data and make a dataset, in **[Numpy](https://numpy.org/)** array.

Then I imported **[scikit-learn](https://scikit-learn.org/stable/)**  to use the in-built `train_test_split` function to divide the dataset into training and validation set(called as test set at the time of training the model). 

 
I am implimenting the model in [**Keras**](https://keras.io/).

I one-hot encoded the labels using `to_categorical` because that's needed in Keras to train the model. 

Then I made a multi-layer sequential model in **CNN**, using ReLU activation function, Dropout regularisation, and ADAM optimiser.

I compiled and then trained the model while using the `history` functionality of Keras, and fed into [matplotlib](https://matplotlib.org/), to generate the graphs of accuracy and loss. 

I got the Training and Validation accuracy of 98.38% and 99.50% respectively.

Then, on running the images in test set through the CNN Model, I got an accuracy of 95.03%. (I used scikit-learn metrics for this).

Finally, I uploaded three images into the runtime, and checked the output for each of them, in order to demonstrate the working of the project.

An example output is in this image:

![](https://i.imgur.com/VzdN6tl.png)

P.S. There might be a few `1+1` 's left in my code, which I might have forgotten to remove. These were done in order to renew the CoLab Runtime.
