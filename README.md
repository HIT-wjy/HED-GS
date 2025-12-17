# HED-GS:HIGH-FIDELITY DYNAMIC SURGICAL SCENE RECONSTRUCTION WITH HASH-GRID ENCODER DEFORMABLE GAUSSIAN SPLATTING  
## Ablation Study  
### Hash-grid hyper-parameters and their effect on speed/quality.  

| Setting | Levels (L) | Hash size (H) | Resolution (R, min→max) | PSNR ↑ | SSIM ↑ | LPIPS ↓ | Time (s) ↓ |
|---|---:|---:|---:|---:|---:|---:|---:|
| **Best (paper setting)** | **16** | **2^19** | **16→4096** | **38.93** | **96.21** | **0.05** | **89** |
| Fewer levels (lower capacity) | 12 | 2^19 | 16→4096 | 38.16 | 95.89 | 0.05 | 86 |
| More levels (diminishing returns / slower) | 20 | 2^19 | 16→4096 | 38.76 | 96.13 | 0.05 | 96 |
| Smaller hash table (more collisions) | 16 | 2^17 | 16→4096 | 38.43 | 95.97 | 0.05 | 95 |
| Larger hash table (diminishing returns / memory) | 16 | 2^21 | 16→4096 | 38.76 | 95.79 | 0.05 | 90|
| Higher max resolution (slower) | 16 | 2^19 | 16→8192 | 38.79 | 96.09 | 0.05 | 103 |

