# Benchmark Report for: sample.txt

Original File Size: 20000000 bytes

## Results

| Method     | Compression Time (ms) | Decompression Time (ms) | Compressed Size (bytes) |
|------------|-------------------------|---------------------------|-------------------------|
| Rust       | 260.0       | 110.0       | 5000022   |
| JavaScript | 2550.0         | 1360.0         | 36666666     |

## Raw Timings (seconds)

| Method     | Compress (Real) | Compress (User) | Compress (Sys) | Decompress (Real) | Decompress (User) | Decompress (Sys) |
|------------|-----------------|-----------------|----------------|-------------------|-------------------|------------------|
| Rust       | 0.26   | 0.22   | 0.03   | 0.11   | 0.08   | 0.03   |
| JavaScript | 2.55     | 1.20     | 1.40     | 1.36     | 0.80     | 0.61     |

