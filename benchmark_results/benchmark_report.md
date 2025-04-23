# Benchmark Report for: sample.txt

Original File Size: 20000000 bytes

## Results

| Method     | Compression Time (ms) | Decompression Time (ms) | Compressed Size (bytes) |
|------------|-------------------------|---------------------------|-------------------------|
| Rust       | 290.0       | 120.0       | 5000022   |
| JavaScript | 2430.0         | 1360.0         | 36666666     |

## Raw Timings (seconds)

| Method     | Compress (Real) | Compress (User) | Compress (Sys) | Decompress (Real) | Decompress (User) | Decompress (Sys) |
|------------|-----------------|-----------------|----------------|-------------------|-------------------|------------------|
| Rust       | 0.29   | 0.25   | 0.03   | 0.12   | 0.07   | 0.04   |
| JavaScript | 2.43     | 1.24     | 1.36     | 1.36     | 0.78     | 0.63     |

