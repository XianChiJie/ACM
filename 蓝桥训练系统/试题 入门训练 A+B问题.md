## 试题 入门训练 A+B问题



资源限制

时间限制：1.0s  内存限制：256.0MB



问题描述

输入A、B，输出A+B。



输入格式

输入的第一行包括两个整数，由空格分隔，分别表示A、B。



输出格式

输出一行，包括一个整数，表示A+B的值。



样例输入

12 45



样例输出

57



数据规模与约定

-10000 <= A, B <= 10000。



```c++
#include <iostream>
using namespace std;
int main()
{
    int a, b;
    cin >> a >> b;
    cout << a + b;
    return 0;
}
```

