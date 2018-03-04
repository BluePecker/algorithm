### 尾部的零
---
设计一个算法，计算出n阶乘中尾部零的个数。

> <font color=red>`样例:` 11!=39916800，因此应该返回2</font>

```CPP
class Solution
{
    public:

        long long trailingZeros(long long n)
        {
            long long sum = 0;
            while((n /= 5) != 0) {
                sum += n;
            }
            return sum;
        }
};
```
