SPHINCS-<img src="https://render.githubusercontent.com/render/math?math=\alpha"> is a stateless hash-based signature scheme, a stateless hash-based signature scheme, which improves upon the state-of-the-art stateless hash-based signature scheme [SPHINCS+](https://sphincs.org/index.html), while preserving the core elements that made the original SPHINCS+ a standout project. 


Hash-based signature is one of the most promising candidates for (and perhaps the most conservative approach to) post-quantum digital signatures. An advantage of hash-based signatures is that its (classical as well as quantum) security strength is better understood (and easier to evaluate) than other candidates, by solely relying on the idealized hardness of the cryptographic hash functions.

Our optimization mainly stems from the optimization of the one-time signature scheme, which we prove to have a size-optimal encoding scheme among all tree-structured one-time signatures.

### Publications

Our [paper](https://eprint.iacr.org/2023/850) is accepted by CRYPTO 2023.

### Performance

Performance of SPHINCS-α, with simple tweakable hash function instantiated with ``shake``. Key generation, signing, and verification time are in terms of CPU cycles; signature size is in bytes. Both public and secret keys are short (128 bytes).


| Para |  Keygen   |   Sign    |  Verify  | SigSize |
|:------|-----------:|----------:|----------:|---------:|
| 128f | 1.0x10^6 | 2.7x10^7 | 2.0x10^6| 16720  |
| 192f | 2.2x10^6 | 4.5x10^7 | 1.7x10^6|  34896  |
| 256f | 4.3x10^6 | 9.1x10^7 | 3.2x10^6| 49312  |
| 128s | 5.1x10^7 | 5.4x10^8 | 2.7x10^6| 6880  |
| 192s | 7.8x10^7 | 9.9x10^8 | 3.9x10^6|  14568  |
| 256s | 5.2x10^7 | 7.6x10^8 | 6.0x10^6| 27232  |

  



Performance comparison between SPHINCS+ and SPHINCS-α. Our scheme offers an overall performance improvement for most parameter settings, in terms of signing time and signature size. On the downside, we experience an up to 253% increase in verification time. Nevertheless, we argue that for specific scenarios where verification time is critical, we can re-tune the parameters towards fast verification.

| Para | Keygen | Sign | Verify | SigSize |
|:-----|------------:|----------:|------------:|-------------:|
| 128f |  -9.35%     | -0.88%    | -8.01%      | -2.15%       |
| 192f |   32.29%    |  -0.41%   | -41.93%     | -2.15%       |
| 256f |  -0.95%     | -0.79%    | 7.00%       | -1.09%       |
| 128s |  -29.17%    | -2.58%    | 217.74%     | -12.42%      |
| 192s |  -25.89%    | -3.26%    | 220.17%     | -10.21%      |
| 256s |  -24.60%    | -16.78%   | 252.99%     | -8.59%       |



### Team Members

Yu Yu (Shanghai Jiao Tong University)

Hongrui Cui (Shanghai Jiao Tong University) 

Kaiyi Zhang (Shanghai Jiao Tong University)
