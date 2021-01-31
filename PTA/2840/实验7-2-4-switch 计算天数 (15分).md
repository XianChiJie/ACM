实验7-2-4-switch 计算天数 (15分)

本题要求编写程序计算某年某月某日是该年中的第几天。

### 输入格式:

输入在一行中按照格式“yyyy/mm/dd”（即“年/月/日”）给出日期。注意：闰年的判别条件是该年年份能被4整除但不能被100整除、或者能被400整除。闰年的2月有29天。

### 输出格式:

在一行输出日期是该年中的第几天。

### 输入样例1:

```in
2009/03/02
```

### 输出样例1:

```out
61
```

### 输入样例2:

```
2000/03/02
```

### 输出样例2:

```
62
```

**鸣谢湖北汽车工业学院袁科老师补充数据**



```c++
#include<iostream>
using namespace std;
int main()
{
	int year, month, day,sum=0;
	scanf("%d/%d/%d", &year, &month, &day);
	for (int i = 1; i < month; i++) {
		if (i == 1 || i == 3 || i == 5 || i == 7 || i == 8 || i == 10 || i == 12) sum += 31;
		else if (i == 4 || i == 6 || i == 9 || i == 11) sum += 30;
		else {
			if ((year % 4 == 0 && year % 100) || year % 400 == 0) sum += 29;
			else sum += 28;
		}
	}
	cout << sum + day << endl;
	return 0;
}
```

