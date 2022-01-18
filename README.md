Hash-based signatures offer a conservative alternative to post-quantum signatures with arguably better-understood security than other post-quantum candidates. Nevertheless, a major drawback that makes it less favorable to deploy in practice is the (relatively) large size of the signatures, and long signing and verification time.

We introduce SPHINCS-<img src="https://render.githubusercontent.com/render/math?math=\alpha">, a stateless hash-based signature scheme, which benefits from a twofold improvement. First, we provide an improved Winternitz one-time signature with an efficient size-optimal encoding, which might be of independent interest. Second, we give a variant of the few-time signature scheme, _FORC_, by applying the  Winternitz method. Plugging the two improved components into the framework of the state-of-the-art (stateless) hash-based [SPHINCS+](https://sphincs.org/index.html), with carefully chosen parameter choices, yields a certain degree of performance improvement. In particular, under the "small" series parameter set aiming for compact signatures, our scheme reduces signature size and signing time by 8-11% and 3-15% respectively, compared to [SPHINCS+](https://sphincs.org/index.html) at all security levels. For the "fast" series that prioritizes computation time, our scheme exhibits a better performance in general. E.g., when instantiating the simple tweakable hash function with SHA-256, our scheme reduces the signing and verification time by 7-10% and up to 10% respectively, while keeping roughly the same signature size. The security proofs/estimates follow the framework of [SPHINCS+](https://sphincs.org/index.html). To facilitate a fair comparison, we give the implementation of SPHINCS-<img src="https://render.githubusercontent.com/render/math?math=\alpha"> by adapting that of [SPHINCS+](https://sphincs.org/index.html), and we provide a theoretical estimate in the number of hash function calls. 

### Publications

An ePrint version is on the way.

### Libraries

TO APPEAR

### Talks

TO APPEAR

### Team Members

TO APPEAR

### Performance

We achieve up to 11% saving on signature size. We list below the experimental results on a desktop computer. (Time is measured by CPU cycles, size is measured by bytes.)

- Fast version, with simple tweakable hash instantiated with SHA256, security level are 128, 196, and 256

|  | 128bit| 192bit |  256bit| 
|- |--: | --: | --: | 
|  **KeyGen** | 1.7x10^6 | 1.4x10^6 | 3.8x10^6 |
|  **KeyGen Ratio**  | -13.44%  | -50.72%  | -47.87% |
|  **Sign** | 2.1x10^7  |   3.5x10^7 |  7.2x10^7 |
|  **Sign Ratio** | -7.11% | -10.28% | -8.64% |
|  **Verify** | 1.7x10^6 | 2.9x10^6 | 3.1x10^6  |
|  **Verify Ratio** |  -9.99%  |   -1.52% |  +1.70% |
|  **Size** | 17040  | 35640 |  49696 |
|  **Size Ratio**   | -0.28% | -0.07%  |  -0.32% |

- Small version, with the same parameter settings

|  | 128bit| 192bit |  256bit| 
|- |--: | --: | --: | 
|  **KeyGen** | 4.8x10^7 | 8.0x10^7 | 6.1x10^7 |
|  **KeyGen Ratio**  | -23.41%  | -12.66%  | +0.31% |
|  **Sign** | 4.6x10^8  |   7.2x10^8 |  6.6x10^8 |
|  **Sign Ratio** | -3.34% | -16.85% | -15.15% |
|  **Verify** | 1.2x10^6 | 2.0x10^6 | 3.3x10^6  |
|  **Verify Ratio** |  +58.48%  |  +65.25% |  +84.76% |
|  **Size** | 6960  | 14784 |  27104 |
|  **Size Ratio**   | -11.41% | -8.88%  |  -9.02% |

### Funding Acknowledgments

TO APPEAR
