# GAN
## What are GANs?
Generative Adversarial Networks (GANs) are one of the most interesting ideas in computer science today. 
Two models are trained simultaneously by an adversarial process. 
A generator ("the artist") learns to create images that look real, while a discriminator ("the art critic") learns to tell real images apart from fakes.
During training, the generator progressively becomes better at creating images that look real, while the discriminator becomes better at telling them apart. 
The process reaches equilibrium when the discriminator can no longer distinguish real images from fakes.
## What is a DCGAN?
A DCGAN is a direct extension of the GAN described above, except that it explicitly uses convolutional and convolutional-transpose layers in the discriminator and generator, respectively. 
The discriminator is made up of strided convolution layers, batch norm layers, and LeakyReLU activations. 
The input is a 3x64x64 input image and the output is a scalar probability that the input is from the real data distribution. 
The generator is comprised of convolutional-transpose layers, batch norm layers, and ReLU activations.
The input is a latent vector, z, that is drawn from a standard normal distribution and the output is a 3x64x64 RGB image.
The strided conv-transpose layers allow the latent vector to be transformed into a volume with the same shape as an image. 
