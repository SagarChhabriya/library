# GPU Architecture, VRAM, AI Compute — Structured Reference Notes

---

# 1. CPU vs GPU Memory Architecture

## 1.1 Functional Comparison

| Component | CPU | GPU |
|------------|------|------|
| Core Design | Few powerful cores | Thousands of parallel cores |
| Optimization Goal | Low latency | High throughput |
| Memory Type | DDR4 / DDR5 | GDDR6 / HBM |
| Primary Workload | OS, logic, applications | Graphics, AI, parallel compute |
| Parallelism Level | Low–moderate | Massive |

---

## 1.2 Memory Bandwidth Comparison

| Memory Type | Typical Bandwidth |
|-------------|-------------------|
| DDR4 System RAM | 25–50 GB/s |
| GDDR6 VRAM | 300–800+ GB/s |
| HBM (High Bandwidth Memory) | Multiple TB/s |

---

## 1.3 Why Separate VRAM Is Required

| Requirement | Explanation |
|-------------|-------------|
| Massive Parallel Access | Thousands of cores require simultaneous data feeds |
| Wide Memory Bus | 256-bit, 384-bit, 512-bit buses |
| Dedicated Controller | Independent scheduling & bandwidth allocation |
| No CPU Contention | Prevents memory bottleneck |
| High Throughput | Essential for AI & rendering workloads |

---

# 2. Cloud GPU Naming vs Actual Hardware

## 2.1 Cloud Instance Mapping

| Cloud Name | Underlying GPU |
|------------|----------------|
| A4X Max | NVIDIA GB300 Ultra |
| A4X | NVIDIA GB200 |
| A4 | NVIDIA B200 |
| A3 Ultra | NVIDIA H200 |
| A3 Mega | NVIDIA H100 |
| A3 High | NVIDIA H100 |
| A3 Edge | NVIDIA H100 |
| A2 Ultra | NVIDIA A100 80GB |
| A2 Standard | NVIDIA A100 40GB |
| G4 | NVIDIA RTX Pro 6000 |
| G2 | NVIDIA L4 |

---

# 3. GPU Comparison Metrics

## 3.1 Compute Metrics

| Metric | Meaning | Used For |
|--------|----------|----------|
| FP32 TFLOPS | 32-bit floating point performance | Graphics, scientific compute |
| FP16 TFLOPS | 16-bit floating point | AI training |
| BF16 | Brain Floating Point | Stable AI training |
| FP8 | 8-bit floating point | High-speed AI compute |
| FP64 | 64-bit floating point | HPC / scientific |
| Tensor TFLOPS | AI-specific acceleration | LLM training |

---

## 3.2 VRAM Capacity Evolution

| GPU | Typical VRAM |
|------|--------------|
| A100 | 40GB / 80GB |
| H100 | 80GB |
| H200 | 141GB |
| B200 | 192GB |
| GB200 | Higher (cluster-level design) |
| GB300 | Higher (rack-scale systems) |

---

## 3.3 Memory Bandwidth Evolution

| GPU Generation | Bandwidth |
|----------------|------------|
| A100 | ~2 TB/s |
| H100 | ~3.35 TB/s |
| H200 | ~4.8 TB/s |
| B200 | ~8+ TB/s |

---

## 3.4 Architecture Generations

| Architecture | GPU Models |
|--------------|------------|
| Ampere | A100 |
| Hopper | H100, H200 |
| Blackwell | B200, GB200, GB300 |

---

## 3.5 Interconnect Technology

| Technology | Purpose |
|------------|----------|
| NVLink | High-speed GPU-to-GPU communication |
| NVSwitch | Multi-GPU fabric interconnect |
| Transformer Engine | Optimized tensor operations for AI |

---

# 4. RTX vs A-Series vs H/B-Series

## 4.1 Product Segmentation

| Series | Target Market | Display Output | AI Optimization | ECC Memory |
|--------|---------------|---------------|------------------|------------|
| RTX | Gaming / Workstation | Yes | Moderate | Limited |
| A-Series | Data Center | No | High | Yes |
| H-Series | AI Data Center | No | Very High | Yes |
| B-Series | Advanced AI | No | Maximum | Yes |

---

## 4.2 Workload Suitability

| Use Case | Best Series |
|----------|-------------|
| Gaming | RTX |
| 3D Rendering | RTX |
| LLM Training | H-Series / B-Series |
| Scientific Compute | A-Series / H-Series |
| Inference at Scale | H-Series / B-Series |

---

# 5. Floating Point Precision Formats

## 5.1 Precision Comparison

| Format | Bit Size | Precision | AI Usage | Speed |
|--------|----------|------------|----------|-------|
| FP64 | 64-bit | Very High | HPC | Slow |
| FP32 | 32-bit | High | Graphics | Moderate |
| FP16 | 16-bit | Medium | AI Training | Fast |
| BF16 | 16-bit | Stable exponent | LLM Training | Fast |
| FP8 | 8-bit | Low | Modern AI | Very Fast |

---

## 5.2 Tradeoffs

| Benefit | Impact |
|----------|--------|
| Lower Precision | Faster compute |
| Lower Precision | Lower memory usage |
| Lower Precision | Slight accuracy tradeoff |

---

# 6. Learning Resources

## 6.1 Books

| Title | Authors | Focus |
|--------|----------|--------|
| Programming Massively Parallel Processors | Kirk & Hwu | CUDA & GPU architecture |
| Computer Architecture: A Quantitative Approach | Hennessy & Patterson | Deep hardware theory |

---

## 6.2 Online Resources

| Resource | Type | Focus |
|----------|------|--------|
| SemiAnalysis | Blog | AI hardware economics |
| Chips and Cheese | Blog | Microarchitecture |
| NVIDIA Developer Blog | Official Blog | GPU deep dives |
| GTC Talks | Conference | Architecture & AI |

---

# 7. Key Terms Index

| Category | Terms |
|----------|-------|
| Memory | VRAM, HBM, GDDR, Memory Bus, Bandwidth |
| Compute | TFLOPS, Tensor Cores, FP32, FP16, BF16, FP8 |
| Interconnect | NVLink, NVSwitch |
| Architectures | Ampere, Hopper, Blackwell |
| GPUs | A100, H100, H200, B200, GB200, GB300, RTX, L4 |
| Workloads | AI Training, Inference, LLM, Transformer |

---

# End of Structured Notes
