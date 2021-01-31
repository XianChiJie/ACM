实验4-1-4-while和do-while 求整数的位数及各位数字之和 (15分)

对于给定的正整数N，求它的位数及其各位数字之和。

### 输入格式：

输入在一行中给出一个不超过10<sup>9</sup>的正整数N。

### 输出格式：

在一行中输出N的位数及其各位数字之和，中间用一个空格隔开。

### 输入样例：

```in
321
```

### 输出样例：

```out
3 6
```



```c++
#include<iostream>
using namespace std;
int main()
{
	long long x, sum = 0,cnt=0;
	cin >> x;
	while (x) {
		sum += x % 10;
		x /= 10;
		cnt++;
	}
	printf("%lld %lld\n", cnt, sum);
	return 0;
}
```

