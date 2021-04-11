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
