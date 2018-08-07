# RelativisticGAN-Tensorflow
Simple Tensorflow implementation of [RelativisticGAN](https://arxiv.org/pdf/1807.00734.pdf)

## Issue
* For 256x256, the network does not generate the image properly. (DCGAN Architecture)
* I think, `RaDRAGAN` more better than `RaLSGAN`

## Usage
### dataset

```python
> python download.py celebA
```

* `mnist` and `cifar10` are used inside keras
* For `your dataset`, put images like this:

```
├── dataset
   └── YOUR_DATASET_NAME
       ├── xxx.jpg (name, format doesn't matter)
       ├── yyy.png
       └── ...
```

### train
* python main.py --phase train --dataset celebA --Ra True --gan_type dragan

### test
* python main.py --phase test --dataset celebA --Ra True --gan_type dragan

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

*Name* | *Original* | *Original + Ra* |
:---: | :---: | :---: |
**GAN** | <img src = './assests/GAN.png' width = '640px' height = '640px'> | <img src = './assests/RaGAN.png' width = '640px' height = '640px'> |
　
**LSGAN** | <img src = './assests/LSGAN.png' width = '640px' height = '640px'> | <img src = './assests/RaLSGAN.png' width = '640px' height = '640px'> |
　
**DRAGAN** | <img src = './assests/DRAGAN.png' width = '640px' height = '640px'> | <img src = './assests/RaDRAGAN.png' width = '640px' height = '640px'> |

## Error
### Original DRAGAN
![dragan_error](./assests/DRAGAN_error.png)
* In the case of `DRAGAN`, the images are sometimes distorted during the training

## Author
Junho Kim
