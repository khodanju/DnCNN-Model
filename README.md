## DnCNN MODEL 

# About Data
The data consists of 400 images of flowers. Data is divided into 5 categories:- Daisies,
Dandelions, Roses, Sunflowers, and Tulips.

# Feature Engineering
Gaussian Filter is applied to the original image with σ= 1,3,6,10.
Each image is standardized to 224*224 (Gray Scale).
The image is divided by 255 to normalize the data.

# Model Architecture
The model consists of 17 layers.
The first layer consists of conv2d+ReLU with filter size = 64 and kernel size (3,3) and
padding equal to same.
The next 15 layers have conv2d+ReLU+BN with the same filter size, kernel size, and
padding.
The last layer has con2d+ReLU with filter size = 1 ( because the output depth should be 1).
The optimizer used for the model is Adam with lr = 0.001 and the loss function is MSE.
Epochs for all the σ = 1,3,6,10 are kept at 100 for uniformity in the result.

# Quantitative analysis:
The different metrics used for quantitative analysis: 
Mean Square Error
Peak Signal to Noise Ratio
Structural Similarity Index



