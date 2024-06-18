# VBTC: GPU-Friendly Variable Block Size Texture Encoding  

### Takeaways
- In order to account for the natural variation in detail, we present an alternative fromat that allows variable bit-rate texture compression with minimal changes to texturing hardware.
  - Our proposed scheme uses one additional level of indirection to allow the variation of the block size across the same texture.
- One artifact of using compressed textures is the that fixed-rate compression introduces an inherent quality versus size tradeoff.
- The key contribution of this paper include:
  - A novel variable bit-rate texture compression method with efficient hardware decompression for curent GPUs.
  - A flexible dictionary-based blcok addressing scheme taking advantage of redundunt compressed blocks and maintaining low latency overheads.
  - A compression algorithm to perform variable bit-rate texture compression with a local image threashold.
- To remedy the afromentioned shortcomings, we propose a two level compressed texture layout to enable variable bit-rate texture compression. 
  - This approach is a dictionary-based scheme using metadata dictionary for:
    - Addressing and fetching a particular block of texels
    - Describing the method of compression for the given block
  - A user-specified error threshold 
- In this paper we have proposed a novel variable-rate texture compression format, which provides reductions in memory usage and memory bandwidth usage.