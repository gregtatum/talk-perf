# Profiler takes a sample every 1ms:

```
1ms   2ms   3ms
---   ---   ---
 a     a     a
 ↓     ↓     ↓
 b     b     b
 ↓     ↓     ↓
 c     c     h
 ↓     ↓     ↓
 d     f     f
 ↓     ↓     ↓   
 e     g     g
```

# Call tree sums the times together into a single tree:

```
           a  3ms
           ↓
           b  3ms
         ↙   ↘
       c       h  1ms
     ↙   ↘       ↘
   d       f      f  1ms
   ↓       ↓      ↓
   e       g      g  1ms
```
