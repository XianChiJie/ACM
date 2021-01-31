实验10-7 -递归函数 递归求Fabonacci数列 (10分)

本题要求实现求Fabonacci数列项的函数。Fabonacci数列的定义如下：

*f*(*n*)=*f*(*n*−2)+*f*(*n*−1) (*n*≥2)，其中*f*(0)=0，*f*(1)=1。

### 函数接口定义：

```c++
int f( int n );
```

函数`f`应返回第`n`个Fabonacci数。题目保证输入输出在长整型范围内。建议用递归实现。

### 裁判测试程序样例：

```c++
#include <stdio.h>

int f( int n );

int main()
{
    int n;

    scanf("%d", &n);
    printf("%d\n", f(n));

    return 0;
}

/* 你的代码将被嵌在这里 */
```

### 输入样例：

```in
6
```

### 输出样例：

```out
8
```



```c++
int f( int n ){
    int a=0,b=1,t;
    if(n==0||n==1) return n==0?0:1;
    for(int i=1;i<n;i++) {
        t=b;
        b=a+b;
        a=t;
    }
    return b;
}
```

