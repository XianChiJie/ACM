实验3-1-if-else 求一元二次方程的根 (20分)

本题目要求一元二次方程ax^2＋bx＋c＝0的根，结果保留2位小数。

### 输入格式:

输入在一行中给出3个浮点系数a、b、c，中间用空格分开。

### 输出格式:

根据系数情况，输出不同结果：

1)如果方程有两个不相等的实数根，则每行输出一个根，先大后小；

2)如果方程有两个不相等复数根，则每行按照格式“实部+虚部i”输出一个根，先输出虚部为正的，后输出虚部为负的；

3)如果方程只有一个根，则直接输出此根；

4)如果系数都为0，则输出"Zero Equation"；

5)如果a和b为0，c不为0，则输出"Not An Equation"。

### 输入样例1:

```in
2.1 8.9 3.5
```

### 输出样例1:

```out
-0.44
-3.80
```

### 输入样例2:

```
1 2 3
```

### 输出样例2:

```
-1.00+1.41i
-1.00-1.41i
```

### 输入样例3:

```
0 2 4
```

### 输出样例3:

```
-2.00
```

### 输入样例4:

```
0 0 0
```

### 输出样例4:

```
Zero Equation
```

### 输入样例5:

```
0 0 1
```

### 输出样例5:

```
Not An Equation
```



```c++
#include<iostream>
#include<cmath>
using namespace std;
int main()
{
	double a, b, c, d, x1, x2;
	cin >> a >> b >> c;
	d = b * b - 4 * a * c;
	if (a == 0) {
		if (b == 0) {
			if (c == 0) printf("Zero Equation\n");
			else printf("Not An Equation\n");
		}
		else printf("%.2f\n", -c / b);
	}
	else if (d == 0) printf("%.2f\n", -b / (a * 2.0));
	else if (d > 0) {
		x1 = ((-b) + sqrt(d)) / (2.0 * a);
		x2 = ((-b) - sqrt(d)) / (2.0 * a);
		printf("%.2f\n%.2f\n", x1, x2);
	}
	else {
		if (b == 0) {
			printf("0.00+%.2fi\n", fabs(sqrt(-d) / 2.0 / a));
			printf("0.00-%.2fi\n", fabs(sqrt(-d) / 2.0 / a));
		}
		else {
			printf("%.2f+%.2fi\n", (-b) / (2.0 * a), fabs(sqrt(-d) / 2.0 / a));
			printf("%.2f-%.2fi\n", (-b) / (2.0 * a), fabs(sqrt(-d) / 2.0 / a));
		}
	}
	return 0;
}
```

