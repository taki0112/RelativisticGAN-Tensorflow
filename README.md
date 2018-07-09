# RelativisticGAN-Tensorflow
Simple Tensorflow implementation of [RelativisticGAN](https://arxiv.org/pdf/1807.00734.pdf)

## Summary
***"the discriminator estimates the probability that the given real data is more realistic than a randomly sampled fake data"*** 

*= RGAN*

***"the discriminator estimates the probability that the given real data is more realistic than fake data, on average"*** 

*= RaGAN*
### Idea
![idea](./assests/idea.png)

### Formulation
*Name* | *Formulation*
:---: | :---: |
**GAN**| <img src = './assests/formulation/original_gan.png' height = '70px'>
　
**RGAN**| <img src = './assests/formulation/RGAN.png' height = '70px'>
　
**RaGAN**| <img src = './assests/formulation/RaGAN.png' height = '120px'>
　
**RaGAN-GP**| <img src = './assests/formulation/RaGAN-GP.png' height = '150px'>
　
**RaLSGAN**| <img src = './assests/formulation/RaLSGAN.png' height = '100px'>
　
**RaHingeGAN**| <img src = './assests/formulation/RaHingeGAN.png' height = '120px'>

## Results
* 128x128 celebA
* 200k iterations (but, 100k iteration is also enough)
* **RaDRAGAN** is not in the paper, I just tried because I wanted to do it.
* 256x256 celebA is being training, but quality is not good...

### RaGAN

### RaLSGAN

### RaDRAGAN

### RaHingeGAN (in training)

## Author
Junho Kim
