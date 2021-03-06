# 第6章	图



#### 1. 选择题

**（1）**在一个为无向图中，所有顶点的度数之和等于图的边数的（C）倍。

​	A.	1/2				B.	1				C.	2				D.	4

> 图中的一条边会产生两个度。

**（2）**在一个有向图中，所有顶点的入度之和等于所有顶点的出度之和的（B）倍。

​	A.	1/2				B.	1				C.	2				D.	4

> 有向图中的一条弧会产生一个入度和一个出度。

**（3）**具有n个顶点的有向图最多有（B）条边。

​	A.	n					B.	n(n-1)				C.	n(n+1)				D.	$n^2$

> 很简单嘛，想象一下每个顶点都可以射出去n-1条弧。

**（4）**n 个顶点的连通图用邻接距阵表示时,该距阵至少有（B）个非零元素。

​	A.	n					B.	2(n-1)				C.	n/2					D.	$n^2$

> n个顶点的连通图至少需要n-1条边，此邻接矩阵为对称矩阵，那么有2(n-1)个非零元素。

**（5）**G 是一个非连通无向图,共有 28 条边,则该图至少有（C）个顶点。

​	A.	7					B.	8						C.	9						D.	10

> 题目中说至少，那么在有限的顶点中拥有尽可能多的边；我们先试一试8吧，因为是非连通图，那么我们拿出7个顶点来试下，7(7 - 1)/2 = 21边；那么我们在试一下9咯，9(9 - 1)/2 = 36条边；所以我们可以取答案C。

**（6）**若从无向图的任意 一 个顶点出发进行 一 次深度优先搜索可以访问图中所有的顶点,则该图一定是（B）图。

​	A.	非连通				B.	连通				C.	强连通				D.	有向

> 这题。。。

**（7）**下面（A）适合构造一个稠密图G的最小生成树。

​	A.	Prim算法			B.	Kruskal算法				C.	Floyd算法				D.	Dijkstra算法

> 稠密图意思是很多边，Prim算法的时间复杂度跟顶点有关，所以选A。

**（8）**用邻接表表示图进行广度优先遍历时,通常可借助（B）来实现算法。

​	A.	栈						B.	队列							C.	树								D.	图

**（9）**用邻接表表示图进行深度优先遍历时,通常可借助（A）来实现算法。

​	A.	栈						B.	队列							C.	树								D.	图

**（10）**图的深度优先遍历类似于二叉树的（A）。

​	A.	先序遍历			B.	中序遍历			C.	后序遍历				D.	层次遍历

**（11）**图的广度优先遍历类似于二叉树的（D）。

​	A.	先序遍历			B.	中序遍历			C.	后序遍历				D.	层次遍历

**（12）**图的 BFS 生成树的树高比 DFS 生成树的树高（C）。

​	A.	小				B.	大				C.	小或相等				D.	大或相等

> 这道题怎么做呢？图可以是一个结点嘛，至少可以相等的咯；还有想象一下，广度优先遍历一下子将多个孩子压入栈中，可以理解为很多分支，都在同一层；而深度优先遍历则一个一个往下找，找不到再回去，那么可以想象出它应该大多数下都比较高咯。

**（13）**已知图的邻接矩阵如图6.30所示,则从顶点v。出发按深度优先遍历的结果是（C）。

![图 6.30](https://github.com/katoluo/DataStructures/raw/master/chapter_06/images/%E5%9B%BE6-30.png)

**（14）**已知图的邻接表如图6.31 所示,则从项点v。出发按广度优先遍历的结果是（D），按深度优先遍历的结果是（D）。

![图 6.31](https://github.com/katoluo/DataStructures/raw/master/chapter_06/images/%E5%9B%BE6-31.png)

**（15）**下面的（B）方法可以判断出一个有向图是否有环。

​	A.	求最小生成树		B.	拓扑排序		C.	求最短路径		D.	求关键路径 

#### 2. 应用题

**（1）**已知图6.32所示的有向图, 请给出：

![图 6.32](https://github.com/katoluo/DataStructures/raw/master/chapter_06/images/%E5%9B%BE6-32%E5%92%8C33.png)

- 每个顶点的入度和出度；

| 顶点 | 出度数 | 入度数 |
| :--: | :----: | :----: |
|  1   |   0    |   3    |
|  2   |   2    |   2    |
|  3   |   2    |   1    |
|  4   |   3    |   1    |
|  5   |   1    |   2    |
|  6   |   3    |   2    |

- 邻接矩阵；
- 邻接表；
- 逆邻接表。

> 我做对了。

（2）已知如图6.33所示的无向网, 请给出：

- 邻接矩阵
- 邻接表
- 最小生成树

> 想象一下。

（3）已知图的邻接矩阵如图 6.34 所示。 试分别画出自顶点 1 出发进行遍历所得的深度优先生成树和广度优先生成树。

![图 6-34和35](https://github.com/katoluo/DataStructures/raw/master/chapter_06/images/%E5%9B%BE6-34%E5%92%8C35.png)

> 我又做对了。

（4）有向网如图 6.35 所示,试用迪杰斯特拉算法求出从顶点a到其他各顶点间的最短路径,完成表 6.9 。

|          |     i=1     |      i=2      |       i=3       |       i=4       |        i=5        |       i=6       |
| :------: | :---------: | :-----------: | :-------------: | :-------------: | :---------------: | :-------------: |
|    b     | $15\\(a,b)$ |  $15\\(a,b)$  |   $15\\(a,b)$   |   $15\\(a,b)$   |    $15\\(a,b)$    |   $15\\(a,b)$   |
|    c     | $2\\(a,c)$  |       /       |        /        |        /        |         /         |        /        |
|    d     | $12\\(a,d)$ |  $12\\(a,d)$  | $11\\(a,c,f,d)$ | $11\\(a,c,f,d)$ |         /         |        /        |
|    e     |      -      | $10\\(a,c,e)$ |  $10\\(a,c,e)$  |        /        |         /         |        /        |
|    f     |      -      | $6\\(a,c,f)$  |        /        |        /        |         /         |        /        |
|    g     |      -      |       -       | $16\\(a,c,f,g)$ | $16\\(a,c,f,g)$ | $14\\(a,c,f,d,g)$ |        /        |
| S 终点集 |    {a,c}    |    {a,c,f}    |    {a,c,f,e}    |   {a,c,f,e,d}   |   {a,c,f,e,d,g}   | {a,c,f,e,d,g,b} |

（5）试对图 6.36 所示的 AOE - 网：

![图 6-36](https://github.com/katoluo/DataStructures/raw/master/chapter_06/images/%E5%9B%BE6-36.png)

- 求这个工程最早可能在什么时间结束；

> 43

- 求每个活动的最早开始时间和最迟开始时间；

|   活动    | 最早 | 最迟 |
| :-------: | :--: | :--: |
| $A_{1,2}$ |  0   |  17  |
| $A_{1,3}$ |  0   |  0   |
| $A_{2,4}$ |  19  |  27  |
| $A_{2,5}$ |  19  |  19  |
| $A_{3,2}$ |  15  |  15  |
| $A_{3,5}$ |  15  |  27  |
| $A_{4,6}$ |  29  |  37  |
| $A_{5,6}$ |  38  |  38  |

> 做的时候忘记按照拓扑排序和你拓扑排序来做了。

- 确定哪些活动是关键活动。

> 上标中最迟-最早=0的就是关键活动；有$A_{1,3}、A_{3,2}、A_{2,5}、A_{5,6}$。



