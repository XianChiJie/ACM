实验4-1-8-while和do-while 求给定精度的简单交错序列部分和 (15分)

本题要求编写程序，计算序列部分和 1 - 1/4 + 1/7 - 1/10 + ... 直到最后一项的绝对值不大于给定精度eps。

### 输入格式:

输入在一行中给出一个正实数eps。

### 输出格式:

在一行中按照“sum = S”的格式输出部分和的值S，精确到小数点后六位。题目保证计算结果不超过双精度范围。

### 输入样例1:

```in
4E-2
```

### 输出样例1:

```out
sum = 0.854457
```

### 输入样例2:

```
0.02
```

### 输出样例2:

```
sum = 0.826310
```

```c++
#include<iostream>
using namespace std;
int main()
{
	double sum = 1,eps,flag=-1,i=1,x=1;
	cin >> eps;
	if (eps >= 1) cout << "sum = 1.000000" << endl;
	else {
		while (x > eps) {
			i += 3;
			x = 1 / i;
			sum += flag* x;
			flag = -flag;
		}
		printf("sum = %.6lf\n", sum);
	}
	return 0;
}
```

