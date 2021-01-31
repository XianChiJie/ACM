实验2-3-5-for／is-else 输出华氏-摄氏温度转换表 (15分)

输入2个正整数`lower`和`upper`（`lower`≤`upper`≤100），请输出一张取值范围为[`lower`，`upper`]、且每次增加2华氏度的华氏-摄氏温度转换表。

温度转换的计算公式：*C*=5×(*F*−32)/9，其中：*C*表示摄氏温度，*F*表示华氏温度。

### 输入格式:

在一行中输入2个整数，分别表示`lower`和`upper`的值，中间用空格分开。

### 输出格式:

第一行输出："fahr celsius"

接着每行输出一个华氏温度fahr（整型）与一个摄氏温度celsius（占据6个字符宽度，靠右对齐，保留1位小数）。

若输入的范围不合法，则输出"Invalid."。

### 输入样例1:

```in
32 35
```

### 输出样例1:

```out
fahr celsius
32   0.0
34   1.1
```

### 输入样例2:

```
40 30
```

### 输出样例2:

```
Invalid.
```



```c++
#include<iostream>
using namespace std;
int main()
{
	int m, n;
	double f;
	cin >> m >> n;
	if (m > n || n > 100) printf("Invalid.\n");
	else {
		printf("fahr celsius\n");
		for (; m <= n; m+=2) {
			f = 5 * (m - 32) *1.0/ 9;
			printf("%d%6.1lf\n", m, f);
		}
	}
	return 0;
}
```

