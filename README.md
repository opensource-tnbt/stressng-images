This repository Stores the OSv-based images of 'pre-configured' stress-ng. Initially 5 'High-Stress' images are created to support Noisy-Neighbor test-cases - specifically for OPNFV-VSPERF.

The description of 5-types (Named as A, B, C, D and E) - in the increasing order of stress - are as follows:

Type-A: CPU, L3-Cache, HDD, VM, MemCpy, Memory-Bandwidth, Memory-Rate, UDP.

stress-ng --aggressive --maximize --cpu 0 --cpu-load 100 --cache 0 --cache-level 3 --stream 0 --stream-l3-size 55M --hdd 0 --vm 0 --vm-bytes 128M --vm-rw 0 --vm-rw-bytes 128M --udp 10 --udp-port 10001 --udp-flood 10 --memrate 0 --memrate-bytes 128M --memrate-rd-mbs 10000M --memrate-wr-mbs 5000M --memcpy 0


Type-B: CPU, L3-Cache, HDD, VM, Memcpy, Memory-Bandwidth, Memory-Rate, UDP, Operations- Matrix Multiplication, Quick-Sort and Binary Search, Vectormath and other searches - tree, hashtable and linear.

stress-ng --aggressive --maximize --cpu 0 --cpu-load 100 --cache 0 --cache-level 3 --stream 0 --stream-l3-size 55M --hdd 0 --vm 0 --vm-bytes 128M --vm-rw 0 --vm-rw-bytes 128M --udp 10 --udp-port 10001 --udp-flood 10 --memrate 0 --memrate-bytes 128M --memrate-rd-mbs 10000M --memrate-wr-mbs 5000M --memcpy 0 --matrix 0 --matrix-size 1000 --qsort 0 --qsort-size 1000000 --bsearch 0 --lsearch 0--lsearch-size 10000 --tsearch 0 --tsearch-size 10000 --hsearch 0 --hsearch-size 10000 --vecmath 0


Type-C: CPU, L3-Cache, HDD, VM, Memory-Bandwidth, Memory-Rate, UDP, memcpy, Operations- {Matrix Multiplication, Quick-Sort and Binary Search, Vectormath and other searches - tree, hashtable and linear}, I/O Operations - {Synchronous and Asynchronous IOs, FIFO, Socket, Socket-Pair, and Read-Write},

stress-ng --aggressive --maximize --cpu 0 --cpu-load 100 --cache 0 --cache-level 3 --stream 0 --stream-l3-size 55M --hdd 0 --vm 0 --vm-bytes 128M --vm-rw 0 --vm-rw-bytes 128M --udp 10 --udp-port 10001 --udp-flood 10 --memrate 0 --memrate-bytes 128M --memrate-rd-mbs 10000M --memrate-wr-mbs 5000M --memcpy 0 --matrix 0 --matrix-size 100 --qsort 0 --qsort-size 1000000 --bsearch 0 --lsearch 0--lsearch-size 10000 --tsearch 0 --tsearch-size 10000 --hsearch 0 --hsearch-size 10000 --vecmath 0 --io 0 --aio 0 --aio-requests 4096 --seek 0 --sock 0 --sock-port 10001 --sock-type stream --sockpair 0


Type-D: CPU, L3-Cache, HDD, VM, Memory-Bandwidth, Memory-Rate, UDP, memcpy Operations- {Matrix Multiplication, Quick-Sort and Binary Search, Vectormath and other searches - tree, hashtable and linear}, I/O Operations - {Synchronous and Asynchronous IOs, FIFO, Socket, Socket-Pair, and Read-Write}, System Calls - {Pthread, Falloc, Malloc, Calloc, MMAP, Poll, Dup, and Exec}

stress-ng --aggressive --maximize --cpu 0 --cpu-load 100 --cache 0 --cache-level 3 --stream 0 --stream-l3-size 55M --hdd 0 --vm 0 --vm-bytes 128M --vm-rw 0 --vm-rw-bytes 128M --udp 10 --udp-port 10001 --udp-flood 10 --memrate 0 --memrate-bytes 128M --memrate-rd-mbs 10000M --memrate-wr-mbs 5000M --memcpy 0 --matrix 0 --matrix-size 100 --qsort 0 --qsort-size 1000000 --bsearch 0 --lsearch 0--lsearch-size 10000 --tsearch 0 --tsearch-size 10000 --hsearch 0 --hsearch-size 10000 --vecmath 0 --io 0 --aio 0 --aio-requests 4096 --seek 0 --sock 0 --sock-port 10001 --sock-type stream --sockpair 0 --bigheap 0 --malloc 0 --malloc-bytes 32M --malloc-max 1000 --mmap 0 --mmap-bytes 80% --fallocate 0 --dup 0 --poll 0 --pthread 0 --pthread-max 1000 --exec 0

Type-E: All

stress-ng --all 0 --aggressive --maximize
