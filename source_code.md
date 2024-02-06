**ソースコード**


- [1. Basics](#1-basics)
- [2. Variables and data types](#2-variables-and-data-types)
- [3. Operators](#3-operators)
- [4. Basics of control statements](#4-basics-of-control-statements)
- [5. Control statements and algorithms](#5-control-statements-and-algorithms)
- [6. Arrays and strings](#6-arrays-and-strings)
- [7. Console input/output](#7-console-inputoutput)
- [8. Basics of functions](#8-basics-of-functions)
- [9. Applications of functions](#9-applications-of-functions)
- [10. Basic of pointers](#10-basic-of-pointers)
- [11. Applications of pointers and structures](#11-applications-of-pointers-and-structures)
- [12. Basics of standard library functions](#12-basics-of-standard-library-functions)
- [13. Applications of standard library functions](#13-applications-of-standard-library-functions)
- [14. Comprehensive exercise](#14-comprehensive-exercise)

## 1. Basics

## 2. Variables and data types

## 3. Operators

## 4. Basics of control statements

``` c title="4-1.c"
#include <stdio.h>

int main(void)
{
    int a = 10;
    int b = 20;

    if (a >= 5)
    {
        printf("first sentence\n");
        printf("second sentence\n");
    }

    if (b == 50)
        printf("third sentence\n");
        printf("fourth sentence\n");

    return 0;
}
```

``` c title="4-2.c"
#include <stdio.h>

int main(void)
{
    int a;
    a = 10;
    printf("(a==10) is %d\n", (a == 10));

    if (a == 10)
    {
        printf("code1\n");
    }

    if (5)
    {
        printf("code2\n");
    }

    if (0)
    {
        printf("code3\n");
    }

    if (a)
    {
        printf("code4\n");
    }

    return 0;
}

```

## 5. Control statements and algorithms


"ABC"を10回表示するプログラム

``` c title="5-1.c"
#include <stdio.h>
int main(void)
{
    int i;
    for (i = 1; i <= 10; i++)
    {
        printf("ABC\n");
    }
    return 0;
}
```

1000から2000までの整数をすべて出力するプログラム
``` c title="5-2.c"
#include <stdio.h>
int main(void)
{
    int i;
    for (i = 1000; i <= 2000; i++)
    {
        printf("%d\n", i);
    }
    return 0;
}
```

1から10まで、数え上げて出力する例
``` c title="5-3.c"
#include <stdio.h>
int main()
{
    int i = 1;
    while (i <= 10)
    {
        printf("%d\n", i);
        i++;
    }
    return 0;
}
```

break文
``` c title="5-4.c"
#include <stdio.h>
int main(void)
{
    int i;
    for (i = 1; i <= 10; i++)
    {
        printf("ABC\n");
        if (i == 5)
            break;
    }
    return 0;
}
```

## 6. Arrays and strings

配列x[]の10倍を配列y[]に格納するプログラム
``` c title="6-1.c"
#include <stdio.h>
int main(void)
{
    int x[5] = {11, 12, 13, 14, 15};
    int y[5], i;
    for (i = 0; i < 5; i++)
    {
        y[i] = x[i] * 10;
    }
    for (i = 0; i < 5; i++)
    {
        printf("%d ", y[i]);
    }
    return 0;
}
```

逆行列を求めるプログラム
``` c title="6-2.c"
#include <stdio.h>
int main(void)
{
    double a[2][2] = {{1.0, 2.0}, {3.0, 4.0}};
    double b[2][2], d;
    d = a[0][0] * a[1][1] - a[0][1] * a[1][0];
    b[0][0] = a[1][1] / d;
    b[0][1] = -a[0][1] / d;
    b[1][0] = -a[1][0] / d;
    b[1][1] = a[0][0] / d;

    printf("%f %f\n", b[0][0], b[0][1]);
    printf("%f %f\n", b[1][0], b[1][1]);

    return 0;
}
```

## 7. Console input/output


    
printf()の変換指定
``` c title="7-1.c"
#include <stdio.h>
int main(void)
{
    char c;
    int n;
    double d;
    char s[20] = "abcde";
    c = 65;
    printf("c: %c\n", c); // c: A
    printf("c: %d\n", c); // c: 65
    n = 66;
    printf("n: %c\n", n); // n: B
    printf("n: %d\n", n); // n: 66
    n = 1000;
    printf("  8: %o\n", n); //  8: 1750
    printf(" 10: %d\n", n); // 10: 1000
    printf("16x: %x\n", n); // 16x: 3e8
    printf("16X: %X\n", n); // 16X: 3E8
    d = 56789.12;
    printf("f: %f\n", d);                // f: 56789.120000
    printf("e: %e\n", d);                // e: 5.678912e+004
    printf("E: %E\n", d);                // E: 5.678912E+004
    printf("s: %s\n", s);                // s: abcde
    printf("c=%d n=%d s=%s\n", c, n, s); // c=65 n=1000 s=abcde
    return 0;
}
``` 

printf()のオプション指定
``` c title="7-2.c"
#include <stdio.h>
int main(void)
{
    double d = 654.321;
    printf("[%f]\n", d);    //[654.321000]
    printf("[%12f]\n", d);  //[  654.321000]
    printf("[%9.2f]\n", d); //[   654.32]
    printf("[%9.f]\n", d);  //[  654]
    printf("[%.2f]\n", d);  //[654.32]
}
```

fgets()関数
``` c title="7-3.c"
#include <stdio.h>
int main(void)
{
    char s[100];
    printf("Enter a string: ");
    fgets(s, 100, stdin);
    printf("%s", s);
    return 0;
}
```

scanf()関数とfgets()関数の違い
``` c title="7-4.c"
#include <stdio.h>
int main(void)
{
    char s1[80], s2[80];
    printf("fgets():");
    fgets(s1, 80, stdin);
    printf("s1=%s\n", s1);
    
    printf("scanf():");
    scanf("%s", s1);
    printf("s1=%s\n", s1);
    scanf("%s", s2);
    printf("s2=%s\n", s2);
    return 0;
}
```

## 8. Basics of functions


関数の単純な使用例(1): 引数の3倍+4を返す関数
``` c title="8-1.c"
#include <stdio.h>

void opening(void)
{
    printf("program start\n");
}

int main(void)
{
    opening();
    return 0;
}
```

関数の引数の使用例(2): Yah!を出力する関数
``` c title="8-2.c"
#include <stdio.h>

int func1(int x)
{
    int y;
    y = 3 * x + 4;
    return y;
}

int main(void)
{
    int y;
    y = func1(2);
    printf("y = %d\n", y);
    return 0;
}
```

出席が10回以上ならo,10回未満ならxを出力する関数
``` c title="8-3.c"
#include <stdio.h>
void syusseki_hantei(int kaisu)
{
    if (kaisu >= 10)
    {
        printf("o\n");
    }
    else
    {
        printf("x\n");
    }
}
int main(void)
{
    int i;
    printf("How many times were you present?\n");
    scanf("%d", &i);
    syusseki_hantei(i);
    return 0;
}
```

Nを与えると，1からNまでの和を求めて返す関数
``` c title="8-4.c"
#include <stdio.h>
int tashizan(int n)
{
    int i, t = 0;
    for (i = 1; i <= n; i++)
        t += i;
    return t;
}
int main(void)
{
    int total, n;
    printf("Input N=");
    scanf("%d", &n);
    total = tashizan(n);
    printf("Total=%d\n", total);
    return 0;
}
```


## 9. Applications of functions
関数に数値を渡す
``` c title="9-1.c"
#include <stdio.h>

double ave(double x, double y);

int main(void)
{
    double a = 100, avdt;
    avdt = ave(a, 200);
    printf("%f\n", avdt);
    return 0;
}

double ave(double x, double y)
{
    double wk;
    wk = (x + y) / 2.0;
    return wk;
}
```

配列を関数に渡す
``` c title="9-2.c"
#include <stdio.h>

void disp_ary(int nn[])
{
    printf("nn[0]=%d\n", nn[0]);
    printf("nn[4]=%d\n", nn[4]);
}

int main(void)
{
    int dt[5] = {100, 200, 300, 400, 500};

    disp_ary(dt);

    return 0;
}
```

## 10. Basic of pointers
変数のアドレスの表示
``` c title="10-1.c"
#include <stdio.h>
int main(void)
{
    int mydt = 1234;
    printf("The value of mydt is %d\n", mydt);
    printf("The address of mydt is %p\n", &mydt);
    return 0;
}
```

ポインタの宣言と初期化
``` c title="10-2.c"
#include <stdio.h>
int main(void)
{
    int *p;
    int mydt = 1234;
    p = &mydt;
    printf("The value of mydt is %d\n", mydt);
    printf("The address of mydt is %p\n", &mydt);
    printf("The value of p is %p\n", p);
    printf("The value of *p is %d\n", *p);
    return 0;
}
```

ポインタと配列
``` c title="10-3.c"
#include <stdio.h>
int main(void)
{
    int ary[5] = {100, 200, 300, 400, 500};
    int *p;

    p = &ary[0];
    printf("pt=%p\n", p);
    p = ary;
    printf("pt=%p\n", p);
    return 0;
}
```

ポインタ演算
``` c title="10-4.c"
#include <stdio.h>
int main(void)
{
    int n, ary[3] = {100, 110, 120};
    int *pt = ary;
    n = *pt; // nは100になる
    printf("%d\n", n);
    n = *(pt + 1); // nは110になる
    printf("%d\n", n);
    n = *(pt + 2); // nは120になる
    printf("%d\n", n);
    return 0;
}
```

## 11. Applications of pointers and structures
ポインタ引数で値を戻す
``` c title="11-1.c"
#include <stdio.h>
void func(int *dt);
int main(void)
{
    int nn;
    nn = 1234;
    printf("main: nn=%d\n", nn);
    func(&nn);
    printf("main: nn=%d\n", nn);
    return 0;
}
void func(int *dt)
{
    *dt = 5678;
    printf("func: *dt=%d\n", *dt);
}
```

ポインタで配列を関数に渡す
``` c title="11-2.c"
#include <stdio.h>
void func1(int d[], int len)
{
    int i;
    for (i = 0; i < len; i++)
        printf("%d ", d[i]);
    printf("\n");
}
void func2(int *d, int len)
{
    int i;
    for (i = 0; i < len; i++)
        printf("%d ", *(d + i));
    printf("\n");
}
int main(void)
{
    int nn[4] = {10, 20, 30, 40};
    func1(nn, 4);
    func2(nn, 4);
    return 0;
}
```

ポインタで文字列を関数に渡す
``` c title="11-3.c"
#include <stdio.h>
void strout_p(char *ss);
int main(void)
{
    char st[] = "ABCDEF";
    strout_p(st);
    return 0;
}
void strout_p(char *pp)
{
    printf("pp=%s\n", pp);
    while (*pp)
    { /* *pp!='\0'でも同じ */
        printf("%X ", *pp);
        ++pp;
    }
    printf("\n");
}

```


## 12. Basics of standard library functions
## 13. Applications of standard library functions
## 14. Comprehensive exercise