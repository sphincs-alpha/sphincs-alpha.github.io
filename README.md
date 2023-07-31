SPHINCS-<img src="https://render.githubusercontent.com/render/math?math=\alpha"> is a stateless hash-based signature scheme, a stateless hash-based signature scheme, which improves upon the state-of-the-art stateless hash-based signature scheme [SPHINCS+](https://sphincs.org/index.html), while preserving the core elements that made the original SPHINCS+ a standout project. 


Hash-based signature is one of the most promising candidates for (and perhaps the most conservative approach to) post-quantum digital signatures. An advantage of hash-based signatures is that its (classical as well as quantum) security strength is better understood (and easier to evaluate) than other candidates, by solely relying on the idealized hardness of the cryptographic hash functions.


### Publications

Our [paper](https://eprint.iacr.org/2023/850) is accepted by CRYPTO 2023.

### Libraries

TO APPEAR

### Talks

TO APPEAR

### Team Members

Yu Yu

Hongrui Cui

Kaiyi Zhang

### Performance

We achieve up to 11% saving on signature size. We list below the experimental results on a desktop computer. (Time is measured by CPU cycles, size is measured by bytes.)

- Fast version, with simple tweakable hash instantiated with SHA256, security level are 128, 196, and 256

|  | 128bit| 192bit |  256bit| 
|- |--: | --: | --: | 
|  **KeyGen** | 1.7x10^6 | 1.4x10^6 | 3.8x10^6 |
|  **Sign** | 2.1x10^7  |   3.5x10^7 |  7.2x10^7 |
|  **Verify** | 1.7x10^6 | 2.9x10^6 | 3.1x10^6  |
|  **Size** | 17040  | 35640 |  49696 |
|  **KeyGen Ratio**  | -13.44%  | -50.72%  | -47.87% |
|  **Sign Ratio** | -7.11% | -10.28% | -8.64% |
|  **Verify Ratio** |  -9.99%  |   -1.52% |  +1.70% |
|  **Size Ratio**   | -0.28% | -0.07%  |  -0.32% |

- Small version, with the same parameter settings

|  | 128bit| 192bit |  256bit| 
|- |--: | --: | --: | 
|  **KeyGen** | 4.8x10^7 | 8.0x10^7 | 6.1x10^7 |
|  **Sign** | 4.6x10^8  |   7.2x10^8 |  6.6x10^8 |
|  **Verify** | 1.2x10^6 | 2.0x10^6 | 3.3x10^6  |
|  **Size** | 6960  | 14784 |  27104 |
|  **KeyGen Ratio**  | -23.41%  | -12.66%  | +0.31% |
|  **Sign Ratio** | -3.34% | -16.85% | -15.15% |
|  **Verify Ratio** |  +58.48%  |  +65.25% |  +84.76% |
|  **Size Ratio**   | -11.41% | -8.88%  |  -9.02% |

### Funding Acknowledgments

TO APPEAR
