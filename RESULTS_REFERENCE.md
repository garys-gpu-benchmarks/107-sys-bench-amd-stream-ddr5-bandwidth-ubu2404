# Results: 107 STREAM - CPU (Copy/Scale/Add/Triad)

**Main goal:** Measure sustained CPU STREAM bandwidth  
**Tools:** Compile src/stream.c with gcc -O3 -fopenmp and run build/stream

Reference results from the validation run on the system shown in each section (recorded 2026-11-22). Your own runs write `results/RESULTS_ACTUAL.md` in the same format.

> Smoke runs use deliberately small sizes. They check that the workload installs and runs end to end; their numbers are not performance results. Baseline and extended are.

<!-- profile:smoke -->
## smoke

- **System:** 1× AMD Instinct MI300X VF (196288 MB) · INTEL(R) XEON(R) PLATINUM 8568Y+ · Ubuntu 24.04.5 LTS · kernel 6.8.0-149-generic · driver 7.1.9.31600000
- **Run:** 2026-11-22T14:16:59Z · status **PASS** (exit 0)
- **Time (mm:ss):** setup 00:36 · benchmark 00:05 · whole run 00:51
- **Source:** run 107_20261122_141659
- **Command:** `bash run_benchmark.sh --smoke --numa-node 0 --num-threads 4 --thread-affinity core --array-size 10000000 --num-iterations 368`

| # | Metric | Result |
|---|---|---|
| 1 | Best Copy bandwidth, GB/s (copy_bandwidth_gb_s) | 100.9045 |
| 2 | Best Scale bandwidth, GB/s (scale_bandwidth_gb_s) | 80.0712 |
| 3 | Best Add bandwidth, GB/s (add_bandwidth_gb_s) | 115.077 |
| 4 | Best Triad bandwidth, GB/s (triad_bandwidth_gb_s) | 119.8487 |
<!-- /profile:smoke -->
