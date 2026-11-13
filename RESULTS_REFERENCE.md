# Results: 412 lmbench Microbench Suite

**Main goal:** Measure a fixed lmbench microbench subset  
**Tools:** Run lmbench lat_syscall (null, read), lat_ctx, lat_mem_rd 16 128, bw_mem 512m rd, and bw_pipe

Reference results measured by the maintainer on the system shown in each section (generator TEMPLATE_00_139 · recorded 2026-11-13). Your own runs write `results/RESULTS_ACTUAL.md` in the same format.

> Smoke runs use deliberately small sizes. They check that the workload installs and runs end to end; their numbers are not performance results. Baseline and extended are.

<!-- profile:smoke -->
## smoke

- **System:** 1× NVIDIA H100 PCIe (81559 MiB) · Intel(R) Xeon(R) Platinum 8352Y CPU @ 2.20GHz · Ubuntu 26.04.1 LTS · kernel 6.8.0-138-generic · driver 595.91.07
- **Run:** 2026-11-13T14:05:26Z · status **PASS** (exit 0)
- **Time (mm:ss):** setup 00:46 · benchmark 00:46 · whole run 01:44
- **Source:** run 412_20261113_140526
- **Command:** `bash run_benchmark.sh --smoke --warmup-duration-us 1000 --repetitions 1`

| # | Metric | Result |
|---|---|---|
| 1 | Null syscall latency, us (lat_syscall_null_us) | 0.2601 |
| 2 | Context-switch latency, us (context_switch_latency_us) | 3.7 |
| 3 | 16 MB stride-128 sequential-read latency, cache- and prefetch-assisted, ns (lat_mem_rd_16mb_stride128_ns) | 5.886 |
| 4 | Single-thread memory read bandwidth, MB/s (bw_mem_mb_s) | 12121.17 |
| 5 | Inter-process pipe bandwidth, MB/s (bw_pipe_mb_s) | 2392.57 |
<!-- /profile:smoke -->
