实验3-8 -if-else 输出三角形面积和周长 (15分)

本题要求编写程序，根据输入的三角形的三条边*a*、*b*、*c*，计算并输出面积和周长。注意：在一个三角形中， 任意两边之和大于第三边。三角形面积计算公式：
$$
area=\sqrt{s(s−a)(s−b)(s−c)}
$$
其中*s*=(*a*+*b*+*c*)/2。

### 输入格式：

输入为3个正整数，分别代表三角形的3条边*a*、*b*、*c*。

### 输出格式：

如果输入的边能构成一个三角形，则在一行内，按照

```
area = 面积; perimeter = 周长
```

的格式输出，保留两位小数。否则，输出

```
These sides do not correspond to a valid triangle
```

### 输入样例1：

```in
5 5 3
```

### 输出样例1：

```out
area = 7.15; perimeter = 13.00
```

### 输入样例2：

```
1 4 1
```

### 输出样例2：

```
These sides do not correspond to a valid triangle
```



```c++
#include<iostream>
#include<cmath>
using namespace std;
int main()
{
	double a, b, c,s;
	cin >> a >> b >> c;
	if (a + b > c && a + c > b && b + c > a && fabs(a - b) < c && fabs(a - c) < b && fabs(b - c) < a) {
		s = (a + b + c) / 2;
		printf("area = %.2lf; perimeter = %.2lf\n", sqrt(s * (s - a) * (s - b) * (s - c)), a + b + c);
	}
	else cout << "These sides do not correspond to a valid triangle" << endl;
	return 0;
}
```

