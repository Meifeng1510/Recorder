# Recorder

## Benchmark

---------------------------------------
CPU: AMD Ryzen 5 2600
GPU: GTX 1050 Ti

---------------------------------------

Total Instance Tracked: 1153
Dynamic (moving) Instance: 1027

---------------------------------------
Takes 7ms on average per frame

Total Frame: 543
Video Duration: 10.43s
Encoding Time: 12.8s

Original size: 16MB (30KB per frame)
Compressed size: 4MB (7.3KB per frame)

Compression Time: 9.83s (1.627MB/s)
Compression Ratio: 75%

-------------------------------------------------------------------------------------------------------------------------------------------

DataStore limit is 4MB per key with 60 requests per minute each server (unaccounted for players).
Assuming memory consumption stays the same, you can easily record up to 548 fps with 1027 moving parts
while being able to autosave to datastore.

It takes 7ms to track 1027 moving parts, which limit the fps to around ~142.8
This is highly optimized, and will be able to handle high amount of dynamic parts.
Assuming same ratio, you can record at 20fps while having 7335 dynamic parts.
This benchmark of course depends on the cpu specification, so if it was done from server,
the result will be significantly better.

-------------------------------------------------------------------------------------------------------------------------------------------
