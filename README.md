# 🚀 Agam Official Showcase Examples

A curated collection of production-grade examples demonstrating the expressiveness, performance, and ergonomics of **Agam** — the Hardware-Accelerated Systems & AI Programming Language.

---

## 📂 Example Index

### `01_basics/` — Language Fundamentals
- [`01_hello_world.agm`](01_basics/01_hello_world.agm) — Basic syntax, string interpolation, and standard I/O.
- [`02_fibonacci.agm`](01_basics/02_fibonacci.agm) — Recursive vs. iterative algorithmic control flow.
- [`03_pattern_matching.agm`](01_basics/03_pattern_matching.agm) — Sum types (enums) and Maranget-verified pattern matching.
- [`04_effects_and_handlers.agm`](01_basics/04_effects_and_handlers.agm) — Algebraic effects (`perform` / `handle`), non-local control, and continuations.

### `02_ai_and_tensors/` — AI-Native Compute
- [`01_shape_aware_tensor.agm`](02_ai_and_tensors/01_shape_aware_tensor.agm) — High-performance multidimensional tensors with shape checking.
- [`02_autodiff_sgd.agm`](02_ai_and_tensors/02_autodiff_sgd.agm) — Reverse-mode automatic differentiation (Baur-Strassen) and SGD training.
- [`03_bayesian_mcmc.agm`](02_ai_and_tensors/03_bayesian_mcmc.agm) — Probabilistic programming, `sample`/`observe`, and Metropolis-Hastings MCMC.

### `03_hardware_acceleration/` — GPU & Tile Computing
- [`01_gpu_warp_reduction.agm`](03_hardware_acceleration/01_gpu_warp_reduction.agm) — NVPTX 5-step butterfly warp shuffle reduction across 32 threads.
- [`02_tile_matrix_multiplication.agm`](03_hardware_acceleration/02_tile_matrix_multiplication.agm) — Tensor Core `Tile<f32, 16>` matrix multiply-accumulate via SPIR-V.

### `04_systems_and_web/` — Systems Engineering & Security
- [`01_async_http_server.agm`](04_systems_and_web/01_async_http_server.agm) — Asynchronous HTTP server and JSON serializer.
- [`02_ebpf_packet_filter.agm`](04_systems_and_web/02_ebpf_packet_filter.agm) — In-kernel eBPF network packet inspection.
- [`03_post_quantum_crypto.agm`](04_systems_and_web/03_post_quantum_crypto.agm) — NIST FIPS 203 ML-KEM-768 post-quantum key exchange.

### `05_declarative_ui/` — UI & Graphics
- [`01_bento_dashboard.agm`](05_declarative_ui/01_bento_dashboard.agm) — Reactive Bento Grid UI rendered to 120 FPS GPU display lists.

---

## 🏃 Running Examples

To compile and run any example with the Agam toolchain:

```bash
# Run immediately via JIT
agamc run examples/01_basics/01_hello_world.agm

# Compile to optimized native binary
agamc build -O 3 examples/02_ai_and_tensors/01_shape_aware_tensor.agm -o tensor_demo
./tensor_demo
```
