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


| Para |   Keygen   |     Sign    |   Verify  | SigSize |
|------|------------|-------------|-----------|---------|
| 128f |  1036602   |  26635716   |  2028186  |  16720  |
| 192f |  2199276   |  45218790   |  1744038  |  34896  |
| 256f |  4286574   |  91335474   |  3175290  |  49312  |
| 128s | 51421086   | 537033762   |  2689650  |   6880  |
| 192s | 78050718   | 988899534   |  3845970  |  14568  |
| 256s | 52048332   | 764352612   |  6005448  |  27232  |


