# EKT333 Modern Operating System ![GitHub last commit](https://img.shields.io/github/last-commit/ehong-w/mos333-asg4-dump?style=for-the-badge)

In my own words,\
`Make your life easier in a blink of a Touch n Go scan!`

![forthebadge](https://forthebadge.com/images/badges/powered-by-electricity.svg)

---

### Assignment 4
![GitHub code size in bytes](https://img.shields.io/github/languages/code-size/ehong-w/mos333-asg4-dump)
![GitHub commit activity](https://img.shields.io/github/commit-activity/m/ehong-w/mos333-asg4-dump)
![GitHub all releases](https://img.shields.io/github/downloads/ehong-w/mos333-asg4-dump/total)

---

#### Question 1
Given memory partitions of 100K, 500K, 200K, 300K and 600K (in order).
- a. Draw these memory partitions in a block of 1700K memory.

```python
+------+--------------+--------+----------+--------------------+
| 100K |     500K     |  200K  |   300K   |        600K        |
+------+--------------+--------+----------+--------------------+
```

- b. Perform the following algorithm for the processes of 212K, 417K, 112K and 426K (in order). Assume the partitions are all empty initially.
- i. First-fit

```python
+------+--------------------+--------+----------+--------------+
| 100K | [212K] [112K] 500K |  200K  |   300K   | [417K] 600K  |
+------+--------------------+--------+----------+--------------+
426k is not allocated, waiting for the next turn.
```

- ii. Best-fit

```python
+------+------------+------------+--------------+-------------+
| 100K | [417K] 83K | [112K] 88K | [212K] 88K   | [426K] 174K |
+------+------------+------------+--------------+-------------+
All processes are allocated.
```

- iii. Worst-fit

```python
+------+------------+--------+----------+-------+-------------+
| 100K | [417K] 83K |  200K  |   300K   | [212K] [112K] 276K  |
+------+------------+--------+----------+-------+-------------+
426K is not allocated, waiting for the next turn.
```

- iv. Next-fit

```python
+------+-------------+--------+----------+-------------------+
| 100K | [212K] 288K |  200K  |   300K   | [417] [112K] 71K  |
+------+-------------+--------+----------+----- -------------+
426K is not allocated, waiting for the next turn.
```

- c. Among these 4 algorithms, evaluate which algorithm makes the most efficient of memory management? Justify you answer using your own words.

>Best-fit algorithm makes the most efficient of memory management. Among the four algorithms proposed, Best-fit is the only algorithm capable of allocating all the given processes to the smallest free partition that meets the requirement of the proesses. By searching for the smallest available free partition first, Best-fit algorithm results in the least external fragmentation compared to the other three algorithms.

---

#### Question 2
Figure 1 shows the example of physical to logical address translation process for segmentation.
Meanwhile, Figure 2 shows the hardware for address translation process. With reference to
Figure 1 and Figure 2, explain in your own words how the logical address of 0001 0010 1111
0000 is translated to physical address of 0010 0011 0001 0000 using the provided hardware
arrangement.

Figure 1: Example of physical to logical address translation

Figure 2: Hardware arrangement for address translation

> The 16-bit logical address is made up of 4-bit segment (MSB) followed by 12-bit offset. The 4-bit segment is... ...

```python
          Length              Base
  +-----------------+---------------------+
1 | 0111  1011 1110 | 0010 0000 0010 0000 |
  +-----------------+---------------------+
```

> After obtaining the length of the segment and... ...

```python
0010 1111 0000 B + 0010 0000 0010 0000 B = 0010 0010 0001 0000 B
```

---

#### Question 3
Consider the following statement. A 512KB block of memory is allocated using the buddy system.
```python
Request A: 100
Request B: 40
Request C: 190
Return A
Request D: 60
Return B
Return D
Return C
```

- a. Show the results of the sequence of requests and draw the Buddy System figure to reflect the situation.

```python
               +-------------------------------------------+
512KB block    |                   512KB                   |
               +-------------------------------------------+

               +-------------------------------------------+
Request A: 100 |  A=128KB  |      128KB      |    256KB    |
               +-------------------------------------------+

               +-------------------------------------------+
Request B: 40  |  A=128KB  | B=64KB |  64KB  |    256KB    |
               +-------------------------------------------+

               +-------------------------------------------+
Request B: 190 |  A=128KB  | B=64KB |  64KB  |   C=256KB   |
               +-------------------------------------------+

               +-------------------------------------------+
Return A       |   128KB   | B=64KB |  64KB  |   C=256KB   |
               +-------------------------------------------+

               +-------------------------------------------+
Request D: 60  |   128KB   | B=64KB | D=64KB |   C=256KB   |
               +-------------------------------------------+

               +-------------------------------------------+
Return B       |   128KB   |  64KB  | D=64KB |   C=256KB   |
               +-------------------------------------------+

               +-------------------------------------------+
Return D       |            256KB            |   C=256KB   |
               +-------------------------------------------+

```

- b. Find the internal fragmentation at each stage of allocation/de-allocation.

```python
+----------------------------------------+
| Statement |   Internal Fragmentation   |
| Request A | A: 128KB - 100KB = 28KB    |
| Request B | ...                        |
| ...       | ...                        |
| ...       | ...                        |
+----------------------------------------+
```

---

**@blaco**🐏: How's life? Did you check out my [GitHub](https://github.com/ehong-w/)? 😟\
**@blaco**🐏: Drop me an email for other source code!\
**@blaco**🐏: It's not free, but it worths just a price of a lunch. 🥗

<p>
  <img width="512" src="https://user-images.githubusercontent.com/68590570/113911631-c52ca900-980c-11eb-8946-19ce84f84c40.png">
</p>

## 🧸 **Leave me a message?**
- 🍺 [E-mail](mailto:ehong.w@gmail.com?subject=[GitHub]%20Problem%20Description)
- 🧺 [Linkedin](https://www.linkedin.com/in/ehong-w/)
- ⛄ [Whatsapp]()
