# Fast Monte Carlo Rendering via Multi-Rensolution Sampling 

### Takeaways
- However, these algorithms need to sample a substantial amount of rays per pixel to enable proper global illumination and thus require an immense amount of computation.
- Our method first generates two versions of a rendering:
  - One at a low resolution with a high sample rate (LRHS) and the other at a high resolution with a low sample rate (HRLS).
  - We then develop a deep convolutional neural network to fuse these two renderings into a high-quality image as if it were rendered at a high resolution with a high sample rate.
- Our idea to speed up ray tracing is to reduce the number of pixels that we need to estimate color values.
- we propose to generate two versions of renderig: 
  - a low-resolution rendering but at a resonable high spp rate (LRHS) and a high-resolution rendering but at a lower spp rate (HRLS).
- 내가 생각한 논문 이 아닌듯.