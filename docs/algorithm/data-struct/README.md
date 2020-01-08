## 大纲

- 线性表
  - [ ] 数组
  - [ ] 链表
    - [ ] 单向
      - [x] 概念
      - [ ] 相关题型
    - [ ] 双向
    - [ ] 循环
    - [ ] 双向循环
  - [ ] 队列
  - [ ] 栈：普通、阻塞、并发、双端
- 散列表
  - [ ] 散列函数
  - [ ] 冲突解决
    - [ ] 链表法
    - [ ] 开放寻址
    - [ ] 其他
  - [ ] 位图
  - [ ] 动态扩容
- 树
  - [ ] 二叉树：二叉查找树、二叉平衡树、平衡二叉查找树、AVL、红黑、完全二叉树
  - [ ] 多路查找树：B、B+、2-3、2-3-4
  - [ ] 堆：大顶、小顶、二项堆、优先队列
- 图
  - [ ] 图的存储
  - [ ] 路径
  - [ ] 最小生成树
  - [ ] 最短路径
  - [ ] 拓扑排序

## 线性表

### 链表

#### 单链表

[搞懂单链表常见面试题](https://juejin.im/post/5aa299c1518825557b4c5806)

特点：

1. 删除元素时间 `O(1)`，查找一个元素复杂度 `O(n)`
2. 不需要预先分配空间大小，避免空间浪费
3. 无法回溯操作

基本操作：

1. 获取链表长度：遍历链表节点 
2. 查询节点
3. 添加元素
4. 删除元素

!> 由单链表的增加删除可以看出，链表的想要对指定索引进行操作（增加，删除）的时候必须获取该索引的前一个元素。

面试题：

- [x] [876. 链表的中间结点](https://leetcode-cn.com/problems/middle-of-the-linked-list/)：快慢指针
- 判断链表是否为循环链表
  - [x] [141. 环形链表](https://leetcode-cn.com/problems/linked-list-cycle/)：快慢指针，套圈
  - [142. 环形链表 II](https://leetcode-cn.com/problems/linked-list-cycle-ii/)
- 已知一个单链表求倒数第 N 个节点：双指针，有种滑动窗口的意味
- [x] [19. 删除链表的倒数第N个节点](https://leetcode-cn.com/problems/remove-nth-node-from-end-of-list/)
- [x] 旋转单链表：[61. 旋转链表](https://leetcode-cn.com/problems/rotate-list/solution/chuan-zhen-yin-xian-by-liweiwei1419/)
- [x] 反转单链表：[206. 反转链表](https://leetcode-cn.com/problems/reverse-linked-list/) 
  - 🧐递归
  - 迭代
- [x] 反转部分单链表：[92. 反转链表 II](https://leetcode-cn.com/problems/reverse-linked-list-ii/)
- [x] 单链表排序
  - 归并排序：🧐[148. 排序链表](https://leetcode-cn.com/problems/sort-list/)
  - 插入排序：🧐[147. 对链表进行插入排序](https://leetcode-cn.com/problems/insertion-sort-list/)
- [x] 划分链表：[86. 分隔链表](https://leetcode-cn.com/problems/partition-list/)
- [x] 链表相加求和
  - [2. 两数相加](https://leetcode-cn.com/problems/add-two-numbers/)
  - 🧐[445. 两数相加 II](https://leetcode-cn.com/problems/add-two-numbers-ii/)
- 删除链表中的重复的元素
  - [x] 有序链表：[83. 删除排序链表中的重复元素](https://leetcode-cn.com/problems/remove-duplicates-from-sorted-list/)
  - 无序链表：
- [x] 重排链表：[143. 重排链表](https://leetcode-cn.com/problems/reorder-list/)
- [x] 🧐判断两个单链表（无环）是相交：[160. 相交链表](https://leetcode-cn.com/problems/intersection-of-two-linked-lists/)

Tips:

- 常用双指针、快慢指针的方法取某个特定节点
- 不想反转链表可以用栈实现「反转效果」