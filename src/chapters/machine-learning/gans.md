# Generative Adversarial Networks

*Generative Adversarial Networks* (GANs) are a **class of machine learning framework**.

GANs were designed by **Ian Goodfellow** and his colleagues in **2014**, and consist of two neural networks, called the ***generator*** and the ***discriminator***, that are trained simultaneously through adversarial processes. Here's an overview of how they work and their components:

#### Generator (G):
The generator's role is to create data that is as similar as possible to real data.

It takes a random noise vector as input and transforms it into a data sample (e.g., an image).

#### Discriminator (D):

The discriminator's role is to distinguish between real data (from the training dataset) and fake data (produced by the generator).

It outputs a probability indicating whether a given input is real or fake.

### The process

1. The generator creates fake data samples.
2. These fake samples are combined with real samples from the training dataset and fed into the discriminator.
3. The discriminator evaluates all samples and attempts to classify them as real or fake.
4. The discriminator is trained to maximize the accuracy of its classifications.
5. The generator is trained to minimize the discriminator's ability to distinguish between real and fake data, effectively "fooling" the discriminator.

### Adversarial Nature

The generator aims to minimize the probability that the discriminator correctly identifies the fake data, while the discriminator aims to maximize its classification accuracy.

### Applications

- Image Generation:
- Data Augmentation:
- Super Resolution:
- Style Transfer:
- Text-to-Image Synthesis:
- Video Generation:

