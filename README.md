# Recorder

## Benchmark

CPU: AMD Ryzen 5 2600

GPU: GTX 1050 Ti

### Instance Tracking
---------------------------------------

Total Instance Tracked: 1153

Dynamic (moving) Instance: 1027

Takes 7ms on average to track each frame

### Video Info
---------------------------------------

Total Frame: 543
 
Video Duration: 10.43s

Encoding Time: 12.8s

### Compression
----

Original size: 16MB (30KB per frame)

Compressed size: 4MB (7.3KB per frame)

----

Compression Time: 9.83s (1.627MB/s)

Compression Ratio: 75%

## Description

The system imposes a minimum of 20Hz on the resumption cycle to prevent script timeout and ensure
it doesn't get too laggy. Processing time can be modified to suit your needs.

DataStore limit is 4MB per key with 60 requests per minute for each server (unaccounted-for players).
Assuming memory consumption stays the same, you can easily record up to 60 fps with 9378 moving parts
while being able to autosave to DataStore.

It takes 7ms to track 1027 moving parts, which imposes a limit of 142.8 fps (not accounting for other time spent).
This shows how highly optimized the code is, and will be able to handle a high amount of dynamic parts.
Assuming the same ratio, you can record at 20fps while having 7335 dynamic parts.
This benchmark of course depends on the CPU specification, so if it was done from the server,
the result would be significantly better.

-------------------------------------------------------------------------------------------------------------------------------------------
