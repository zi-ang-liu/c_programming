**C言語演習問題**

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
**問題１.** 
自分の名前をローマ字で出力するプログラム （教科書p.16参考）

**問題２.**
キーボードから入力された数値を，７倍した後，３加えて，出力するプログラム

**問題３.**
キーボードから入力された２つの数値の和を計算して出力するプログラム

**問題４.**
余裕があれば，教科書p.34の練習問題に取り組みましょう．とにかく，たくさん書いて覚える．

## 2. Variables and data types
**問題１.** 
キーボードから入力した数値をaへ格納し，10÷aの計算結果を出力するプログラム．ただし，変数はint型で宣言すること．10÷aはプログラムでは10/aと書く．

**問題２.** 
上と同じプログラム. ただし，変数はdouble型で宣言すること. 

!!! note
	練習１と２の出力結果が異なることを体験してください．

**問題３.** 
国語，社会，理科の３科目の点数を入力し，３科目の合計と平均を表示する．

??? tip
	科目の点数の合計は整数型，平均は浮動小数点型  

**問題４.** 
単価，数量を入力し，金額と消費税込みの金額を表示する．

??? tip
	* 税込み金額＝金額×110÷100   
	* 金額は整数型で扱う

## 3. Operators
**問題１.** 
a=123, b=456とし，それぞれの数値の加算・減算・乗算・除算・剰余算の結果を出力するプログラムを作れ．

**問題２.** 
a=12.3, b=45.6とし，それぞれの数値の加算・減算・乗算・除算の結果を出力するプログラムを作れ．
   
**問題３.** 
$a, b$を入力すると，$𝑎^2-𝑏^2$を求めるプログラムを作れ．

**問題４.** 
円の半径を入力すると，直径，円周，面積をそれぞれ計算・出力するプログラムを作れ．

??? tip
	* 円周率は3.1416等の定数を書く．（有効桁数は必要に応じて自分で決める）

**問題５.** 
秒数で表される時間を入力し，時間・分・秒に変換し表示するプログラムを作れ．

??? tip
	* 秒数÷６０→分、　余りを秒とする。
	* 分　÷６０→時間、余りを分とする。


## 4. Basics of control statements
**問題１.** 
月(1～12)を入力すると，下の表のように対応する季節(spring, summer, autumn, winter)を出力するプログラムを作れ.    

      | 入力値(month) | 出力メッセージ |
      | ------------- | -------------- |
      | 3~5           | It's spring.   |
      | 5~8           | It's summer.   |
      | 9~11          | It's autumn.   |
      | 12,1,2        | It's winter.   |


**問題２.** 
大小2つの整数を入力し，小さい方で大きい方が割り切れたら"Multiple!"（倍数）と出力し，割り切れなければ余りを出力するプログラム.

**問題３.** 
キーボードから３つの数を入力すると，その中で最大値と最小値を出力するプログラムを作れ．

**問題４.** 
キーボードから1文字入力し，大文字なら「upper」，小文字なら「lower」，それ以外なら「error」と出力するプログラムを作れ．

## 5. Control statements and algorithms
**問題１.** 
for文を使って，1から100までの整数をすべて出力せよ．

**問題２.** 
while文を使って，1から𝑛までの整数をすべて出力せよ．𝑛はキーボードから入力した値．

**問題３.** 
1からnまでの整数のうち，３で割り切れない数の和を求めよ．nはキーボードから入力した値．

**問題４.** 
九九表（1の段～９の段）を表示せよ．

**問題５.** 
キーボードから数値を繰り返し入力し，その合計が100以上になったら入力を止めて，合計を表示せよ．

**問題６.** 
5のプログラムを無限ループを使って作れ．

## 6. Arrays and strings
**問題１.** 
キーボードから入力した4つの数値を4つの配列にそれぞれ記憶させた後，それらの合計を求めて出力せよ．（forやwhileは使わずに）

**問題２.** 
上と同じことをfor文を使って作る．入力時と計算時で，for文を２度使ってよい. (4回繰り返すためにforを使う)

**問題３.** 
5個の数値をキーボードから入力し，入力された数値を偶数と奇数に分けて表示するプログラムを作成せよ．

**問題４.** 
char ss[50];と宣言された配列に，自分の名前（半角ローマ字）を格納し，出力せよ．（キーボードからの入力でなくて良い）. さらに，配列ss[]の各要素（格納されている値）を1文字ずつで出力せよ．参考：p.49

**問題５.** 
入力された文字列を逆順に表示するプログラムを作成せよ．またプログラム中に「a」が含まれていたら，「A」に変換せよ．

**問題６.** 
3人の学生のテスト結果(3回分)をキーボードから入力し，それぞれの平均点を計算し，出力せよ．

??? tip
	配列の要素ss[ ]が0（‘\0’）である所までを繰り返し文(forやwhileなど)を使って出力する．

## 7. Console input/output
**問題１.** 
キーボードから入力した10進数の数値を，8進数と16進数で表示せよ．

**問題２.** 
キーボードから入力した文字列を配列に格納し，１文字ずつ文字コード（2桁の16進数）で表示せよ．(参考： p.244-245) 

**問題３.** 
キーボードから入力した文字列をアルファベット順に並び替えて出力せよ．ただし，入力するアルファベットはすべて小文字とする．

??? tip
	- scanfは%sで文字列読み込みができる(p.117)
	- 各文字は文字コード表にある値で表される(p.244 – 245)
	- 「隣り合う配列の要素と比較し，順序が逆であれば入れ替える」ということを繰り返す

## 8. Basics of functions
問題１. 「Hello」と出力する関数（引数なし，戻り値なし）を作り，main()関数内から２回呼び出せ．参考：p.124

問題２. 度単位の角度を引数として渡すと，ラジアン単位に換算した戻り値を返す関数（引数double型，戻り値double型）を作り，main()関数でその関数を使え．($\pi/180*deg=rad$)

問題３. ２つの整数を渡すと，大きい方の数値を戻り値として返す関数を作り，main()関数でその関数を使え．

問題４. サイズを示す数値（整数）と，表示する文字を引数として渡すと，引数で指定した文字とサイズの三角形を表示する関数を作り，main()関数でその関数を使え．

問題５. 下のプログラムでは，同じような計算が何度も出てくる．計算の部分を関数化し，それを用いてプログラム記述をシンプルにせよ． (この計算式は並列抵抗値を求める)

``` c title="5.c"
#include <stdio.h>

int main(void)
{
    double r1=11, r2=51, ra=30, rb=27, Ra=300, Rb=100;
    double r3, rc, Rc;
    r3 = (r1*r2)/(r1+r2);
    rc = (ra*rb)/(ra+rb);
    Rc = (Ra*Rb)/(Ra+Rb);
    printf("%.1f %.1f %.1f\n",r3,rc,Rc);
    return 0;
}
```

## 9. Applications of functions
問題１. ２つの整数の平均値をdouble型で返す関数averageを作れ．またその動作を確認せよ．
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
    // ???
}

```
問題２. int型の配列とその長さを引数として渡すと，その平均値をdoubleで返す関数average2を作れ．またその動作を確認せよ．
``` c title="9-2.c"
#include <stdio.h>
double average2(int s[], int len);

int main(void){
	int a[] = {2,4,6,1,5};
	printf("%f\n", average2(a,5));
	return 0;
}

double average2(int s[], int len){
	// ???
}

```

問題３. 引数に渡されたint型の配列の各数値を2倍にする関数nibaiを作れ．またその動作を確認せよ．
``` c title="9-3.c"
#include <stdio.h>
void nibai(int s[], int len){
	// ???
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

問題４. 引数に渡された文字列を調べて「a」があれば「@」に置き換える関数replaceを作れ．またその動作を確認せよ．
``` c title="9-4.c"
#include <stdio.h>
void replace(char s[])
{
    // ???
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
Problem 1. A~Cを適切に埋め，プログラムを実行せよ．
``` c title="10-1.c"
#include <stdio.h>
int main(void)
{
    int aa, bb;
    int *pt;
    aa = 123;
    pt = /*A 変数aaのアドレスを設定*/
    bb = /*B ポインタptの指すアドレスにある値を設定*/
    printf("aa=%d *pt=%d bb=%d\n", aa, *pt, bb);
    pt = /*C 変数bbのアドレスを設定*/
    *pt = 999;
    printf("aa=%d *pt=%d bb=%d\n", aa, *pt, bb);
    return 0;
}
```

Problem 2. 下の？に適当なプログラムを書いて，キーボードから入力されたｘの値をyにもコピーせよ．ただし，y=x; を書いてはいけない．
``` c title="10-2.c"
#include <stdio.h>
int main(void)
{
    int x, y, *p;
    printf("x=");
    // ??
    // ??
    // ??
    printf("x=%d y=%d\n", x, y); // 同じ値の結果を出す
    return 0;
}
```

Problem 3. 下線部を埋めて，入力した５文字が逆順で表示されるようにせよ．ただし，sを使ってはいけない．pとiは使ってよい．
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
        printf("%c", ________); /* p[4-i]でも良い */
    }
    printf("\n");
    return 0;
}
```

Problem 4. 入力した文字列を一文字ずつ表示させるプログラムを作れ．ただし，ポインタを使うこと．
``` c title="10-4.c"
#include <stdio.h>
int main(void)
{
    char s[20], *p;
    printf("Input a string(max.19): ");
    fgets(s, 20, stdin);
    // ???
    // ???
	// ???
    // ???
	// ???
    // ???
    return 0;
}
```

## 11. Applications of pointers and structures
Problem 1. 下線部(4カ所)を埋めて，プログラムを完成させよ．
``` c title="11-1.c"
#include <stdio.h>
// void cmp(char ____, int *r)
{
    char *s2 = "microwave oven\n";
    // *r = ____;
    while (*s1 || *s2)
    {
        if (*s1 != *s2)
            return;
        // ____++;
        s2++;
    }
    *r = 0;
}
int main(void)
{
    char s[80];
    int result;
    fgets(s, 80, stdin);
    // cmp(s, ____);
    if (result == 1)
        printf("No\n");
    else
        printf("Yes\n");
    return 0;
}
```

Problem 2. 文字列を渡すと逆順にする関数reverse()を作れ．
``` c title="11-2.c"
#include <stdio.h>
#include <string.h> /*for strlen()*/
void reverse(char *s);
int main(void)
{
    
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

Problem 3. 文字列と繰り返す文字を，渡した文字数分，入力した文字列を繰り返し表示する関数を作れ．
``` c title="11-3.c"
#include <stdio.h>
void repeat(char *strp, int n);
int main(void)
{

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

Problem 4. 下線部を埋めて，プログラムを完成させよ．
``` c title="11-4.c"
#include <string.h>
struct myst
{
    char name[40];
    int age;
};
int main(void)
{
    struct ____ Taro, Hanako;
    strcpy(______, "Tanaka Taro");
    ___ = 18;
    strcpy(______, "Yamada Hanako");
    ______ = 16;
    printf("%s is %d years old.\n", ______, ______);
    printf("%s is %d years old.\n", ______, ______);
    return 0;
}
```


## 12. Basics of standard library functions
## 13. Applications of standard library functions
## 14. Comprehensive exercise