# 第5章	树和二叉树



#### 1. 选择题

（1）把一棵树转换为二叉树后, 这棵二叉树的形态是（A）。

​	A.	唯一的															  B.	有多种

​	C.	有多种，但根节点都没有左孩子					D.	有多种，但根节点都没有右孩子



（2）由 3 个结点可以构造出多少种不同的二叉树？（D）

​	A.	2																		B.	3

​	C.	4																		D.	5



（3）一棵完全二叉树上有1001个结点，其中叶子结点的个数是（D）。

​	A.	250																	B.	254

​	C.	500																	D.	501

> 我们知道完全二叉树中度为1的结点n1要么只有1个要么没有；还有叶子结点数n0 = n2 + 1；所以第一步得到n0 + n2 = 2n2 + 1；这个数为奇数，我们根据总结点数为1001也为奇数，说明n1=0；那么便可得2n2 + 1 = 1001；得出n0 = 500 + 1 = 501。

（4）一个具有1025个结点的二叉树的高h为（C）。

​	A.	10																		B.	11

​	C.	11至1025之间													D.	10至1024之间

> 当树是完全二叉树时，高是最小的：$h=\log_21025=\log_22^{10}+1=11$；
>
> 当这棵二叉树向链边一样时是最长的：h = 1025。

（5）深度为h的满m叉树的第k层有（A）个结点（$1\leq k\leq h$）

​	A.	$m^{k-1}$																	B.	$m^k-1$

​	C.	$m^{h-1}$																	D.	$m^h-1$



（6）利用二叉链表存储树，则根节点的右指针（C）。

​	A.	指向最左孩子														B.指向最右孩子

​	C.	为空																		D.	非空



（7）对二叉树的结点从 1 开始进行连续编号,要求每个结点的编号大于其左、右孩子的编号,同一结点的左右孩子中, 其左孩子的编号小于其右孩子的编号, 可采用（C）遍历实现编号。

​	A.	先序																		B.	中序

​	C.	后序																		D.	从根开始按层次



（8）在一棵度为4的树T中，若有20个度为4的结点，10个度为3的结点，1个度为2的结点，10个度为1的结点，则树T的叶结点个数是（B）。

​	A.	41																			B.	82

​	C.	113																		  D.	122

> 总结点数等于总度数+1=20×4+10×3+1×2+10×1+1=123；123 - 20 - 10 -1 - 10 = 82。

（9）在下列存储形式中，（D）不是树的存储形式？

​	A.	双亲表示法																B.	孩子链表表示法

​	C.	孩子兄弟表示法														D.	顺序存储表示法



（10）一棵非空的二叉树的先序遍历序列与后序遍历序列正好相反, 则该二叉树一定满足（C）。

​	A.	所有的结点均无左孩子											B.	所有的结点均无右孩子

​	C.	只有一个叶子结点													D.	是任意一棵二叉树



（11）设哈夫曼树中有 199 个结点, 则该哈夫曼树中有（B）个叶子结点。

​	A.	99																				B.	100

​	C.	101																			  D.	102

> n个叶子结点，构成哈夫曼树的话需要增加n-1个结点，得到n+n-1 = 199；n=100。

（12）若 X 是二叉中序线索树中一个有左孩子的结点,且 X 不为根,则 X 的前驱为（C）。

​	A.	X的双亲																		B.	X的右子树中最左的结点

​	C.	X的左子树中最右结点												 D.	X的左子树中最右叶结点

> 中序的顺序为：左	根	右；X为当前子树的根节点，X的左子树中最后一个遍历的结点就是它的前驱，题目现在说X有左孩子，那么X存在左子树，最后访问的结点即为这棵左子树的最右结点。

（13）引入二叉线索树的目的是（A）。

​	A.	加快查找结点的前驱或后继的速度

​	B.	为了能在二叉树中方便地进行插入与删除

​	C.	为了能方便地找到双亲

​	D.	使二叉树的遍历结果唯一



（14）设F是 一 个森林, B是由F变换得的二叉树。若F中有 n 个非终端结点,则B中右指针域为空的结点有（C）个。

​	A.	n - 1																			B.	n

​	C.	n + 1																			D.	n + 2

> 这道题该怎么入手呢？最简单应该是特殊值入手！！

（15）$n(n\geq 2)$个权值均不相同的字符构成哈夫曼树，关于该树的叙述中，错误的是（A）。

​	A.	该树一定是一棵完全二叉树

​	B.	树中一定没有度为1的结点

​	C.	树中两个权值最小的结点一定是兄弟结点

​	D.	树中任一非叶结点的权值一定不小于一下层任一结点的权值



#### 2. 应用题

（1）试找出满足下列条件的二叉树。

- 先序序列与后序序列相同。
- 中序序列与后序序列相同。
- 先序序列与中序序列相同。
- 中序序列与层序遍历序列相同。

> 出这题目，我属实很为难，空数、只有根结点的二叉树。

（2）设一棵二叉树的先序序列：A B D F C E G H ，中序序列：B F D A G E H C。

- 画出这棵二叉树。
- 画出这棵二叉树的后序线索树。
- 将这棵二叉树转换成对应的树（或森林）。

> 我做对了，非常棒。

（3）假设用于通信的电文仅由 8 个字母组成, 字母在电文中出现的频率分别为 0.07, 0.19,0.02, 0.06, 0.32, 0.03, 0.21 , 0.10 。

- 试为这8个字母设计哈夫曼编码。
- 试设计另一种由二进制表示的等长编码方案。
- 对千上述实例, 比较两种方案的优缺点。

（4）已知下列字符 A 、 B 、 C 、 D 、 E 、 F 、 G 的权值分别为 3 、 12 、 7 、 4 、 2 、 8, 11, 试填写出其对应哈夫曼树HT存储结构的初态和终态。

<center>HT的初态</center>

| 结点i | weight | parent | lchild | rchild |
| :---: | :----: | :----: | :----: | :----: |
|   1   |   3    |   0    |   0    |   0    |
|   2   |   12   |   0    |   0    |   0    |
|   3   |   7    |   0    |   0    |   0    |
|   4   |   4    |   0    |   0    |   0    |
|   5   |   2    |   0    |   0    |   0    |
|   6   |   8    |   0    |   0    |   0    |
|   7   |   11   |   0    |   0    |   0    |
|   8   |   -    |   0    |   0    |   0    |
|   9   |   -    |   0    |   0    |   0    |
|  10   |   -    |   0    |   0    |   0    |
|  11   |   -    |   0    |   0    |   0    |
|  12   |   -    |   0    |   0    |   0    |
|  13   |   -    |   0    |   0    |   0    |

<center>HT的终态</center>

| 结点i | weight | parent | lchild | rchild |
| :---: | :----: | :----: | :----: | :----: |
|   1   |   3    |   8    |   0    |   0    |
|   2   |   12   |   12   |   0    |   0    |
|   3   |   7    |   10   |   0    |   0    |
|   4   |   4    |   9    |   0    |   0    |
|   5   |   2    |   8    |   0    |   0    |
|   6   |   8    |   10   |   0    |   0    |
|   7   |   11   |   11   |   0    |   0    |
|   8   |   5    |   9    |   1    |   5    |
|   9   |   9    |   11   |   8    |   4    |
|  10   |   15   |   12   |   3    |   6    |
|  11   |   20   |   13   |   9    |   7    |
|  12   |   27   |   13   |   10   |   2    |
|  13   |   47   |   0    |   11   |   12   |



