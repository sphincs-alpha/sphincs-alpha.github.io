SPHINCS-<img src="https://render.githubusercontent.com/render/math?math=\alpha"> is a stateless hash-based signature scheme, a stateless hash-based signature scheme, which improves upon the state-of-the-art stateless hash-based signature scheme [SPHINCS+](https://sphincs.org/index.html), while preserving the core elements that made the original SPHINCS+ a standout project. 


Hash-based signature is one of the most promising candidates for (and perhaps the most conservative approach to) post-quantum digital signatures. An advantage of hash-based signatures is that its (classical as well as quantum) security strength is better understood (and easier to evaluate) than other candidates, by solely relying on the idealized hardness of the cryptographic hash functions.

Our optimization mainly stems from the optimization of the one-time signature scheme, which we prove to have a size-optimal encoding scheme among all tree-structured one-time signatures.

### Publications

Our [paper](https://eprint.iacr.org/2023/850) is accepted by CRYPTO 2023.


### Team Members

Yu Yu

Hongrui Cui

Kaiyi Zhang

### Performance

Performance of SPHINCS-α, with simple tweakable hash function instantiated with ``shake``. Key generation, signing, and verification time are in terms of CPU cycles; signature size is in bytes. Both public key and secret are short (128 bytes).

| Para |   Keygen   |     Sign    |   Verify  | SigSize |
|:-----|-----------:|------------:|----------:|--------:|
| 128f |  1036602   |  26635716   |  2028186  |  16720  |
| 192f |  2199276   |  45218790   |  1744038  |  34896  |
| 256f |  4286574   |  91335474   |  3175290  |  49312  |
| 128s | 51421086   | 537033762   |  2689650  |   6880  |
| 192s | 78050718   | 988899534   |  3845970  |  14568  |
| 256s | 52048332   | 764352612   |  6005448  |  27232  |



Our scheme offers an overall performance improvement for most parameter settings, in terms of signing time and signature size. On the downside, we experience an up to 253% increase in verification time. Nevertheless, we argue that for specific scenarios where verification time is critical, we can re-tune the parameters towards fast verification.

| Para | KeygenRatio | SignRatio | VerifyRatio | SigSizeRatio |
|:-----|------------:|----------:|------------:|-------------:|
| 128f |  -9.35%     | -0.88%    | -8.01%      | -2.15%       |
| 192f |   32.29%    |  -0.41%   | -41.93%     | -2.15%       |
| 256f |  -0.95%     | -0.79%    | 7.00%       | -1.09%       |
| 128s |  -29.17%    | -2.58%    | 217.74%     | -12.42%      |
| 192s |  -25.89%    | -3.26%    | 220.17%     | -10.21%      |
| 256s |  -24.60%    | -16.78%   | 252.99%     | -8.59%       |
