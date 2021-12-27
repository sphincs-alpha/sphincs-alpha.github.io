SPHINCS Alpha is an improvement on the NIST PQC Round 3 hash-based signature [SPHINCS+](https://sphincs.org/index.html). This is the official site for this construction, where we provide technical specifications, experimental results, and a prototype implementation.

### Publications

TO APPEAR

### Libraries

TO APPEAR

### Talks

TO APPEAR

### Team Members

TO APPEAR

### Performance

We achieve up to 10% saving on signature size without sacrificing signing and verification time. We list the experimental results below.

Small version, with simple tweakable hash

| Parameter  | Keygen | Sign | Verify | Signature | pk | sk | 
| --- |  --- | --- | --- | --- | --- | --- |
|sha256-128s-simple   | 47681964|	457985448|	1202958|	6960|	32|	64|
|sha256-192s-simple | 80291520|	722659932|	2049930|	14784|	48|	96|
|sha256-256s-simple  | 60974802|	661839894|	3318174|	27104|	64|	128|


Fast version, with simple tweakable hash

| Parameter  | Keygen | Sign | Verify | Signature | pk | sk | 
| --- |  --- | --- | --- | --- | --- | --- |
|sha256-128f-simple   | 1727604 |	21354462|	1709622|	17040|	32|	64|
|sha256-192f-simple | 1364364 |	35095410|	2904768|	35640|	48|	96|
|sha256-256f-simple  | 3760272 |	72368298|	3138498|	49696|	64|	128|

### Funding Acknowledgments

TO APPEAR
