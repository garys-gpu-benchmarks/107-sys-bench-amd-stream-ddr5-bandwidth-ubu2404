# Results: 107 STREAM - CPU (Copy/Scale/Add/Triad)

**Main goal:** Measure sustained CPU STREAM bandwidth  
**Tools:** Compile src/stream.c with gcc -O3 -fopenmp and run build/stream

Reference results measured by the maintainer on the system shown in each section (generator TEMPLATE_00_145 · recorded 2026-11-17). Your own runs write `results/RESULTS_ACTUAL.md` in the same format.

> Smoke runs use deliberately small sizes. They check that the workload installs and runs end to end; their numbers are not performance results. Baseline and extended are.

<!-- profile:smoke -->
## smoke

- **System:** 1× AMD Instinct MI300X VF (196288 MB) · INTEL(R) XEON(R) PLATINUM 8568Y+ · Ubuntu 24.04.5 LTS · kernel 6.8.0-147-generic · driver 7.1.9.31600000
- **Run:** 2026-11-17T11:02:50Z · status **PASS** (exit 0)
- **Time (mm:ss):** setup 00:07 · benchmark 00:01 · whole run 00:18
- **Source:** run 107_20261117_110250
- **Command:** `bash run_benchmark.sh --smoke --numa-node 0 --num-threads 4 --thread-affinity core --array-size 10000000 --num-iterations 2`

| # | Metric | Result |
|---|---|---|
| 1 | Best Copy bandwidth, GB/s (copy_bandwidth_gb_s) | 98.0208 |
| 2 | Best Scale bandwidth, GB/s (scale_bandwidth_gb_s) | 76.6066 |
| 3 | Best Add bandwidth, GB/s (add_bandwidth_gb_s) | 113.161 |
| 4 | Best Triad bandwidth, GB/s (triad_bandwidth_gb_s) | 118.8072 |
<!-- /profile:smoke -->
