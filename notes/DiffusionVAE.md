## [ICLR 2015] NICE: Non-linear Independent Components Estimation
* Normalizing flow

## [ICLR 2018] Spectral Normalization for Generative Adversarial Networks
* Spectral norm bounds the lipschitz of linear convolution layers

## [ICML 2019] Invertible Residual Networks
* ResNet with Lipchetz constant < 1 can be inverted by viewing it as a Euler ODE solver

## [ICCV 2021] Emerging Properties in Self-Supervised Vision Transformers
* DINO

## [ICLR 2022] Image BERT Pre-training with Online Tokenizer
* Joint DINO and MIM like pre-training of images

## [TMLR 2024] DINOv2: Learning Robust Visual Features without Supervision
* Better DINO with mix of iBOT loss

## [CVPR 2025] Softvq-vae: Efficient 1-dimensional continuous tokenizer
* Align latent space to DINO leads to better diffusion VAE

## [CVPR 2025] Reconstruction vs. Generation: Taming Optimization Dilemma in Latent Diffusion Models
* Align latent space to DINO leads to better diffusion VAE

## [ICML 2025] DCTdiff: Intriguing Properties of Image Generative Modeling in the DCT Space
* Diffusion in DCT space of image

## [ICML 2025] Eq-vae: Equivariance regularized latent space for improved generative image modeling. 
* Equvariance loss is benefical to diffusion training

## [ICML 2025] Improving the Diffusability of Autoencoders
* Scaling invariance loss is benefical to diffusion training

## [ICML 2025] Masked Autoencoders Are Effective Tokenizers for Diffusion Models
* MAE training + reconstruction loss leads to better VAE for diffusion models
* Mode convergence theory + GMM metric

## [ICCV 2025] Scaling Language-Free Visual Representation Learning
* DINO on large dataset

## [ICCV 2025] REPA-E: Unlocking VAE for End-to-End Tuning with Latent Diffusion Transformers
* Xingjian Leng, Jaskirat Singh, Yunzhong Hou, Zhenchang Xing, Saining Xie, Liang Zheng
* REPA loss back prop to VAE encoder lead to faster convergence 

## [Preprint 2025] VQRAE: Representation Quantization Autoencoders for Multimodal Understanding, Generation and Reconstruction
* VQ version of RAE

## [AAAI 2026] Missing Fine Details in Images: Last Seen in High Frequencies
* DINO alignment loss of VAVAE only with low frequency parts

## [ICLR 2026] Diffusion Transformers with Representation Autoencoders
* Boyang Zheng, Nanye Ma, Shengbang Tong, Saining Xie
* latent diffusion model converges faster with DINO encoder.
* it is possible to use other encoder, but in general DINO > CLIP > MAE.
* it is also important to have DiT dim < latent dim, time shift and robust decoder training with noising

## [ICLR 2026] Latent Diffusion Model without Variational Autoencoder
* Minglei Shi, Haolin Wang, Wenzhao Zheng, Ziyang Yuan, Xiaoshi Wu, Xintao Wang, Pengfei Wan, Jie Zhou, Jiwen Lu
* DINO encoder + residual encoder, residual branch latent is aligned to DINO latent space. The latent is concated. The latent is optimized with reconstruction decoder and task decoder.

## [CVPR 2026] DA-VAE: Plug-in Latent Compression for Diffusion via Detail Alignment
* High resolution diffusion, by adding a high resolution latent through VAVAE and diffusion finetune

## [CVPR 2026] DeCo: Frequency-Decoupled Pixel Diffusion for End-to-End Image Generation
* Two stage diffusion, first on low frequency then on high resolution

## [Preprint 2026] One Layer Is Enough: Adapting Pretrained Visual Encoders for Image Generation
* autoencode the feature of RAE into fewer channel is benefical to diffusion

## [Preprint 2026] End-to-End Training for Unified Tokenization and Latent Denoising
* Shared parameter of diffusion model and tokenizer

## [Preprint 2026] Scaling Text-to-Image Diffusion Transformers with Representation Autoencoders
* Text to image diffusion model with Siglip image encoder
