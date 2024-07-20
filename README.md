# **Generative DeepLearning Model for Image Creation**
![Python](https://img.shields.io/badge/Python-3.12.4-blueviolet)
![Tensorflow](https://img.shields.io/badge/API-Tensorflow-fcba03)
![JupyterNB](https://img.shields.io/badge/Editor-JupyterNB-blue)
![keras](https://img.shields.io/badge/DeepLearning-Keras-red)

![intro_gan](https://github.com/aryanc381/Image-Generation-DL-Model/blob/main/ganintro.jpg)

In this project, I have made a ```GAN``` i.e generative adversarial network to generate completely new fashion clothing images. This model can be scaled to generate any type of images.

## Project Workflow
1. Importing dependencies.
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
   - In the end of the updated notebook trained the model overnight for 2000 epochs which gave me the accuracy I wanted.
   - I have shared the model as ```generatormodel.h5```
8. Saving the model as ```generatormodel.h5```.

## GAN Architecture (How does it work?)
A GAN or a generative Adversarial Network consists of two neural networks, a generator and a discriminator that are trained simultaneously through adversarial training.
The job of the generator is to create data indistinguishable to the original data and the discriminator is to distinguish between real and fake data. 

![gen_dis_img](https://github.com/aryanc381/Image-Generation-DL-Model/blob/main/ganimg.jpg)

### Components of a GAN
1. **Generator**
   - ```Purpose``` - To generate data
   - ```Input``` - Random noise of input vector
   - ```Output``` - Data that mimics the real data distribution vector.
2. **Discriminator**
   - ```Purpose``` - To distinguish between real and fake data.
   - ```Input``` - Data (either real or fake)
   - ```Output``` - A probability score indicating whether data is real or fake (0-1)
3. **Training Process**
   - ```Generate random data``` - Starting with generator and discriminator with random weights.
   - ```Generate fake data``` - The generator takes in random noise as input and produces fake data.
   - ```Training the discriminator``` - This is a 4 step process.
      1. Feed the discriminator with a batch of real data and label it as 1.
      2. Feed the discriminator with a batch of fake data and label it as 0.
      3. Calculate the discriminating loss by measuring the difference between real data and fake data.
      4. Update the discriminator weights to minimize the loss function.
   - ```Training the generator``` - This is a 5 step process.
      1. ```Generate random data``` - Feed the generator with random noise to produce fake data.
      2. ```data -> Discriminator``` - Feed this data to the discriminator to achieve probability score.
      3. ```Goal``` - The goal of the generator is to generate images for which the discriminator passes an accuracy score as close to 1 or 1 itself.
      4. ```Weights``` - Update the discriminator weights to minimize the loss function.
4. **Repetition** - Keep repeating this process to increase the accuracy of the Generator and Discriminator, and the most important thing while doing this is the rate at which the generator and discriminator are being trained.
5. **Adversarial Training**
   - This training is called adversarial which means conflict. The goal of the generator and discriminator is different here, isn't it? The job of the generator is to generate new images, similarly, the job of the discriminator is to judge if they are correct or incorrect.
   - This process is carried out by the network till the generator can create accurate images for which the discriminator will output [1].
6. **Problems with GAN**
   - ```Model Collapse``` - The generator outputs a limited range of images meaning it practically cannot generate new images.
   - ```Training Instability``` - The rate at which the discriminator or generator should be very fluent for this network to work which is hard to achieve.

## Conclusion
In this project, I successfully built and trained a Generative Adversarial Network (GAN) to generate fashion clothing images. This project demonstrated the potential of GANs to create new, realistic images from random noise input. The model was trained using TensorFlow and Keras, and the final generator model was saved as ```generatormodel.h5```.

## References 
1. [What are GANs](https://www.geeksforgeeks.org/generative-adversarial-network-gan/)
2. [Project link for Youtube explanation](https://www.youtube.com/watch?v=AALBGpLbj6Q&ab_channel=NicholasRenotte) 

## Usage
To use this project, follow these steps:

1. Clone the repository to your local machine:
```bash
git clone https://github.com/yourusername/your-repository.git
```
2. Navigate to the project directory:
```bash
cd your-repository
```
3. Install the required packages:
```bash
pip install tensorflow keras numpy matplotlib opencv-python scikit-learn
```
4. Finally, download and extract the dataset as described in the Dataset section.

5. Open the Jupyter Notebook:
```bash
jupyter notebook main.ipynb
```
6. Run the cells in the notebook to train and evaluate the model.
---
If you have any contributions to make or any queries/doubts related to the project, you can reach me at ```venomc381@gmail.com```.
