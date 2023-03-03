---
title: 'math'
date: 2021-03-14 20:57:54
tags: system design
index_img: /img/page/cpp.png
---

## 指数POW函数

```c++
int pow(unsigned long long int num, int p) { // 要求num > 0, 0 <= p <= 64
        unsigned long long int ret = 1;
        unsigned int MOD = pow(10, 9) + 7;
        
        for (unsigned long long int i = 0, index = 1, tt = num % MOD; i < 64; i++) {
            if (p & index) {
                ret = (ret * tt) % MOD;
            }
            
            tt = (tt * tt) % MOD;
            index <<= 1;
        }
        
        return ret;
    }
```



