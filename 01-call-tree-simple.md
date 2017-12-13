# Profiler takes a sample every 1ms:

```
 1ms      2ms      3ms      4ms      5ms      6ms
-----    -----    -----    -----    -----    -----
  a        a        a        a        a        a   
  ↓        ↓        ↓        ↓        ↓        ↓   
  b        b        b        b        b        b   
  ↓        ↓        ↓        ↓        ↓        ↓   
  c        c        c        c        c        c   
  ↓        ↓        ↓        ↓        ↓        ↓   
doWork   doWork   doWork   doWork   doWork   doWork
```

# Call tree sums the times together into a single tree:

```
  a       (Running time: 6ms) (Self time: 0ms)    
  ↓
  b       (Running time: 6ms) (Self time: 0ms)
  ↓
  c       (Running time: 6ms) (Self time: 0ms)
  ↓     
doWork    (Running time: 6ms) (Self time: 6ms)
```
