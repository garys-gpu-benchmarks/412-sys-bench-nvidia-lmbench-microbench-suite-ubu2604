# Results: 412 lmbench Microbench Suite

**Main goal:** Measure a fixed lmbench microbench subset  
**Tools:** Run lmbench lat_syscall (null, read), lat_ctx, lat_mem_rd 16 128, bw_mem 512m rd, and bw_pipe

Reference results measured by the maintainer on the system shown in each section (generator TEMPLATE_00_146 · recorded 2026-11-18). Your own runs write `results/RESULTS_ACTUAL.md` in the same format.

> Smoke runs use deliberately small sizes. They check that the workload installs and runs end to end; their numbers are not performance results. Baseline and extended are.

<!-- profile:smoke -->
## smoke

- **System:** 1× NVIDIA H100 NVL (95830 MiB) · AMD EPYC 9374F 32-Core Processor · Ubuntu 26.04.1 LTS · kernel 6.8.0-138-generic · driver 595.112.07
- **Run:** 2026-11-18T10:50:39Z · status **PASS** (exit 0)
- **Time (mm:ss):** setup 00:33 · benchmark 00:42 · whole run 01:20
- **Source:** run 412_20261118_105039
- **Command:** `bash run_benchmark.sh --smoke --warmup-duration-us 1000 --repetitions 1`

| # | Metric | Result |
|---|---|---|
| 1 | Null syscall latency, us (lat_syscall_null_us) | 0.3112 |
| 2 | Context-switch latency, us (context_switch_latency_us) | 1.58 |
| 3 | 16 MB stride-128 sequential-read latency, cache- and prefetch-assisted, ns (lat_mem_rd_16mb_stride128_ns) | 4.621 |
| 4 | Single-thread memory read bandwidth, MB/s (bw_mem_mb_s) | 45988.6 |
| 5 | Inter-process pipe bandwidth, MB/s (bw_pipe_mb_s) | 3552.31 |
<!-- /profile:smoke -->
