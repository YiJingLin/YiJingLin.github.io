# GAN Most workshop & competition

> **speaker** : Soumith Chintala ([profile](http://speech.ee.ntu.edu.tw/~tlkagk/))\
> **time** : morning, Dec 21, 2017


# GAN introduction

## history
- Wavelet-based : Generate texture
- Image quilting :
	 - Overlap image, generate texts, style transform
- Autoencoders:
	 - Bottleneck layer in the middle, loss=MSE
- Variantional Autoencoder
- Auto-regressive models
- Pixel-CNN
	- better than Autoencoder in image generation
- **Generative Adversarial Networks** :
	- problem : How to define loss ? How to define similarity in matathetic?
	- Sol. : learn itself
	- Drawbacks in original work:
		1. No condition-generation
		2. Unstalbe training
		3. saccross architecture
		4. across datasets
		5. across domains
		6. No way to evaluate other than looking at samples
	- Class-conditional GANs

- Better architectire based on GAN
	1. DCGANs : Latent space arithmetic
	2. Stack GAN : more stable, train recursively
	3. Progressive GAN : add new layer between G and D 

## Regularizer
- Norm of gradient
- Wasserstein GAN, improved WGAN
- Spectral Normalization for GANs: [link](https://openreview.net/forum?id=B1QRgziT-)

## Evaluation / validation
- Wasserstein Distance : Wasserstein GAN
- Inception score : Impre Tach for training GANs
- Frechet Inception Distance : GAMs trained by a Two Time-Scale Update Rule Converge to a Local Nash Equilbrium

## Other domians
- Video Predictions
	- add MSE at Sample
- Image in-painting :
- Text-conditional GANs
- image to image translation

## Open problems
- Stability of GANs
- Evaluation of generative models
- long-term video prediction


## Comparision to Classification ConvNets
- Throw things at the wall and see what sticks
- intuition is proper
-

## Tips for Training GANs
1. Normalize the inputs
2. Modified loss function (classic GAN)
	- min log 1-D in paper, but max log 1-D in practice
3. Use spherical 'z'
4. BatchNorm
	- differnet batches for real and fake
	- when batcjnorm is not an option use instance
5. Avoid Sparse Gradients : 
	- most grandient = 0
	- ReLU, MaxPool
	- Leaky ReLU
6. Soft and Noisy Labels
7. Architectures : 
	- DCGANs / Hybrids
8. Stability tricks from RL [Pfau & Vinyals (2016)]()
9. Use Gradient Penalty
10. DONT balance via loss statistics (classic GAN)
11. Add noise to inputs, decay over time
12. **Train Discriminator more** (especially when you have noise)
13. Avoid descrete spaces (Pose the generation as a continuous prediction)
14. Discrete Variables (for condition-GAN)
	- Use embedding Layer
	- Add as additional channel to image


# PyTorch


## Advantage
- defualt dataset in pytorch community
- environmnet (RL)
- debug
- find bottleneck
- compilation time
- Ecosystem
- model-zoo

## Recent feature
- Distributed pytorch
- Higher order derivatives
- Broadcasting
