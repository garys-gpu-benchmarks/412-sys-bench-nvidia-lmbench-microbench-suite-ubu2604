# Results: 412 lmbench Microbench Suite

**Main goal:** Measure a fixed lmbench microbench subset  
**Tools:** Run lmbench lat_syscall (null, read), lat_ctx, lat_mem_rd 16 128, bw_mem 512m rd, and bw_pipe

Reference results measured by the maintainer on the system shown in each section (generator TEMPLATE_00_149 · recorded 2026-11-19). Your own runs write `results/RESULTS_ACTUAL.md` in the same format.

> Smoke runs use deliberately small sizes. They check that the workload installs and runs end to end; their numbers are not performance results. Baseline and extended are.

<!-- profile:smoke -->
## smoke

- **System:** 1× NVIDIA H100 NVL (95830 MiB) · Intel(R) Xeon(R) Platinum 8452Y · Ubuntu 26.04.1 LTS · kernel 6.8.0-138-generic · driver 595.112.07
- **Run:** 2026-11-19T21:37:59Z · status **PASS** (exit 0)
- **Time (mm:ss):** setup 00:49 · benchmark 00:43 · whole run 01:38
- **Source:** run 412_20261119_213759
- **Command:** `bash run_benchmark.sh --smoke --warmup-duration-us 1000 --repetitions 1`

| # | Metric | Result |
|---|---|---|
| 1 | Null syscall latency, us (lat_syscall_null_us) | 0.2331 |
| 2 | Context-switch latency, us (context_switch_latency_us) | 7.6 |
| 3 | 16 MB stride-128 sequential-read latency, cache- and prefetch-assisted, ns (lat_mem_rd_16mb_stride128_ns) | 9.088 |
| 4 | Single-thread memory read bandwidth, MB/s (bw_mem_mb_s) | 11625.36 |
| 5 | Inter-process pipe bandwidth, MB/s (bw_pipe_mb_s) | 2690.74 |
<!-- /profile:smoke -->
