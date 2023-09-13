
# Big Food Vision 🍔
In this project we working on `Food101` Dataset , In this Dataset we have 101 kind of food and for every food we have `1,000` Images (`750` for `train` and `250` `validation`).

We build a model to classify validation images to one of the `101 categories` . 

We go through these steps to build model:

## Step 1 
* Load Data
First we load dataset from tensorflow datasets
* Preprocess images
Neural network perform best when data is in a certain way (e.g `batched` , `normalized` , etc).However , not all data (including data from Tensorflow Dataset) comes like this .
so in order to get it ready for neural network, you'll often have to write peprocessing functions and map it to your data.
* Setup `Mixed Precision`
Mixed precision training involves using a mix of `float16` and `float32` tensors to make better use of your GPU's memory.
## Step 2 
* Build `Data Augmentation` layer
To prevent our model to `Overfit`  and to Improve our model `Generalization` , we use Augmentation layer.
* Build `Feature Extraction` model
First step in `Transfer learning` is `Feature Extraction` , so first we build our model and train our output layer.
* Next step is `Fine tuning` , In this step we unfreeze 50 layer and train our model for 12 epochs.
