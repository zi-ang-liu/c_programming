**解答例**

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
``` c title="1-1.c"
#include <stdio.h>
int main(void)
{
   printf("Ziang Liu\n");
   return 0;
}
```

``` c title="1-2.c"
#include <stdio.h>
int main(void){
	int dt;
	printf("Input number:");
	scanf("%d",&dt);
	dt = (dt * 7) + 3;
	printf("%d\n",dt);
	return 0;
}
```

``` c title="1-3.c"
#include <stdio.h>
int main(void){
	int dt_1,dt_2, sum;
	printf("Input number 1:");
	scanf("%d",&dt_1);
	printf("Input number 2:");
	scanf("%d",&dt_2);
	sum = dt_1 + dt_2;
	printf("SUM = %d\n",sum);
	return 0;
}
```

## 2. Variables and data types
``` c title="2-1.c"
#include <stdio.h>
int main(void)
{
    int a,b;
    printf("a=");
    scanf("%d",&a);
    b=10/a;
    printf("10/a=%d\n",b);
    return 0;
}
```

``` c title="2-2.c"
#include <stdio.h>
int main(void)
{
    double a,b;
    printf("a=");
    scanf("%lf",&a);
    b=10/a;
    printf("10/a=%f\n",b);
    return 0;
}
```

``` c title="2-3.c"
#include <stdio.h>
int main(void){
	int kokugo, shakai, rika, goukei;　double ave;
	printf("kokugo=");
	scanf("%d",&kokugo);
	printf("shakai=");
	scanf("%d",&shakai);
	printf("rika=");
	scanf("%d",&rika);
	goukei = kokugo + shakai + rika;
	ave = goukei / 3.0;
	printf("SUM=%d AVE=%f\n",goukei, ave);
	return 0;
}
```

``` c title="2-4.c"
#include <stdio.h>
int main(void)
{
	int up, qty, amount, ti;

	printf("Unit price=");
	scanf("%d",&up);
	printf("Quantity=");
	scanf("%d",&qty);

	amount = up * qty;
	ti = amount * 110 / 100;
	printf("Amount of money=%d　Tax included=%d\n",amount,ti);
	
	return 0;
}

```

## 3. Operators
``` c title="3-1.c"
#include <stdio.h>
int main(void){
	int a=123, b=456, r1,r2,r3,r4,r5;
	
	r1 = a + b; //加算
	r2 = a - b; //減算
	r3 = a * b; //乗算
	r4 = a / b; //除算
	r5 = a % b; //剰余算
	
	printf("%d %d %d %d %d\n",r1,r2,r3,r4,r5);
	
	return 0;
}
```

``` c title="3-2.c"
#include <stdio.h>
int main(void){
	double a=12.3, b=45.6, r1,r2,r3,r4;
	
	r1 = a + b; //加算
	r2 = a - b; //減算
	r3 = a * b; //乗算
	r4 = a / b; //除算
	
	printf("%f %f %f %f\n",r1,r2,r3,r4);
	
	return 0;
}
```

``` c title="3-3.c"
#include <stdio.h>
int main(void)
{
	int a,b,c;
	printf("a=");
	scanf("%d",&a);
	printf("b=");
	scanf("%d",&b);
	
	c = a*a-b*b;

	printf("c=%d\n",c);
	return 0;
}

```

``` c title="3-4.c"
#include <stdio.h>
int main(void)
{
	double r,d,l,s;
	printf("radius="); scanf("%lf",&r);
	d=2*r;
	l=3.1416*d;
	s=3.1416*r*r;
	printf("diameter=%f\n",d);
	printf("circumference=%f\n",l);
	printf("area=%f\n",s);
	return 0;
}

```

``` c title="3-5.c"
#include <stdio.h>
int main(void)
{
	int input,hour,min,sec;

	printf("sec=");
	scanf("%d",&input);

	min = input / 60;
	sec = input % 60;
	hour = min / 60;
	min = min % 60;

	printf("%d sec = %d hour %d min %d sec\n",input,hour,min,sec);

	return 0;
}

```

## 4. Basics of control statements

``` c title="4-1.c"
#include <stdio.h>
int main(void)
{
	int month,season;
	printf("month[1-12]="); scanf("%d",&month);
	season = month / 3;
	if(season==1){
		printf("It's spring.\n");
	}
	else if(season==2){
		printf("It's summer.\n");
	}
	else if(season==3){
		printf("It's autumn.\n");
	}
	else{
		printf("It's winter.\n");
	}
	return 0;
}
```

``` c title="4-2.c"
#include <stdio.h>
int main(void)
{
	int large,small,remainder;
	printf("Large number="); scanf("%d",&large);
	printf("Small number="); scanf("%d",&small);

	remainder = large % small;
	if(remainder==0) printf("Multiple!\n");
	else printf("Remainder=%d\n",remainder);
	
	return 0;
}
```

``` c title="4-3.c"
#include <stdio.h>
int main(void)
{
	int a,b,c,min,max;
	printf("a="); scanf("%d",&a);
	printf("b="); scanf("%d",&b);
	printf("c="); scanf("%d",&c);

	if(a>b){
		max=a;  min=b;
	}else{
		max=b;  min=a;
	}
	if(c>max) max=c;
	if(c<min) min=c;

	printf("Maximum=%d Minimum=%d\n",max,min);
	return 0;
}

```

``` c title="4-4.c"
#include<stdio.h>

int main(void){
	char input;
	printf("Input a character:");
	scanf("%c",&input);
	
	if(input >= 'A' && input <= 'Z'){
		printf("upper\n");
	}else if(input >= 'a' && input <= 'z'){
		printf("lower\n");
	}else{
		printf("error\n");
	}
	
	return 0;
}
```


## 5. Control statements and algorithms

``` c title="5-1.c"
#include <stdio.h>
int main(void)
{
	int i;
	for(i=1;i<=100;i++){
		printf("%d\n",i);
	}
	return 0;
}
```

``` c title="5-2.c"
#include <stdio.h>
int main(void)
{
	int n,i=1;
	printf("n="); scanf("%d",&n);
	while(i<=n){
		printf("%d\n",i);
		i++;
	}
	return 0;
}
```

``` c title="5-3.c"
#include <stdio.h>
int main(void)
{
	int i,n,wa=0;
	printf("n="); scanf("%d",&n);
	for(i=1;i<=n;i++){
		if(i%3 != 0) wa+=i;
	}
	printf("wa=%d\n",wa);
	return 0;
}
```

``` c title="5-4.c"
#include <stdio.h>
int main(void)
{
	int i,j;
	for(i=1;i<10;i++){
		for(j=1;j<10;j++){
			printf("%d\t",i*j);
		}
		printf("\n");
	}
	return 0;
}
```


``` c title="5-5.c"
#include <stdio.h>
int main(void){
	int dt,sum;
	sum = 0;
	while(sum < 100){
		printf("Input number=");
		scanf("%d",&dt);
		sum += dt;
	}
	printf("sum=%d\n",sum);
	return 0;
}

```

``` c title="5-6.c"
#include <stdio.h>
int main(void){
	int dt,sum;
	sum = 0;
	while(1){
		printf("Input number=");
		scanf("%d",&dt);
		sum += dt;
		if(sum>=100)break;
	}
	printf("sum=%d\n",sum);
	return 0;
}
```

## 6. Arrays and strings

``` c title="6-1.c"
#include <stdio.h>
int main(void)
{
	int a[4],b;
	printf("a[0]="); scanf("%d",&a[0]);
	printf("a[1]="); scanf("%d",&a[1]);
	printf("a[2]="); scanf("%d",&a[2]);
	printf("a[3]="); scanf("%d",&a[3]);

	b = a[0] + a[1] + a[2] + a[3];
	printf("sum of a[]=%d\n",b);
	return 0;
}
```

``` c title="6-2.c"
#include <stdio.h>
int main(void)
{
    int a[4],b,i;
    for(i=0;i<4;i++){
        printf("a[%d]=",i); scanf("%d",&a[i]);
    }
    b=0;
    for(i=0;i<4;i++){
        b += a[i];
    }
    printf("sum of a[]=%d\n",b);
    return 0;
}
```

``` c title="6-3.c"
#include <stdio.h>
int main(void)
{
    int num[5];
    int i;
    for (i = 0; i < 5; i++){
        printf("#%d:", i + 1);
        scanf("%d", &num[i]);
    }
    printf("\neven: ");
    for (i = 0; i < 5; i++){
        if ((num[i] % 2) == 0)
            printf("%d,", num[i]);
    }
    printf("\nodd: ");
    for (i = 0; i < 5; i++){
        if ((num[i] % 2) != 0)
            printf("%d,", num[i]);
    }
}
```

``` c title="6-4.c"
#include <stdio.h>
#include <string.h>
int main(void)
{
    char ss[50]; int i;
    strcpy(ss,"Taro");
    printf("%s\n",ss);
    i=0;
    while(ss[i]!='\0'){
        printf("%c ",ss[i]);
        i++;
    }
    return 0;
}

```

``` c title="6-5.c"
#include <stdio.h>
int main(void)
{
    char str[50];
    int len = 0;
    printf("String?:");
    scanf("%s", str);
    while (str[len] != 0)
        len++;
    for (len--; len >= 0; len--)
    {
        if (str[len] == 'a')
            str[len] = 'A';
        printf("%c", str[len]);
    }
    printf("\n");
    return 0;
}
```

``` c title="6-6.c"
#include <stdio.h>
int main(void)
{
    int dt[3][3], i, j, total = 0;
    double ave[3];
    //3人分のテスト成績を入力
    for (i = 0; i < 3; i++)
    {
        printf("#%d\n", i + 1);
        for (j = 0; j < 3; j++)
        {
            printf("test result %d:", j + 1);
            scanf("%d", &dt[i][j]);
        }
    }
    //それぞれの平均値を計算
    for (i = 0; i < 3; i++)
    {
        for (j = 0; j < 3; j++)
        {
            total += dt[i][j];
        }
        ave[i] = total / 3.0;
        total = 0;
    }
    //平均値を出力
    printf("\n");
    for (i = 0; i < 3; i++)
        printf("#%d ave:%.2f\n", i + 1, ave[i]);
    return 0;
}

```


## 7. Console input/output

``` c title="7-1.c"
#include <stdio.h>
int main(void)
{
    int num;
    printf("input a number: \n");
    scanf("%d",&num);
    printf("8:%o\n16x:%x\n",num,num);
    return 0;
}
```

``` c title="7-2.c"
#include <stdio.h>
int main(void)
{
    char ss[80]; int i=0;
    printf("Input a string:");
    fgets(ss,80,stdin);
    while(ss[i] != '\0'){
        printf("%2X ",ss[i++]);
    }
    printf("\n");
    return 0;
}
```

``` c title="7-3.c"
#include <stdio.h>
int main(void){
    int i,j,temp;
    char str[100];
    scanf("%s",str);
    for(i=0;str[i]!=0;i++){
        for(j=i+1;str[j]!=0;j++){
            if(str[i] > str[j]){
                temp = str[i];
                str[i] = str[j];
                str[j] = temp;
            }
        }
    }
    printf("%s\n",str);
    return 0;
}
```

## 8. Basics of functions

``` c title="8-1.c"
#include <stdio.h>

void func_hello(void);

int main(void)
{
    func_hello();
    func_hello();
    return 0;
}

void func_hello(void)
{
    printf("Hello\n");
}
```

``` c title="8-2.c"
#include <stdio.h>

double deg2rad(double a);

int main(void)
{
    double ang = 120;
    printf("%f deg = %f rad\n", ang, deg2rad(ang));
    return 0;
}

double deg2rad(double a)
{
    double b;
    b = a * 3.1416 / 180;
    return b;
}
```

``` c title="8-3.c"
#include <stdio.h>

int max_value(int a, int b);

int main(void)
{
	printf("%d\n",max_value(50,100));
	return 0;
}

int max_value(int a, int b)
{
	if(a > b) return a;
	else return b;
}
```

``` c title="8-4.c"
#include <stdio.h>
void DrawTriangle(int size, char ch);
int main(void){
	DrawTriangle(3,'%');
	DrawTriangle(5,'&');
	return 0;
}
void DrawTriangle(int size, char ch){
	int i,j;
	for(i=0;i<size;i++){
		for(j=0;j<=i;j++) printf("%c",ch);
		printf("\n");
	}
}
```

``` c title="8-5.c"
#include <stdio.h>

double fn(double a, double b)
{
	return (a*b)/(a+b);
}

int main(void)
{
    double r1=11, r2=51, ra=30, rb=27, Ra=300, Rb=100;
    double r3, rc, Rc;
    r3 = fn(r1,r2);
    rc = fn(ra,rb);
    Rc = fn(Ra,Rb);
    printf("%.1f %.1f %.1f\n",r3,rc,Rc);
    return 0;
}
```

## 9. Applications of functions

``` c title="9-1.c"
#include <stdio.h>
double average(int num1, int num2);

int main(void){
	int x,y;
	double ave;
	scanf("%d",&x);
	scanf("%d",&y);
	
	ave = average(x,y);
	printf("average of %d and %d = %f\n",x,y,ave);
	
	return 0;
}

double average(int num1, int num2){
	return (num1 + num2)/2.0;
}
```

``` c title="9-2.c"
#include <stdio.h>
double average2(int s[], int len);

int main(void){
	int a[] = {2,4,6,1,5};
	printf("%f\n", average2(a,5));
	return 0;
}

double average2(int s[], int len){
	double sum=0;
	int i;
	for(i=0; i<len; i++){
		sum += s[i];
	}
	return sum/len;
}
```

``` c title="9-3.c"
#include <stdio.h>
void nibai(int s[], int len){
	int i;
	for(i=0;i<len;i++){
		s[i] = s[i] * 2;
	}
}

int main(void){
	int i,a[5] = {1,2,3,4,5};
	for(i=0;i<5;i++){
		printf("%d\t",a[i]);
	}
	printf("\n");
	nibai(a,5);
	for(i=0;i<5;i++){
		printf("%d\t",a[i]);
	}
	return 0;
}
```

``` c title="9-4.c"
#include <stdio.h>

void replace(char s[])
{
	int i=0;
	while(s[i]){
		if(s[i]=='a') s[i]='@';
		i++;
	}
}

int main(void)
{
	char st[]="Okadai Taro";
	puts(st);
	replace(st);
	puts(st);
	return 0;
}
```

## 10. Basic of pointers

``` c title="10-1.c"
#include <stdio.h>
int main(void)
{
    int aa, bb;
    int *pt;
    aa = 123;
    pt = &aa; /*変数aaのアドレスを設定*/
    bb = *pt; /*ポインタptの指すアドレスにある値を設定*/
    printf("aa=%d *pt=%d bb=%d\n", aa, *pt, bb);
    pt = &bb; /*変数bbのアドレスを設定*/
    *pt = 999;
    printf("aa=%d *pt=%d bb=%d\n", aa, *pt, bb);
    return 0;
}
```

``` c title="10-2.c"
#include <stdio.h>
int main(void)
{
    int x, y, *p;
    printf("x=");
    scanf("%d", &x);
    p = &x;
    y = *p;
    printf("x=%d y=%d\n", x, y); // 同じ値の結果を出す
    return 0;
}
```

``` c title="10-3.c"
#include <stdio.h>
int main(void)
{
    int i;
    char s[6], *p;
    printf("Input 5 characters: ");
    fgets(s, 6, stdin);
    p = s;
    for (i = 0; i < 5; i++)
    {
        printf("%c", *(p + 4 - i)); /* p[4-i]でも良い */
    }
    printf("\n");
    return 0;
}
```

``` c title="10-4.c"
#include <stdio.h>
int main(void)
{
    char s[20], *p;
    printf("Input a string(max.19): ");
    fgets(s, 20, stdin);
    p = s; /* p = &s[0]と同じ */
    while (*p != '\0')
    {
        printf("%c ", *p);
        p++;
    }
    return 0;
}
```

## 11. Applications of pointers and structures
``` c title="11-1.c"
#include <stdio.h>
void cmp(char *s1, int *r)
{
    char *s2 = "microwave oven\n";
    *r = 1;
    while (*s1 || *s2)
    {
        if (*s1 != *s2)
            return;
        s1++;
        s2++;
    }
    *r = 0;
}
int main(void)
{
    char s[80];
    int result;
    fgets(s, 80, stdin);
    cmp(s, &result);
    if (result == 1)
        printf("No\n");
    else
        printf("Yes\n");
    return 0;
}
```

``` c title="11-2.c"
#include <stdio.h>
#include <string.h> /*for strlen()*/
void reverse(char *s);
int main(void)
{
    char str[] = "program";
    reverse(str);
    printf("str=%s\n", str);
    return 0;
}
void reverse(char *s)
{
    int wk, n1 = 0, n2;
    n2 = strlen(s) - 1;
    while (n1 < n2)
    {
        wk = *(s + n1);
        *(s + n1) = *(s + n2);
        *(s + n2) = wk;
        ++n1;
        --n2;
    }
}

```

``` c title="11-3.c"
#include <stdio.h>
void repeat(char *strp, int n);
int main(void)
{
    char str[100];
    printf("Input a string:");
    scanf("%s", str);
    repeat(str, 20);
    return 0;
}
void repeat(char *strp, int n)
{
    int i;
    char *p = strp;
    for (i = 0; i < n; i++)
    {
        if (*strp == '\0')
            strp = p;
        printf("%c", *(strp++));
    }
    printf("\n");
}

```

``` c title="11-4.c"
#include <stdio.h>
#include <string.h>
struct myst
{
    char name[40];
    int age;
};
int main(void)
{
    struct myst Taro, Hanako;
    strcpy(Taro.name, "Tanaka Taro");
    Taro.age = 18;
    strcpy(Hanako.name, "Yamada Hanako");
    Hanako.age = 16;
    printf("%s is %d years old.\n", Taro.name, Taro.age);
    printf("%s is %d years old.\n", Hanako.name, Hanako.age);
    return 0;
}
```


## 12. Basics of standard library functions
## 13. Applications of standard library functions
## 14. Comprehensive exercise