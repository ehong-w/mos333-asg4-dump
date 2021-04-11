# EKT333 Modern Operating System

In my own words,\
`Make your life easier in a blink of a Touch n Go scan!`

---

### Assignment 4

---

#### Question 1
Given memory partitions of 100K, 500K, 200K, 300K and 600K (in order).
- a. Draw these memory partitions in a block of 1700K memory.

```
+------+--------------+--------+----------+--------------------+
| 100K |     500K     |  200K  |   300K   |        600K        |
+------+--------------+--------+----------+--------------------+
```

- b. Perform the following algorithm for the processes of 212K, 417K, 112K and 426K (in order). Assume the partitions are all empty initially.
- i. First-fit

```
+------+--------------------+--------+----------+--------------+
| 100K | [212K] [112K] 500K |  200K  |   300K   | [417K] 600K  |
+------+--------------------+--------+----------+--------------+
426k is not allocated, waiting for the next turn.
```

- ii. Best-fit

```
+------+------------+------------+--------------+-------------+
| 100K | [417K] 83K | [112K] 88K | [212K] 88K   | [426K] 174K |
+------+------------+------------+--------------+-------------+
All processes are allocated.
```

- iii. Worst-fit

```
+------+------------+--------+----------+-------+-------------+
| 100K | [417K] 83K |  200K  |   300K   | [212K] [112K] 276K  |
+------+------------+--------+----------+-------+-------------+
426K is not allocated, waiting for the next turn.
```

- iv. Next-fit

```
+------+-------------+--------+----------+-------------------+
| 100K | [212K] 288K |  200K  |   300K   | [417] [112K] 71K  |
+------+-------------+--------+----------+----- -------------+
426K is not allocated, waiting for the next turn.
```

- c. Among these 4 algorithms, evaluate which algorithm makes the most efficient of memory management? Justify you answer using your own words.

>Best-fit algorithm makes the most efficient of memory management. Among the four algorithms proposed, Best-fit is the only algorithm capable of allocating all the given processes to the smallest free partition that meets the requirement of the proesses. By searching for the smallest available free partition first, Best-fit algorithm results in the least external fragmentation compared to the other three algorithms.

#### Question 2
Figure 1 shows the example of physical to logical address translation process for segmentation.
Meanwhile, Figure 2 shows the hardware for address translation process. With reference to
Figure 1 and Figure 2, explain in your own words how the logical address of 0001 0010 1111
0000 is translated to physical address of 0010 0011 0001 0000 using the provided hardware
arrangement.

Figure 1: Example of physical to logical address translation

Figure 2: Hardware arrangement for address translation

> The 16-bit logical address is made up of 4-bit segment (MSB) followed by 12-bit offset. The 4-bit segment is... ...

```
          Length              Base
  +-----------------+---------------------+
1 | 0111  1011 1110 | 0010 0000 0010 0000 |
  +-----------------+---------------------+
```

> After obtaining the length of the segment and... ...

```
0010 1111 0000 B + 0010 0000 0010 0000 B = 0010 0010 0001 0000 B
```
