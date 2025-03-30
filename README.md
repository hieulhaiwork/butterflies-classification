# butterflies-classification

This is my personal project to classify 75 different classes of butterflies.

## Dataset

My dataset I used in the notebook come from a private competition but you now can find it on [Kaggle](https://www.kaggle.com/datasets/phucthaiv02/butterfly-image-classification)

The dataset features 75 different classes of Butterflies. The dataset contains about 1000+ labelled images including the validation images. Each image belongs to only one butterfly category.

## Model description

I used 2 models to classify independently then averaged the probability predictions of each model to take advantage of the strengths of each model to support each other and reduce the wrong prediction results due to overfitting during training. 

2 models that were fine-tuned based on "google/vit-base-patch16-224-in21k" and "microsoft/swin-base-patch4-window7-224". Specifically, for Google's model I kept its structure, unfreezed all layers aiming to capture all features of each classes thanks to its large number of parameters. Then with Microsoft's model with hierarchical feature maps, I freezed all convolution layers and changed the classification layer to my custom layer that I got after experiment several times. 

## Results

I used last 1500 images in dataset for testing and got about 94% accuracy. 

