实验10-6-递归函数 递归计算Ackermenn函数 (15分)

本题要求实现Ackermenn函数的计算，其函数定义如下：

![](https://raw.githubusercontent.com/XianChiJie/PicGoimg/master/20210131213859.png)

### 函数接口定义：

```c++
int Ack( int m, int n );
```

其中`m`和`n`是用户传入的非负整数。函数`Ack`返回Ackermenn函数的相应值。题目保证输入输出都在长整型

范围内。

### 裁判测试程序样例：

```c++
#include <stdio.h>

int Ack( int m, int n );

int main()
{
    int m, n;

    scanf("%d %d", &m, &n);
    printf("%d\n", Ack(m, n));

    return 0;
}

/* 你的代码将被嵌在这里 */
```

### 输入样例：

```in
2 3
```

### 输出样例：

```out
9
```



```c++
int Ack( int m, int n ){
    if(!m) return n+1;
    else if(m>0&&n==0) return Ack(m-1,1);
    else if(m>0&&n>0) return Ack(m-1,Ack(m,n-1));
}
```

