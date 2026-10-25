# Multithreading in C

## Aim
To implement and demonstrate multithreading in C using POSIX threads (pthreads), including multi-core parallel execution and single-core time-sliced execution.

## Programs Included

### 1. Multi-Core Multithreading (`pa.c`)
This program creates four threads using the pthread library. Each thread prints a message indicating its execution.

**Sample Output:**
```text
Thread 1 executing (multi-core parallel)
Thread 2 executing (multi-core parallel)
Thread 3 executing (multi-core parallel)
Thread 4 executing (multi-core parallel)
```

### 2. Single-Core Multithreading (`pb.c`)
This program creates four threads and attempts to assign them to CPU core 0 using CPU affinity. The threads share the same core and are scheduled by the operating system.

**Sample Output:**
```text
Thread 1 time-sliced on single core
Thread 2 time-sliced on single core
Thread 3 time-sliced on single core
Thread 4 time-sliced on single core
```

*Note: The order of thread output may vary depending on the operating system scheduler.*

## Requirements
- GCC compiler
- Linux operating system or Ubuntu
- POSIX thread library (`pthread`)

## How to Compile and Run

### Multi-Core Program
```bash
gcc pa.c -o pa -pthread
./pa
```

### Single-Core Program
```bash
gcc pb.c -o pb -pthread
./pb
```

## Concepts Used
- Multithreading
- POSIX threads (pthreads)
- Thread creation using `pthread_create()`
- Thread synchronization using `pthread_join()`
- CPU affinity using `pthread_setaffinity_np()`
- Operating system thread scheduling

## Conclusion
Thus, multithreading was implemented in C using POSIX threads. The programs demonstrate multiple threads and illustrate how CPU affinity can be used to restrict threads to a single processor core.
# multithreading
