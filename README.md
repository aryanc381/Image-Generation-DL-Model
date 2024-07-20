# **Image Generative DeepLearning Model**
![Python](https://img.shields.io/badge/Python-3.12.4-blueviolet)
![Tensorflow](https://img.shields.io/badge/API-Tensorflow-fcba03)
![JupyterNB](https://img.shields.io/badge/Editor-JupyterNB-blue)
![keras](https://img.shields.io/badge/DeepLearning-Keras-red)

![intro_gan](https://github.com/aryanc381/Image-Generation-DL-Model/blob/main/ganimg.jpg)

In this project, I have made a ```GAN``` i.e generative adversarial network to generate completely new fashion clothing images. This model can be scaled to generate any type of images.

## Project Workflow
1. Importing dependancies.
2. Configuring tensorflow-GPU.
3. Extracting dataset.
4. Visualisation of dataset
   - 4.1 Scaling dataset values
   - 4.2 Unraveling tensorflow
5. Building the GAN
   - 5.1 Importing Modelling components
   - 5.2 Building the generator model
   - 5.3 Building the discriminator model
6. Custom training the GAN
   - 6.1 Setting up losses and optimizers
   - 6.2 Building the sub-class model
   - 6.3 Building callback using ModelMonitor class
   - Training the model for 20 epochs
   - 6.5 Reviewing the performance
7. Testing out the generator
   - I in the end of the udated notebook trained the model overnight for 2000 epochs which gave me the accuracy I wanted.
   - I have shared the model as ```generatormodel.h5```
8. Saving the model as ```generatormodel.h5```


