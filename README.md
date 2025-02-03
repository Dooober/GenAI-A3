# GenAI-A3

## Theory Questions

**Q1: Why is the KL Divergence term important in the VAE loss function?**

The KL Divergence term regularizes the latent space, ensuring that it is smooth and continuous. This allows the model to generate data from any point in the latent space.

**Q2: How does the reparameterization trick enable backpropagation through the stochastic layers of a VAE?**

The reparameterization trick transforms the random sampling into a differentiable function with a noise term drawn from a normal distribution.

**Q3: Why does a VAE use a probabilistic latent space instead of a fixed latent space?**

Using a probabilistic latent space allows the VAE to generate new data that closely resembles the input. Generating new data as diverse and realistic would not be possible with the fixed latent space.

**Q4: What role does KL Divergence play in ensuring a smooth latent space?**

Since the loss function includes both Reconstruction Loss and KL Divergence, both terms need to be balanced for successful training. Reconstructoon Loss focuses only on the accuracy of the model, where KL Divergence regularizes the latent space to ensure that it is smooth. It does this by minimizing the difference between the learned distribution and a standard Gaussian distribution. 

## Coding Tasks

**Task 1**

![Fully Connected VAE](images/FCVAE.png)

The fully connected layers were not effective for this image dataset. The quality of the output was low and did not really resemble the CIFAR10 dataset.

![Convolutional VAE](images/CVAE.png)

The convolutional layers were much more effective at capturing the data from the CIFAR10 dataset. The generated images more closely resemble CIFAR images.

**Task 2**

![Interpolated Images](images/interpolate.png)


**Task 3**
![Images throughout latent space](images/latent_space.png)

Images generated that are closer to the center of the latent space tend to perform somewhat better than images closer to the extreme. The images closer to A=0 are darker while the images closer to A=1 are lighter.