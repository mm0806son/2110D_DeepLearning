### Lecture 7 - Generative Adversarial Networks (GAN)

David HURTADO & Zijie NING

> Let's start with Deep Generative Models...

**Generative Models** is an unsupervised algorithm. Given training data, it can generate new samples from same distribution. 

The training data has **no labels**. The network tries to find some **underlying hidden structure** of data.

$\min _{\theta_{g}} \max _{\theta_{d}}\left[\mathbb{E}_{x \sim p_{\text {data }}} \log D_{\theta_{d}}(x)+\mathbb{E}_{z \sim p(z)} \log \left(1-D_{\theta_{d}}\left(G_{\theta_{g}}(z)\right)\right)\right]$

$\max _{\theta_{d}}\left[\mathbb{E}_{x \sim p_{\text {data }}} \log D_{\theta_{d}}(x)+\mathbb{E}_{z \sim p(z)} \log \left(1-D_{\theta_{d}}\left(G_{\theta_{g}}(z)\right)\right)\right]$

$\max _{\theta_{g}} \mathbb{E}_{z \sim p(z)} \log \left(D_{\theta_{d}}\left(G_{\theta_{g}}(z)\right)\right)$

$\nabla_{\theta_{d}} \frac{1}{m} \sum_{i=1}^{m}\left[\log D_{\theta_{d}}\left(x^{(i)}\right)+\log \left(1-D_{\theta_{d}}\left(G_{\theta_{g}}\left(z^{(i)}\right)\right)\right)\right]$

$\nabla_{\theta_{g}} \frac{1}{m} \sum_{i=1}^{m} \log \left(D_{\theta_{d}}\left(G_{\theta_{g}}\left(z^{(i)}\right)\right)\right)$
