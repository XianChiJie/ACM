实验6-1-for 近似求PI (15分)

本题要求编写程序，根据下式求*π*的近似值，直到最后一项小于给定精度eps。
$$
\frac{\pi}{2} = 1+\frac{1!}{3}+\frac{2!}{3*5}+\frac{3!}{3*5*7}+...+\frac{i!}{3*5*...*(2*i-1)}+...
$$

### 输入格式：

输入在一行中给出精度eps，可以使用以下语句来读输入：

```c++
scanf("%le", &eps);
```

### 输出格式：

在一行内，按照以下格式输出*π*的近似值（保留小数点后5位）：

```
PI = 近似值
```

### 输入样例：

```in
1E-5
```

### 输出样例：

```out
PI = 3.14158
```



```c++
#include<iostream>
using namespace std;
int main()
{
	double eps,mu=3,sum=1,zi=1;
	cin >> eps;
	if (eps >= 1) printf("PI = 2.00000\n");
	else {
		for (double i=2; zi / mu >= eps;++i) {
			sum += zi / mu;
			zi *= i;
			mu *= 2 * i+ 1;
		}
		printf("PI = %.5lf\n", (sum+zi/mu) * 2);
	}
	return 0;
}
```

