实验4-1-1-while和do-while 最大公约数和最小公倍数 (15分)

本题要求两个给定正整数的最大公约数和最小公倍数。

### 输入格式:

输入在一行中给出两个正整数M和N（≤1000）。

### 输出格式:

在一行中顺序输出M和N的最大公约数和最小公倍数，两数字间以1空格分隔。

### 输入样例:

```in
511 292
```

### 输出样例:

```out
73 2044
```

**鸣谢安阳师范学院段晓云老师和软件工程五班李富龙同学补充测试数据！**



```c++
#include<iostream>
using namespace std;
int main()
{
	int a, b,x,y, c;
	cin >> a >> b;
	x = a >= b ? a : b;
	y = a <= b ? a : b;
	c = x % y;
	while (c) {
		x = y;
		y = c;
		c = x % y;
	}
	printf("%d %d\n", y, a * b / y);
	return 0;
}
```

