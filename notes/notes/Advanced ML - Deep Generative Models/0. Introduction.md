----


## Motivation

- ML models that can generate data → complex distributions over real-world data (images, graphs, audio signals...)

----

## About generative models

##### 1. Deterministic Generative Models
e.g. computer graphics
```
Image = Renderer(object = cube, color = red, size=..., position = ..., ...)
```
##### 2. Statistical Generative Models
> combine data and prior knowledge (model family, loss function, optimization) to learn a **probability distribution**

#### Desiderata for Statistical Generative Models
1. **efficient sampling**: we want to easily sample new instances $x_{new} \sim p(x)$ that is similar to the training data
2. **efficient likelihood estimation**: we also want to easily evaluate $p(x)$ e.g. for MLE
3. **extract features**: we want to *optionally* be able to extract features/representations that capture the important aspects

#### Applications of Generative Models
- image generation
- 3D graphics, fluid dynamics
- speech + music synthesis
- drug discovery

----

## Complexity of real-world data

we need to be able to model real-world data which is usually
> multi-modal and asymmetric

##### Continuous distribution over high-dim data: Why not use Gaussian [mixture models](https://en.wikipedia.org/wiki/Mixture_model)?
similar to polynomials: can approximate any function with sufficiently high degreee
→ often impractical

##### Discrete distribution over high-dim data
- number of parameters grows exponentially with dimension
- think binary encoding: image with $N$ pixels needs $2^N-1$ values


