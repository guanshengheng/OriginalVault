这个文件下主要包含做题遇到的一些小寄巧

### [CF2158C](https://codeforces.com/contest/2158/problem/C)
DP的模型。含负数的最大子数组和，数组存以当前结尾的最大的子数组和状态，转移时是
```
dp[i]=max(dp[i-1]+a[i],a[i]);
```
对于存在修改的情况，就要用数组存包含当前元素的最大子数组，然后再对当前元素进行修改。
```
ans=max(dpl[i]+dpr[i]-a[i]+b[i],ans);
```

### [CF2158B](https://codeforces.com/contest/2158/problem/B)
构造和分讨。VP时guess通过了，奇数次的元素贡献固定为1，偶数次的元素贡献可以为2。仅有