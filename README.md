# GAN-MNIST
Generative Adversarial Networks applied to MNIST dataset

<b>Generative adversarial networks (GANs) </b>are deep neural net architectures comprised of two nets, pitting one against the other (thus the “adversarial”). <br/>

GANs’ potential is huge, because they can learn to mimic any distribution of data. That is, GANs can be taught to create worlds eerily similar to our own in any domain: images, music, speech, prose. They are robot artists in a sense, and their output is impressive – poignant even. <br/> <br/>

## How GANs Works?
One neural network, called the generator, generates new data instances, while the other, the discriminator, evaluates them for authenticity; i.e. the discriminator decides whether each instance of data it reviews belongs to the actual training dataset or not.
<br/>

### GAN Steps
<img src="https://skymind.ai/images/wiki/GANs.png">
<br/>

<ul>
  <li>The Generator takes in random numbers and returns an image.</li>
  <li>This generated image is fed into the Discriminator alongside a stream of images taken from the actual dataset.</li>
  <li>The Discriminator takes in both real and fake images and returns probabilities, a number between 0 and 1, with 1 representing a prediction of authenticity and 0 representing fake.</li>
</ul>

## Code
The code was impplemented using Python 3, and had the follow dependences:<br/>
<ul>
  <li>Tensorflow</li>
  <li>Keras</li>
  <li>Numpy</li>
</ul>

## Results
<img src="https://matheusfacure.github.io/img/tutorial/vanilla_gan/digit_gan.gif">
The results can be seen above. Notice how, at the beginning of the training, RAG produces only noise. As the training happens, the generated images come closer and closer with handwritten digits. Eventually, the generated images all resemble each other. That means the training has collapsed. Or the generator has found that producing ones is a shortcut to trick the discriminator easily, or the discriminator is at a very low cost.
