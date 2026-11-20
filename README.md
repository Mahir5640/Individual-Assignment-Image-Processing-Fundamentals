# Image Processing Fundamentals - Option A

**Mahir Foysol Chowdhury**

## Question

Which fixed denoising method best restores the MATLAB sample image ## Reproduce the experiment

Open The noise was generated once using seed 42, Gaussian mean 0 and variance 0.01, followed by salt-and-pepper noise with density 0.02. The filters were a 3 x 3 median, Gaussian with sigma 1.5, and 3 x 3 median followed by Gaussian with sigma 1. Other settings used MATLAB defaults.

## Results

| Method | PSNR (dB) | SSIM |
|---|---:|---:|
| Degraded baseline | 18.09 | 0.3696 |
| Median 3 x 3 | 25.37 | 0.6232 |
| Gaussian, sigma 1.5 | 25.75 | 0.6921 |
| Median then Gaussian, sigma 1 | 26.37 | 0.7051 |

![Same 80 x 80 crop for all methods](results/zoom_comparison.png)

## Conclusion and limitation

Median then Gaussian, sigma 1 achieved the highest PSNR (26.37 dB). Median then Gaussian, sigma 1 achieved the highest SSIM (0.7051) and is my metric-based preference because preserving grain structure is the priority in this comparison. The experiment uses one reference image and one synthetic noise realization, so the same ranking may change with another image or noise level.

## AI assistance

I used ChatGPT to help draft the MATLAB code, structure the comparison, and generate the README.
