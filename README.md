# 跟着[《代码随想录》](https://github.com/youngyangyang04/leetcode-master)开始刷题！
## 第一天（顺便练练markdown写笔记）
### 一、数组
#### 1. 数组是存放在连续内存空间上的相同类型数据的集合。
#### 2. 练练二分查找
    防溢出小技巧：将 middle = (left + right) / 2 写成
    middle = left + (right - left) / 2;
    
[Leetcode : 35.搜索插入位置](https://leetcode-cn.com/problems/search-insert-position/)

[Leetcode : 34.在排序数组中查找元素的第一个和最后一个位置](https://leetcode-cn.com/problems/find-first-and-last-position-of-element-in-sorted-array/)

有一说一看carl写的 看了很久才搞懂意思，属实有点蠢
几乎照着打了一遍，AC不了[流汗] 后面检查出来了
        
[Leetcode : 69.x 的平方根](https://leetcode-cn.com/problems/sqrtx/)

我选择暴力算法从1开始
```cpp 
class Solution {
public:
    int mySqrt(int x) {
        if (x == 0) return 0;
        for (long long i = 1; i <= (x + 1) / 2 ; i++) {
            if( i * i <= x && (i + 1L * (i + 1) > x) return i;
        }
        return -1;
    }
};
```
发现好像跑不了很大大数 例如:2147483647
错误提示:
    Line 5: Char 39: runtime error: signed integer overflow: 2147483647 + 1 cannot be represented in type 'int' (solution.cpp)
    SUMMARY: UndefinedBehaviorSanitizer: undefined-behavior prog_joined.cpp:14:39

突然发现好像咱练习的是二分查找 明天想想该咋做($\color{#FF0000}{2022.4.22}$ )

[Leetcode : 367.有效的完全平方数](https://leetcode-cn.com/problems/valid-perfect-square/)

