
## Independent Component Analysis A Tutorial
* Neural Networks 1999
* Independent Component Analysis
  * Definition of ICA:
    $$
    x_1,...,x_n,\\
    x_j = a_{j1}s_1 + ... + a_{jn}s_n.
    $$
  * $x_j,s_k$ are ramdom variable
  * Now assume $x$ is column vector
    $$
    x = As,\\
    x = \sum a_i s_i.
    $$
  * Also assume $s_i$ are statistically independent. -> follow non-gaussian distribution
  * assume mixing matrix is square, but can be related
    $$
    s = Wx = A^{-1}x
    $$
* Ambiguities of ICA
  * We can not determine the variance of independent components. 
  * We can not determine the order of independent components.
* Princuple of ICA
  * Nongaussian is independent, $w^T$ is a vector that maximizes the non-gaussianity of $w^Tx$. 
* Measures of nongaussianity
  * Kurtosis, negentropy
* Mutual information
  $$
  I(y_1,...,y_m) = \sum H(y_i) - H(y) = DKL(p(y_1,...,y_m)||p(y_1)...p(y_m))
  $$
  * for invertible linear transform $y = Wx$, we have
  $$
  I(y_1,...,y_m) = \sum H(y_i) - H(x) - \log |W|
  $$
  * When $y_i$ are not correlated and has unit variance
  $$
  I(y_1,...,y_m) = C - \sum J(y_i)
  $$
* Maximum likelihood
  * Assume $f_i$ are density functions of $s_i$, which is assumed to be known
    $$
    \mathcal{L} = \sum_t \sum_i \log f_i(w_i^Tx(t)) + T\log |W|
    $$
* Infomax principle
  * neural network $g_i(w_i^T x)$, $g(.)$ are some non-linear scalar function
    $$
    \mathcal{L} = H(g_1(w_1^Tx),...,g_n(w_n^Tx))
    $$
## Understanding Contrastive Representation Learning through Alignment and Uniformity on the Hypersphere
* alignment and uniformity as measures of representation quality
* those two metrics impact downstream task performance
* metric as loss lead to good performance

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
## Understanding Self-Supervised Learning via Latent Distribution Matching
* ICML 2026
* SSL maximize log probability under assumed latent model / alignment, while maximize latent entropy to prevent collapse / uniformity.
