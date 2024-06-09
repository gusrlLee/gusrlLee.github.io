# Hyeon-ki Lee
**Keywords**: Ray/Path Tracing, Real-Time Rendering, Texture Compression, Image Processing 
**Objective**: Develop or research Real-Time Applications such as Rendering, Image processing, and Ray/Path Tracing by utilizing CPU (Multi-threading, SIMD Intrinsic) and GPU (Graphics API, GPGPU).

## Projects
![fig:H-ETC2](./assets/H-ETC2.png){: width="90%" height="90%"}{: .align-center}
**H-ETC2 : Design of a CPU-GPU Hybrid ETC2 Encoder**
#### Summary
- 개요: CPU와 GPU를 활용하는 Hybrid ETC2 Encoding Pipeline 구축
- 담당: 전반적인 Ecnoding Pipeline 구현 및 실험
#### Details
- OpenGL의 Compute Shader와 Multi-Threading, AVX2 SIMD Intrinsic 사용
- Encoding Quality 측면 최대 20% 향상, Encoding Speed 측면 최대 100 ~ 1000% 향상
  

![fig:MBVH](./assets/MBVH.png){: width="90%" height="90%"}{: .align-center}
**Multi-Bounding Volume Hierarchy (MBVH) for Sound Propagation**
#### Summary
- 개요: Ray Tracing method 를 사용하는 Geometry-Acoustics (GA) 기반의 Sound Propagation 가속을 위한 Acceleration Structure 비교 실험
- 담당: Ray Tracing 의 Acceleration Structure 로 사용되는 Multi Bounding Volume Hierarchies (MBVH) 구현 및 실험
#### Details
- Mobile device를 타겟으로 ARM NEON Intrinsic 을 이용한 구현
- Baseline 과 비교하여 20~30% 의 성능 개선

![fig:Auto](./assets/AUTODOG.jpeg){: width="90%" height="90%"}{: .align-center}
**AutoDog**
- Auto Driving System

![fig:ADAS](./assets/ADAS.png){: width="90%" height="90%"}{: .align-center}
**ADAS Program*험
- Developing ADAS Program

## Publications
1. **Hyeon-ki Lee** and Jae-Ho Nah, "H-ETC2: Design of a CPU-GPU Hybrid ETC2 Encoder", Computer Graphics Forum (Special Issue of Pacific Graphics 2023), 42(7), 2023, [(Link)](https://onlinelibrary.wiley.com/doi/10.1111/cgf.14969?af=R), [(Code)](https://github.com/gusrlLee/HETC2)
2. **Hyeon-ki Lee**, Hyeju Kim, Dong-Yun Kim, Woo-Chan Park and Jae-Ho Nah, "Considerations for the Acceleration Structure of Sound Propagation on Embedded Devices: Kd-trees versus Multi Bounding Volume Hierarchies", Multimedia Tools and Applications, 2024 (Under review), [(Demo)]()

## Education
- M.S., Computer Scienece	 | Sangmyung University, Seoul, Korea ( _2023.03 ~ 2024.08_ )			        		
- B.S., Electric Engineering | Sangmyung University, Seoul, Korea ( _2017.03 ~ 2023.02_ )

## Experience
- GPU Tech Labs @ Sanmyung University, Seoul, Korea ( _2022.04 ~ 2024.08_ )
- Creative Contents Labs @ Sanmyung University, Seoul, Korea ( _2021.04 ~ 2022.03_ )