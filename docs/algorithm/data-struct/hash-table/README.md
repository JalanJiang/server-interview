## 散列表

- [LeetCode: 哈希表](https://leetcode-cn.com/explore/learn/card/hash-table/)
- [动画：什么是散列表？](https://juejin.im/post/5c32a4c2f265da611b58823a#heading-10)

分成两种数据结构：

- 哈希集合
- 哈希映射

### 两个关键

- 关键思想：使用**哈希函数**将键映射到存储桶
- 关键问题：哈希函数、冲突解决

### 冲突解决

#### 开放寻址法

- 线性探测法：当我们往散列表中插入数据时，如果某个数据经过散列函数散列之后，存储位置已经被占用了，我们就从当前位置开始，依次往后查找，看是否有空闲位置，直到找到为止。
- 二次探测：二次探测是二次方探测法的简称。顾名思义，使用二次探测进行探测的步长变成了原来的「二次方」，也就是说，它探测的下标序列为 `hash(key)+0，hash(key)+1^2或[hash(key)-1^2]`，`hash(key)+2^2` 或 `[hash(key)-2^2]`。
- 双重散列：所谓双重散列，意思就是不仅要使用一个散列函数，而是使用一组散列函数 `hash1(key)`，`hash2(key)`，`hash3(key)`…… 先用第一个散列函数，如果计算得到的存储位置已经被占用，再用第二个散列函数，依次类推，直到找到空闲的存储位置。

#### 链表法

在散列表中，每个位置对应一条链表，所有散列值相同的元素都放到相同位置对应的链表中。

### 相关题目

- 设计哈希表：
  - [x] [705. 设计哈希集合](https://leetcode-cn.com/problems/design-hashset/)
  - [x] 🤔[706. 设计哈希映射](https://leetcode-cn.com/problems/design-hashmap/)
- [ ] 哈希集合
  - [x] [217. 存在重复元素](https://leetcode-cn.com/problems/contains-duplicate/)
  - [x] [136. 只出现一次的数字](https://leetcode-cn.com/problems/single-number/)
    - 如果不使用额外空间：用异或完成
  - [x] [349. 两个数组的交集](https://leetcode-cn.com/problems/intersection-of-two-arrays/)
  - [x] [202. 快乐数](https://leetcode-cn.com/problems/happy-number/) 
- [ ] 哈希映射
  - [x] [1. 两数之和](https://leetcode-cn.com/problems/two-sum/) 
- [ ] 设计键