# 🚀 Agam Official Showcase Examples

A curated collection of production-grade examples demonstrating the expressiveness, performance, and ergonomics of **Agam** — the Hardware-Accelerated Systems & AI Programming Language.

---

## 🎭 Dual-Syntax Profiles: `@lang.base` vs. `@lang.advance`

Agam allows developers to write in two interchangeable syntax profiles with **100% identical SSA execution throughput**:
- **`@lang.base`**: Clean, readable, Python-style syntax (indentation-based).
- **`@lang.advance`**: Explicit, typed, Rust/C++ style syntax (braced, algebraic effects, `@gpu`).

---

## 📂 Example Index

### `01_basics/` — Language Fundamentals & Dual Profiles
- [`01_hello_world_base.agam`](01_basics/01_hello_world_base.agam) — Hello World in Pythonic `@lang.base` profile.
- [`01_hello_world_advance.agam`](01_basics/01_hello_world_advance.agam) — Hello World in typed `@lang.advance` profile.
- [`02_quicksort_base.agam`](01_basics/02_quicksort_base.agam) — In-place Quicksort in `@lang.base` profile.
- [`02_quicksort_advance.agam`](01_basics/02_quicksort_advance.agam) — In-place Quicksort in `@lang.advance` profile.
- [`03_prime_sieve_base.agam`](01_basics/03_prime_sieve_base.agam) — Sieve of Eratosthenes in `@lang.base` profile.
- [`03_prime_sieve_advance.agam`](01_basics/03_prime_sieve_advance.agam) — Sieve of Eratosthenes in `@lang.advance` profile.
- [`fibonacci_base.agam`](01_basics/fibonacci_base.agam) — Recursive Fibonacci in `@lang.base`.
- [`fibonacci_advance.agam`](01_basics/fibonacci_advance.agam) — Recursive Fibonacci in `@lang.advance`.
- [`03_pattern_matching.agm`](01_basics/03_pattern_matching.agm) — Sum types (enums) and Maranget-verified pattern matching.
- [`04_effects_and_handlers.agm`](01_basics/04_effects_and_handlers.agm) — Algebraic effects (`perform` / `handle`), non-local control, and continuations.

### `02_ai_and_tensors/` — AI-Native Compute
- [`01_shape_aware_tensor.agm`](02_ai_and_tensors/01_shape_aware_tensor.agm) — Multidimensional tensors with compile-time shape verification.
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
# 1. Run immediately via In-Memory Cranelift JIT
agamc run examples/01_basics/fibonacci_base.agam

# 2. Benchmark native execution time directly
agamc bench examples/01_basics/02_quicksort_advance.agam

# 3. Compile to optimized standalone native binary via LLVM
agamc build -O 3 examples/01_basics/fibonacci_advance.agam -o fib_demo
./fib_demo
```

---

## 📜 License

Dual-licensed under [MIT](LICENSE-MIT) and [Apache 2.0](LICENSE-APACHE).
