实验4-1-2-while和do-while 求奇数和 (15分)

本题要求计算给定的一系列正整数中奇数的和。

### 输入格式:

输入在一行中给出一系列正整数，其间以空格分隔。当读到零或负整数时，表示输入结束，该数字不要处理。

### 输出格式:

在一行中输出正整数序列中奇数的和。

### 输入样例:

```in
8 7 4 3 70 5 6 101 -1
```

### 输出样例:

```
116
```



```c++
#include<iostream>
using namespace std;
int main()
{
	int x,sum=0;
	cin >> x;
	while (x > 0) {
		if (x % 2) sum += x;
		cin >> x;
	}
	cout << sum << endl;
	return 0;
}
```

