
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
