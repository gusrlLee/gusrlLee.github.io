# Multi-Bounding Volume Hierarchy (MBVH) for Sound Propagation

![fig:MBVH](./assets/MBVH.png)      
### **Multi-Bounding Volume Hierarchy (MBVH) for Sound Propagation**    
#### Summary
- 개요: Ray Tracing method 를 사용하는 Geometry-Acoustics (GA) 기반의 Sound Propagation 가속을 위한 Acceleration Structure 비교 실험
- 담당: Ray Tracing 의 Acceleration Structure 로 사용되는 Multi Bounding Volume Hierarchies (MBVH) 구현 및 실험

#### Details
- [Kim et al. 2023](https://www.mdpi.com/1424-8220/23/2/973) 을 기반으로 [Ernst and Greiner 2008](https://ieeexplore.ieee.org/document/4634618) 참고하여 MBVH를 적용
- ARM NEON Intrinsic 을 이용한 Ray Traversal & Intersection test (T & I) step 최적화 진행
- Baseline 과 비교하여 20~30% 의 성능 향상  


---
[Home](../README.md)