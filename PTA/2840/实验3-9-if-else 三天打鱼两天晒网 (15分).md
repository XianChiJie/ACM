实验3-9-if-else 三天打鱼两天晒网 (15分)

中国有句俗语叫“三天打鱼两天晒网”。假设某人从某天起，开始“三天打鱼两天晒网”，问这个人在以后的第N天中是“打鱼”还是“晒网”？

### 输入格式：

输入在一行中给出一个不超过1000的正整数N。

### 输出格式：

在一行中输出此人在第N天中是“Fishing”（即“打鱼”）还是“Drying”（即“晒网”），并且输出“in day N”。

### 输入样例1：

```in
103
```

### 输出样例1：

```out
Fishing in day 103
```

### 输入样例2：

```
34
```

### 输出样例2：

```
Drying in day 34
```

**鸣谢内蒙古师范大学张志平老师补充数据**



```c++
#include<iostream>
using namespace std;
int main()
{
	int n;
	cin >> n;
	if (n % 5 == 4 || n % 5 == 0) printf("Drying in day %d", n);
	else printf("Fishing in day %d", n);
	return 0;
}
```

