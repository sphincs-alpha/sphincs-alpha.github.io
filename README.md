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

We achieve up to 11% saving on signature size without sacrificing signing and verification time. We list the experimental results below. (Time is measured by CPU cycles, size is measured by bytes.)

- Fast version, with simple tweakable hash instantiated with SHA256, security level are 128, 196, and 256

| **KeyGen**       | **Ratio**  | **Sign**         | **Ratio**  | **Verify**       | **Ratio** | **Size** | **Ratio** |
| ---------------- | ---------- | ---------------- | ---------- | ---------------- | --------- | -------- | --------- |
| <img src="https://render.githubusercontent.com/render/math?math=1.4\times 10^6"> | <img src="https://render.githubusercontent.com/render/math?math={-50.72\%}"> | <img src="https://render.githubusercontent.com/render/math?math=3.5\times 10^7"> | <img src="https://render.githubusercontent.com/render/math?math=-10.28\%"> | <img src="https://render.githubusercontent.com/render/math?math=2.9\times 10^6"> | <img src="https://render.githubusercontent.com/render/math?math=-1.52\%"> | <img src="https://render.githubusercontent.com/render/math?math=35640">  | <img src="https://render.githubusercontent.com/render/math?math=-0.07\%"> |
| <img src="https://render.githubusercontent.com/render/math?math=3.8\times 10^6"> | <img src="https://render.githubusercontent.com/render/math?math=-47.87\%"> | <img src="https://render.githubusercontent.com/render/math?math=7.2\times 10^7"> | <img src="https://render.githubusercontent.com/render/math?math=-8.64\%">  | <img src="https://render.githubusercontent.com/render/math?math=3.1\times 10^6"> | <img src="https://render.githubusercontent.com/render/math?math=+1.70\%"> | <img src="https://render.githubusercontent.com/render/math?math=49696">  | <img src="https://render.githubusercontent.com/render/math?math=-0.32\%"> |

- Small version, with the same parameter settings

| **KeyGen**       | **Ratio**      | **Sign**         | **Ratio**      | **Verify**       | **Ratio**      | **Size** | **Ratio**  |
| ---------------- | ---------- | ---------------- | ---------- | ---------------- | ---------- | -------- | ---------- |
| <img src="https://render.githubusercontent.com/render/math?math=4.8\times 10^7"> | <img src="https://render.githubusercontent.com/render/math?math=-23.41\%"> | <img src="https://render.githubusercontent.com/render/math?math=4.6\times 10^8"> | <img src="https://render.githubusercontent.com/render/math?math=-3.34\%">  | <img src="https://render.githubusercontent.com/render/math?math=1.2\times 10^6"> | <img src="https://render.githubusercontent.com/render/math?math=+58.48\%"> | <img src="https://render.githubusercontent.com/render/math?math=6960">   | <img src="https://render.githubusercontent.com/render/math?math=-11.41\%"> |
| <img src="https://render.githubusercontent.com/render/math?math=8.0\times 10^7"> | <img src="https://render.githubusercontent.com/render/math?math=-12.66\%"> | <img src="https://render.githubusercontent.com/render/math?math=7.2\times 10^8"> | <img src="https://render.githubusercontent.com/render/math?math=-16.85\%"> | <img src="https://render.githubusercontent.com/render/math?math=2.0\times 10^6"> | <img src="https://render.githubusercontent.com/render/math?math=+65.25\%"> | <img src="https://render.githubusercontent.com/render/math?math=14784">  | <img src="https://render.githubusercontent.com/render/math?math=-8.88\%">  |
| <img src="https://render.githubusercontent.com/render/math?math=6.1\times 10^7"> | <img src="https://render.githubusercontent.com/render/math?math=+0.31\%">  | <img src="https://render.githubusercontent.com/render/math?math=6.6\times 10^8"> | <img src="https://render.githubusercontent.com/render/math?math=-15.15\%"> | <img src="https://render.githubusercontent.com/render/math?math=3.3\times 10^6"> | <img src="https://render.githubusercontent.com/render/math?math=+84.76\%"> | <img src="https://render.githubusercontent.com/render/math?math=27104">  | <img src="https://render.githubusercontent.com/render/math?math=-9.02\%">  |


### Funding Acknowledgments

TO APPEAR
