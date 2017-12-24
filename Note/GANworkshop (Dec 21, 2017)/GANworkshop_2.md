# GAN Most workshop & competition

> **speaker** : 李宏毅 ([profile](https://www.linkedin.com/in/soumith/))\
> **time** : afternoon, Dec 21, 2017


# Introduction to GAN

- like **Structure Learning/Prediction**
	- language translation
	- speech to text
	- chatbot


### Generator 
- 通常使用NN
- input vector 每個dimension有不同的意義，依據vector產生output
- 透過Gradient Descent 找出Discriminator高分處

### Discriminator
- also NN
- 用於評分
- bianry classifier (1 for real image, and 0 for fake one)

# special GAN

## LSGAN(Least Square GAN)
- 將sigmoid換成linear
- 超過1或小於0

## WGAN
- Sentence generation : but weak than RNN
- 改進linear,output scalar and find max scalar
- problem : 不會收斂
- 使用1-Lipschitz funcion,make function smooth, but how ?
	- Weight Clipping
	- improved WGAN : Gradient Penalty

## Loss-sensitive GAN (LSGAN)
- 定義圖片的好壞,算delta value(越小越好)

## Energy-based GAN (EBGAN)
- Using an autoencoder as discriminator D
- a good image can be **reconstructed by autoencoder**
- 透過對bottleneck layer dimension設定可限制可reconstruct的img數

## InfoGAN 
- 將input區分為兩部分(c,z'),在G ouput 加入一個Classifier,predict c

# condition Generation
- discriminator D 的input為generator G 的condition c & output x

## unsupervised:
- Cycle GAN / Disco GAN
- 引入另一個generator, 將first generator output再轉回input img，強迫input img與sec. generator output越相近越好

## feature extraction: (domain independent)
- 讓generator能抽feature
- domain adversial training : 加入**domain classifier**及**Label predictor**
- VAE-GAN
- BiGAN

# Reinforcement Learning
Actor, Env, Reward func
 
- 將Actor視為Generator, Env想成Discriminator(output reward)
- 若不能微分(沒有Gradient), 則用policy gradient train

## Imitation Learning
- 前提：沒有reward func, 只能透過 expert record 訓練

## Inverse Reinforcement Learning
- 用export record 找出 reward func.
- principle : expert always the best

# improved Seq2seq model
- minimize crossentropy = maximize Likelihood

## RL 
根據generator(decoder) output及 encoder input 作為Reward func的input

## unsupervised 
- Abstractive Summarization :
	- 使用autoencoder概念，兩側layers以兩個seq2seq代替, 但怎麼控制中間summaries的output
	- 使用discriminator驗證中間摘要output來控制
- Translation

## Text Style Translation
- 賦予文字情感
- Assumption : 有sentiment classifier.
- Approach
	1. 調整model本身
	2. 將model output作為sentiment input得到sentiment output
	3. Plug & Play
	4. Cycle GAN