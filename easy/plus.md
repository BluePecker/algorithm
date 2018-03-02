##### A+B问题
---
给出两个整数a和b，求他们的和。但不能使用+等数学运算符

> <font color=red>`样例:`  如果a=1, b=2 返回 3</font>

```CPP
class Solution {
    public:
        // 加法
        int aplusb(int a, int b) {
            int ans = 0;
            while (b) {
                ans = a ^ b;
                b = (a & b) << 1;
                a = ans;
            }
            return ans;
        }

        // int aplusb(int a, int b) {
        //      return b ? aplusb(a ^ b, (a & b) << 1) : a;
        // }

        // 减法
        int minus(int a, int b) {
            return aplusb(a, aplusb(~b, 1));
        }
}
```
