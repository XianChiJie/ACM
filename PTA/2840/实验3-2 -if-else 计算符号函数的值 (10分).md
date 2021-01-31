实验3-2 -if-else 计算符号函数的值 (10分)

对于任一整数*n*，符号函数sign(n)的定义如下：

![](https://raw.githubusercontent.com/XianChiJie/PicGoimg/master/20210131085735.png)

请编写程序计算该函数对任一输入整数的值。

### 输入格式:

输入在一行中给出整数n。

### 输出格式:

在一行中按照格式“sign(n) = 函数值”输出该整数n对应的函数值。

### 输入样例1:

```in
10
```

### 输出样例1:

```out
sign(10) = 1
```

### 输入样例2:

```
0
```

### 输出样例2:

```
sign(0) = 0
```

### 输入样例3:

```
-98
```

### 输出样例3:

```
sign(-98) = -1
```



```c++
#include<iostream>
using namespace std;
int main()
{
	int n;
	cin >> n;
	if (n > 0) printf("sign(%d) = 1", n);
	else if (n == 0) printf("sign(0) = 0");
	else printf("sign(%d) = -1", n);
	return 0;
}
```

