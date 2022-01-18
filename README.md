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

We achieve up to 11% saving on signature size without sacrificing signing and verification time. We list below the experimental results on a desktop computer. (Time is measured by CPU cycles, size is measured by bytes.)

- Fast version, with simple tweakable hash instantiated with SHA256, security level are 128, 196, and 256

| **KeyGen**           | **Ratio**        | **Sign**             | **Ratio**      | **Verify**           | **Ratio**       | **Size**    | **Ratio**     |
| -------------------- | ---------------- | -------------------- | -------------- | -------------------- | --------------- | ----------- | ------------- |
|  1.7x10^6  |  {-13.44\%}  |  2.1x10^7  |  -7.11\%   |  1.7x10^6  |  -9.99\%    |  17040  |  -0.28\%  |
|  1.4x10^6  |  {-50.72\%}  |  3.5x10^7  |  -10.28\%  |  2.9x10^6  |  -1.52\%    |  35640  |  -0.07\%  |
|  3.8x10^6  |  -47.87\%    |  7.2x10^7  |  -8.64\%   |  3.1x10^6  |  +1.70\%  |  49696  |  -0.32\%  |

- Small version, with the same parameter settings

| **KeyGen**           | **Ratio**      | **Sign**             | **Ratio**      | **Verify**           | **Ratio**      | **Size**    | **Ratio**      |
| -------------------- | -------------- | -------------------- | -------------- | -------------------- | -------------- | ----------- | -------------- |
|  4.8x10^7  |  -23.41\%  |  4.6x10^8  |  -3.34\%   |  1.2x10^6  |  +58.48\%  |  6960   |  -11.41\%  |
|  8.0x10^7  |  -12.66\%  |  7.2x10^8  |  -16.85\%  |  2.0x10^6  |  +65.25\%  |  14784  |  -8.88\%   |
|  6.1x10^7  |  +0.31\%   |  6.6x10^8  |  -15.15\%  |  3.3x10^6  |  +84.76\%  |  27104  |  -9.02\%   |


### Funding Acknowledgments

TO APPEAR
