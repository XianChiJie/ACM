for 统计素数并求和 (20分)

本题要求统计给定整数*M*和*N*区间内素数的个数并对它们求和。

### 输入格式:

输入在一行中给出两个正整数*M*和*N*（1≤*M*≤*N*≤500）。

### 输出格式:

在一行中顺序输出*M*和*N*区间内素数的个数以及它们的和，数字间以空格分隔。

### 输入样例:

```in
10 31
```

### 输出样例:

```out
7 143
```



```c++
#include<iostream>
using namespace std;
int isPrime(int x) {
	if (x == 0 || x == 1) return 0;
	for (int i = 2; i * i <= x; ++i) if (x % i == 0) return 0;
	return 1;
}
int main()
{
	int m,n,cnt=0,sum=0;
	cin >> m >> n;
	for (; m <= n; m++) if (isPrime(m)) {
		cnt++;
		sum += m;
	}
	cout << cnt << " " << sum << endl;
	return 0;
}
```

