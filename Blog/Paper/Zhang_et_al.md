# Area ReSTIR: Resampling for Real-Time Defocus and Antialiasing

### Abstract 
Recent advancements in spatiotemporal reservoir resampling (ReSTIR) lever- age sample reuse from neighbors to efficiently evaluate the path integral. Like rasterization, ReSTIR methods implicitly assume a pinhole camera and evaluate the light arriving at a pixel through a single predetermined subpixel location at a time (e.g., the pixel center). This prevents efficient path reuse in and near pixels with high-frequency details.
We introduce Area ReSTIR, extending ReSTIR reservoirs to also integrate each pixel’s 4D ray space, including 2D areas on the film and lens. We design novel subpixel-tracking temporal reuse and shift mappings that max- imize resampling quality in such regions. This robustifies ReSTIR against high-frequency content, letting us importance sample subpixel and lens coordinates and efficiently render antialiasing and depth of field.

### Takeaways 
- This has been applied to various rendering problems: many-light sampling, diffuse global illumination, and more general light paths including volumetric scattering. 
- But these algorithms shade only at pixel centers, essentially using a delta function as the pixel filter; this introduces **aliasing**.
- Thus, high-frequency detail often causes significant quality degradation. 
- To solve this problem, we introduce *Area ReSTIR*, which expands ResTIR to sample pixel footprints.
- our method also integrates over camera aperture, resampling primary rays in a 4D ray space.
- we reuse to solve the higher-dimensional *measurement eqaution*, which integrates over the pixel filter and camera parameters, enhancing analysis of overlaps among adjacent pixel domains or reservoirs. 
- We initially aimed to reduce aliasing with ReSTIR, but discovered our method also improves reuse on areas. 
- Randomizing **u**_j mutates ReSTIR's target distribution, potentially invalidating temporal reuse where *f* changes quickly due to high-frequency normal maps, glinty materials, hair, or foliage. **Camera or object motion can degrade reuse quality in these regions even if using fixed $u_j$ at pixel centers, but the issue are magnified when rendering with camera jittering for antialiasing**
- We let ReSTIR also importance importance sample subpixel locations. 
- We outline two options for identifying previous frame samples: a **fast option** that picks from samples overlapping the backprojected pixel, and a more expensive and robust option that ensures all nearby samples can contribute, by shifting them onto the pixel's support. 


---
[Blog Home](../Blog.md)