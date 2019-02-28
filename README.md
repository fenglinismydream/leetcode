# leetcode

1、[Two Sum   ---easy](https://github.com/fenglinismydream/leetcode/blob/master/test/1.%20Two%20Sum)
=====
题目：给定一个整数数组，两个数字的返回索引，它们加到一个特定的目标。
-----
思路：一个双循环，第二个循环从第一个循环下标的下一个作为起点。(暴力解法，此解法算是刚拿到题目首先想到的解法。)<br>
另一种解法：提高降低时间复杂度，增加空间复杂度。

2、[Add Two Numbers   ---medium](https://github.com/fenglinismydream/leetcode/blob/master/test/2.%20Add%20Two%20Numbers)
=====
题目：给出了两个非空链表，表示两个非负整数。数字以倒序存储，每个节点都包含一个数字。添加两个数字并将其作为一个链表返回。(给定两个长度不定的单链表，数字以倒序存储，两个单链表相加，返回一个单链表)
-----
思路：当时第一次看到题目的时候，没有看懂题意，对链表的知识掌握不多，忘记了链表的定义和一些基本的操作。题目中括号里是之后自己对题目的理解。题目中并没有规定两个链表的长度是否相同，就要考虑长度不同的情况。至于倒序存储还没有明白（如果接下来搞明白，会来记录一下）

3、[Longest Substring Without Repeating Characters](https://github.com/fenglinismydream/leetcode/blob/master/test/3.%20Longest%20Substring%20Without%20Repeating%20Characters.html)  ---medium
=====
题目：给定一个字符串，查找没有重复字符的最长子字符串的长度。
-----
思路: 中心扩展,在回文中心的两侧互为镜像.因此可以从它的中心展开,并且只有2n-1个这样的中心(字母数为偶数的回文的中心可以处于两字母之间)

4、Median of Two Sorted Arrays  ---hard
=====
题目：在两个有序数组中寻找中位数  时间复杂度应该为O(log(m+n))
-----
思路：1、自己的解法：（hhhhhhhhhhhhhhhhaaa）当自己写出来的时候，完全笑了，原来还能这样做，怎么看怎么不像是算法，放在这里就让大家看下笨人的笨方法吧- -。我看到了时间复杂度的要求！我也知道要用二分法！但是我不会！等着，我去学习然后更新这个题目二分法解法！！！

5、Longest Palindromic Substring  ---medium
=====
题目：给定一个字符串s，在s中找到最长的回文子串，你可以假设s的最大长度是1000。
-----
思路：假设字符串为'dbaaab'，<br>
1、从i=0开始，prev记录字符串开始下标，next记录字符串结束下标，（next、prev分别等于i值）。maxLen记录回文字符串长度，先判断相邻字段是否相同，如（d和b）<br>
2、不相同则判断db向两边扩散，next++,prev--，此时prev= -1 所以i=0判断结束,i++<br>
3、当i=2,下标为next和next+1的相同时，++next，直至next!==next+1，此时prev =2,next=4, 进入2步骤<br>
4、记录prev,maxLen，输出s.substr(prev,manLen)

6、[Reverse Integer  ---easy](https://github.com/fenglinismydream/leetcode/blob/master/test/6.%20Reverse%20Integer)
=====
题目:给出一个 32 位的有符号整数，你需要将这个整数中每位上的数字进行反转。
-----
注意:假设我们的环境只能存储得下 32 位的有符号整数，则其数值范围为 [−231,  231 − 1]。请根据这个假设，如果反转后整数溢出那么就返回 0。<br>
思路:
- 数字转为字符串操作
- 取余反转

7、 [String to Integer (atoi)](https://github.com/fenglinismydream/leetcode/blob/master/test/7.%20String%20to%20Integer%20(atoi))
=====
题目: 使其能将字符串转换成整数.
-----
思路:
- 字符串操作
- 正则匹配

8、 [Palindrome Number]()
=====
题目: 判断一个整数是否是回文数。回文数是指正序（从左向右）和倒序（从右向左）读都是一样的整数。
-----
思路:
- 将数字转换为字符串
- 将数字反转,然后将反转后的数字跟原数字比较,为了避免反转后的数字超过int整数范围.尝试反转一半,即1221反转后一半21为12,如是回文,必与前一半相同.如何判定是否反转了一半,在于反转后的数字大于原数字反转后剩下的即为反转了一半.如果原始数字为奇数长度.如121,反转一半后为12,原始数字剩下1,即反转后除以10,去掉中位数(因为奇数长度的回文数字,中位数一定是自己等于自己),来比较即可.


