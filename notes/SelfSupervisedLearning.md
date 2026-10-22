## [ICML 2020] A Simple Framework for Contrastive Learning of Visual Representations
* Ting Chen, Simon Kornblith, Mohammad Norouzi, Geoffrey Hinton
* data aug is the key to contrasive learning. crop & resize, cutout are most effective alone. color + crop is best combination.
* a learnable nonlinear transform between representation and contrasive loss is important.
* contrasive learning requires larger batch size and more training steps

## [ICML 2020] Understanding Contrastive Representation Learning through Alignment and Uniformity on the Hypersphere
* Tongzhou Wang, Phillip Isola
* performance of SSL can be predicted by alignment loss $\mathbb{E}[||f(x) - f(x+)||]$ and uniformity loss $\mathbb{E}[||f(x) - f(y)||]$.
* using alignment and uniformity loss alone can achieve good SSL model.
* Preliminaries:
  * Assumption: data distribution $p(.)$ and positive pair distribution $p_+()$ is
    * Symmetric, such that $p_{+}(x,y)=p_{+}(y,x)$.
    * Matching marginal, such that $\int p_{+}(x,y) dy = p(x)$.

* Contrasive loss:
  $$
  \mathcal{L}(f,\tau,) = \mathbb{E}_{(x,x^+)~p_+,x^-\sim p}[-\log \frac{e^{f(x)^Tf(x^+)/\tau}}{e^{f(x)^Tf(x^+)/\tau} + \sum e^{f(x^{-})^Tf(x^+)/\tau}}],
  $$
  where $\tau$ is temperature.

* Infomax principle: Some works view the loss above as 
  $$ 
  \max I(f(x),f(y)) = D_{KL}(p(f(x),f(y))||p(f(x))p(f(y)))
  $$
* Intuition
  * Alignment: two sample from positive pair should be mapped to nearby features, and be invariant to noise factors
  * uniformity: cover uniy hypersphere and preserve information of data 

* Alignment loss
  $$
  \mathcal{L}_{a}(f,\alpha) = \mathbb{E}_{(x,x^+)\sim p_+}[||f(x) - f(x^+)||^\alpha_2] 
  $$
* Uniformity loss
  $$
  \mathcal{L}_{u}(f,t) = \mathbb{E}_{(x,x^-)\sim p}[e^{-t||f(x) - f(x^-)||^2_2}] 
  $$

## [ICML 2026] Understanding Self-Supervised Learning via Latent Distribution Matching
* SSL maximize log probability under assumed latent model / alignment, while maximize latent entropy to prevent collapse / uniformity.
