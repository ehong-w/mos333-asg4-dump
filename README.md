# EKT333 Modern Operating System

In my own words,\
`Make your life easier in a blink of a Touch n Go scan!`

---

### Assignment 4

---

#### Question 1
Given memory partitions of 100K, 500K, 200K, 300K and 600K (in order).
- a. Draw these memory partitions in a block of 1700K memory.

100K|500K|200K|300K|600K]
----|----|----|----|-----

- b. Perform the following algorithm for the processes of 212K, 417K, 112K and 426K (in order). Assume the partitions are all empty initially.
- i. First-fit

100K|[212K] [112K] (176K)|200K|300K|[417K] (183K)
----|--------------------|----|----|-------------


- ii. Best-fit

100K|[417K] (83K)|[112K] (88K)|[212K] (88K)|[426K] (174K)
----|------------|------------|------------|-------------
