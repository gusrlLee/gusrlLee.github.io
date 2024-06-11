# Hybrid CPU-GPU Texture Compression Methodology




<!-- |H-ETC2 System Overview| Performance |
|   :-:     |   :-:      |
|![fig:H-ETC2](./assets/H-ETC2.png)      | ![fig:teaser_image](./assets/teaser_image.png) |
### **H-ETC2 : Design of a CPU-GPU Hybrid ETC2 Encoder**    
#### Summary    
- 개요: CPU와 GPU를 활용하는 Hybrid ETC2 Encoding Pipeline 구축
- 담당: 전반적인 Ecnoding Pipeline 구현 및 실험

#### Details    
- 빠른 속도와 좋은 품질을 위해 OpenGL의 Compute Shader와 Multi-Threading, AVX2 SIMD Intrinsic 사용
- CPU Encoder 에서는 *"Problematic Pixel Block"* 을 판단을 하며 빠른 Encoding 진행
- 판단 된 *"Problematic Pixel Block"* 들은 GPU Encoder 의 input으로 전처리
- 생성 된 input image는 GPU Encoder 에 의해 Encoding 된 후 최종 Texture Compression 을 마무리
- Encoding Quality 측면 최대 20% 향상, Encoding Speed 측면 최대 100 ~ 1000% 향상 -->


---
[Home](../README.md)