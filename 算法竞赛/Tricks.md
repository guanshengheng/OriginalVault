这个文件下主要包含做题遇到的一些小寄巧

### [CF2158C](https://codeforces.com/contest/2158/problem/C)
DP的模型。含负数的最大子数组和，数组存以当前结尾的最大的子数组和状态，转移时是
```
dp[i]=max(dp[i-1]+a[i],a[i])
```
