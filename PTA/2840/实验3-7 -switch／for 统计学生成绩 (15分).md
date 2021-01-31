实验3-7 -switch／for 统计学生成绩 (15分)

本题要求编写程序读入N个学生的百分制成绩，统计五分制成绩的分布。百分制成绩到五分制成绩的转换规则：

- 大于等于90分为A；
- 小于90且大于等于80为B；
- 小于80且大于等于70为C；
- 小于70且大于等于60为D；
- 小于60为E。

### 输入格式:

输入在第一行中给出一个正整数N（≤1000），即学生人数；第二行中给出N个学生的百分制成绩，其间以空格分隔。

### 输出格式:

在一行中输出A、B、C、D、E对应的五分制成绩的人数分布，数字间以空格分隔，行末不得有多余空格。

### 输入样例:

```in
7
77 54 92 73 60 65 69
```

### 输出样例:

```
1 0 2 3 1
```



```c++
#include<iostream>
using namespace std;
int main()
{
	int A = 0, B = 0, C = 0, D = 0, E = 0,n,x;
	cin >> n;
	while (n--) {
		cin >> x;
		x /= 10;
		switch (x) {
        case 10:
		case 9:A++; break;
		case 8:B++; break;
		case 7:C++; break;
		case 6: D++; break;
		default:E++; break;
		}
	}
	printf("%d %d %d %d %d\n", A, B, C, D, E);
	return 0;
}
```

