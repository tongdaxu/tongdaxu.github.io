## [NIPS 2024] How Diffusion Models Learn to Factorize and Compose
* Qiyao Liang, Ziming Liu, Mitchell Ostrow, Ila Fiete
* diffusion model learn to hyper-factoriz given factorized continous conditional inputs by learning orthogonal feature for both independent but also different values of same feature
* For 2D Gaussian bump images, diffusion model learn composition with few daat. However, it interpolate poorly

## [ICLR 2025] Representation Alignment for Generation: Training Diffusion Transformers Is Easier Than You Think
* Sihyun Yu, Sangkyung Kwak, Huiwon Jang, Jongheon Jeong, Jonathan Huang, Jinwoo Shin, Saining Xie
* align diffusion model with vision foundation model improves generalization
* different lauer index and foundation model effect performance
* strong linear correlation between classification accuracy and gFID

## [NIPS 2025] Why Diffusion Models Don’t Memorize: The Role of Implicit Dynamical Regularization in Training
* Two important timescale:
* $\tau_{gen}$ begin to generate high quality sample.
* $\tau_{mem}$ begin to memorize.
* $\tau_{gen} < \tau{mem}$. $\tau_{gen}$ is content to dataset n, $\tau_{mem}$ scales linearly.
* when model achieves a threshold, no memorization
* Architecture regularization and dynamic regularization

## [NIPS 2025] Understanding Hallucinations in Diffusion Models through Mode Interpolation
* Propose mode interpolation, that diffusion models smoothly interpolate data modes, lead to out of distribution data.
* By 1D, 2D GMM experiment, show discounitty of loss in diffusion decoder, lead to mode interpolation.
* Show that ood samples accompany high variance in trajectory and can thereby detected and removed.

## [NIPS 2025] On the Edge of Memorization in Diffusion Models
* Denoisers trained via gradient descent-like methods memorize or generalize depending on whether the empirical (training) loss is lower for parameter-matched memorizing denoisers or generalizing denoisers

## [Preprint 2025] Selective Underfitting in Diffusion Models
* Diffusion model generalizes as they approximate the score in some region while underfit in others.

## [ICLR 2026] On the Interpolation Effect of Score Smoothing in Diffusion Models
* Zhengdao Chen
* Analytical solution between score smoothing and interpolation when data underlying dimension is 1D.
* piece wise linear smoothed socre with theorem are proved based on two layer RELU NN.
* Analyatical ODE solution with piece wise linear smoothed score, with genenralization to high dimension with 1 inner dimension subspace

## [Preprint 2026, ICLR 2026 rej] Diffuse and Disperse: Image Generation with Representation Regularization
* Runqian Wang, Kaiming He
* replace REPA by disperse loss also improves diffusion generalization
* dispersion loss serves as contrasive learning w/o positive pairs

## [Preprint 2026] PixelGen: Improving Pixel Diffusion with Perceptual Supervision
* Zehong Ma, Ruihan Xu, Shiliang Zhang, 
* LPIPS + DINO loss is better than MSE for supervising pixel diffusion model. x-predictin fm loss is needed too.

## [ICML 2026] Latent Forcing: Reordering the Diffusion Trajectory for Pixel-Space Image Generation
* Alan Baade, Eric Ryan Chan, Kyle Sargent, Changan Chen, Justin Johnson, Ehsan Adeli, Li Fei-Fei
* Training pixel diffusion alone with a DINO feature makes it converge faster
* The timestep can not be sychronized. less noise to DINO branch is the key.

## [Preprint 2026] Generalization of Diffusion Models Arises with a Balanced Representation Space
* Zekai Zhang, Xiao Li, Xiang Li, Lianghe Shi, Meng Wu, Molei Tao, Qing Qu
* for intermediate representation of score estimation network, memeorizatoin comes from local and spiky representation.
* generalization comes from balanced representation that is both robust and dispersive
* theorems are proved using two layer RELU network

## [Preprint 2026] Diffusion Model's Generalization Can Be Characterized by Inductive Biases toward a Data-Dependent Ridge Manifold
* Ye He, Yitong Qiu, Molei Tao
* diffusion model sample converge to a manifold named ridge, which is determined by the low rank approximation of ground truth score jacobian
* during inference, the generated samples evolve by reach, align slide stage. The samples first enter neighbour of ridge, and the distance is controled by normal component of training error, and finally slide along ridge controlled by tangential component.
* theorems are proved using RFNN