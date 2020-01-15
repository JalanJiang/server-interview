## 链表

### 单链表

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

### 双向链表

- 构建：前面插入

### 循环链表

### 其他题目

- [x] [203. 移除链表元素](https://leetcode-cn.com/problems/remove-linked-list-elements/submissions/)

## 栈

- [数据结构和算法面试题系列—栈](https://juejin.im/post/5b9c78cdf265da0ab915b5da)

## 特点

后进先出。

- 后缀表达式
- 函数递归

## 基本操作

- 压入 `push`
- 弹出栈顶元素 `pop`
- 取出栈顶元素 `peek`

## 相关题目

- [ ] [150. 逆波兰表达式求值](https://leetcode-cn.com/problems/evaluate-reverse-polish-notation/)