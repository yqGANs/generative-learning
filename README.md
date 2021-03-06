# Generative-learning
A python library for generative learning methods with PyTorch.

## List of Trainers Available
This repo has PyTorch implementations of training a Gan.
- Trainers for Unconditional Gans
  - sgan
  - lsgan
  - hingegan
  - wgan
  - wgan-gp
  - qpgan
  - rasgan
  - ralsgan
  - rahingegan
- Trainers for Conditional Gans
  - sgan
  - lsgan
- Trainers for CycleGan
  - lsgan
- Trainers for Pix2Pix
  - sgan
  - lsgan
  - ralsgan
  - rahingegan
- Trainers for Pix2PixHD
  - ralsgan
- Trainers for Progressive Gans
  - rasgan
  - ralsgan
  - rahingegan
  - wgan-gp
  
## List of Architectures Available
- Gans
 - Deconv DCGAN
 - PixelShuffle DCGAN
 - ResizeConv DCGAN
- Conditional Gans
 - Deconv DCGAN (with label)
- Img2Img (Pix2Pix, Pix2PixHD, CycleGan)
 - U-Net (Pix2Pix)
 - ResNetGan (Pix2Pix)
 - PatchGAN (70x70)
 - PatchGAN (286x286)
- Progressive Gan
 - Progressive Architecture
 
Gans, Conditional Gans, Img2Img mostly has options to chose normalization type, such as batchnorm, instancenorm, spectralnorm.

## Training
### Progressive Gan
[![PGGAN Training](https://img.youtube.com/vi/WUYDf0E7e9Q/0.jpg)](https://www.youtube.com/watch?v=WUYDf0E7e9Q)

The code for this training had some errors in the code, the new training video will be updated soon.

### Pix2Pix
[![Pix2Pix Training](https://img.youtube.com/vi/QnggTk63qH4/0.jpg)](https://www.youtube.com/watch?v=QnggTk63qH4)

Pix2Pix Trained on edge2shoe dataset. Because of the U-Net architecture, it trains faster than Pix2PixHD, and seems to converge faster, but in my opinion Pix2PixHD seems to have better generalized results, and less artifacts.

### Pix2PixHD
[![Pix2PixHD Training](https://img.youtube.com/vi/o7rx6FV0eMw/0.jpg)](https://www.youtube.com/watch?v=o7rx6FV0eMw)

Pix2PixHD Trained on edge2shoe dataset as you see, around 0:20 the dimension changes, which is where the Local Network gets added to the network and training begins. Around 0:41, the entire network will start finetuning. (Since Pix2PixHD's biggest advantage is that it trains on very high resolutions, I'll later upload Pix2PixHD trained on CityScapes dataset.)

## TODO
- [x] Add Spectral Normalization
- [x] Implement Progressive Gan
- [x] Implement Pix2PixHD
- [x] Add trained results
- [ ] Implement WaveGan (raw audio generation)
- [ ] make the losses into a function and put them in a single file (code cleaning)
- [ ] Implement BicycleGan (multimodal Pix2Pix)
- [ ] Improve README
- [ ] Implement StyleGAN
- [ ] Implement SPADE
