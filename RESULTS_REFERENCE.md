# Results: 117 GEMM / rocBLAS Microbenchmark

**Main goal:** Measure rocBLAS GEMM throughput  
**Tools:** Run the repository-local rocblas-bench built from ROCm rocBLAS source by scripts/build.sh (rocm_compile_rocblas_bench)

Reference results measured by the maintainer on the system shown in each section (generator TEMPLATE_00_138 · recorded 2026-11-12). Your own runs write `results/RESULTS_ACTUAL.md` in the same format.

> Smoke runs use deliberately small sizes. They check that the workload installs and runs end to end; their numbers are not performance results. Baseline and extended are.

<!-- profile:smoke -->
## smoke

- **System:** 1× AMD Instinct MI300X VF (196288 MB) · INTEL(R) XEON(R) PLATINUM 8568Y+ · Ubuntu 24.04.5 LTS · kernel 6.8.0-147-generic · driver 7.1.9.31600000
- **Run:** 2026-11-12T23:10:32Z · status **PASS** (exit 0)
- **Time (mm:ss):** setup 04:19 · benchmark 00:05 · whole run 04:40
- **Source:** run 117_20261112_231032
- **Command:** `bash run_benchmark.sh --smoke --dtype f32_r --M 64 --N 64 --K 64 --transposeA N --transposeB N --alpha 1 --beta 0 --lda 64 --ldb 64 --ldc 64 --batch-count 1 --warmup-iters 2 --num-iterations 2 --norm-check 1`

| # | Metric | Result |
|---|---|---|
| 1 | Achieved compute throughput, TFLOP/s (achieved_compute_tflops) | 0.04194304 |
| 2 | Kernel execution time (kernel_time_msec) | 0.0125 |
| 3 | Minimum operand traffic, GB/s (minimum_operand_traffic_gb_s) | 3.93216 |
| 4 | Relative L1 of checked columns (relative_l1_checked_columns) | 1.28778e-07 |
| 5 | CPU reference GFLOPS (cpu_gflops) | 40.3298 |
<!-- /profile:smoke -->
