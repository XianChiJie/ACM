实验3-3-if-else 比较大小 (10分)

本题要求将输入的任意3个整数从小到大输出。

### 输入格式:

输入在一行中给出3个整数，其间以空格分隔。

### 输出格式:

在一行中将3个整数从小到大输出，其间以“->”相连。

### 输入样例:

```in
4 2 8
```

### 输出样例:

```
2->4->8
```



```c++
#include<iostream>
using namespace std;
int main()
{
	int a[3],temp;
	for (int i = 0; i < 3; ++i) cin >> a[i];
	for (int i = 0; i < 2; i++) for (int j = 0; j < 2 - i; j++) if (a[j] > a[j + 1]) { temp = a[j]; a[j] = a[j + 1]; a[j + 1] = temp; }
	printf("%d->%d->%d\n", a[0], a[1], a[2]);
	return 0;
}
```

