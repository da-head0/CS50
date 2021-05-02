
```
#include <stdio.h> #stdio.h 라는 이름의 파일을 찾아서 printf 함수에 접근할 수 있도록 해줌
int main(void)
```
시작한다는 의미.

C언어에서는 print 대신에 printf를 쓴다. 그리고 명령어 뒤에 ;을 붙인다.

\n : 줄바꿈 기능.

C로 작성한 코드는 "파일이름.c"로 저장한다. (C로 작성된 코드라는 의미)

우리가 작성한 `소스 코드`를 2진수로 변환하는 작업을 `컴파일러`가 해준다. 컴퓨터가 이해할 수 있도록.

```
./a.out # 현재 디렉토리에 있는 a.out이란 프로그램을 실행하게 해줌.
```
맨 앞의 .은 현재 폴더를 나타낸다.

---

```
string answer = get_string ("What's your name? \n");
printf ("hello,%s\n, answer);
```
String = assign types
Placeholder %s

\n이 " " 밖에 있다면? -> error message.
" ~ \n" → 이렇게 안에 있어야 함.
`clang -o string string.c -lcS50`
:연결해 주는것
hello → machine code
hello. c → sourcecode)
`make string`으로 알아서 컴파일하게 할 수 있다. (" 프로그램을 실행해라")
→ 소스코드에서 머신코드를 만들음


## 반복문, 조건문

```
if (x > y)
{
    printf ("x가 y보다 크다\n");
}
else if (x < y)
{
    printf("y가 x보다 크다\n");
}
else if (x==y) <!-- 당연한 것이니 생략 가능 -->
{ 
    printf("x is equal to y\n");
}
```
```
while (true)
{
    print ("hello, world\n");
}
```

`counter += 1`  = `counter ++` 로 표시할 수 있다.

```
for (int i = 0; i < 50 ; i = i + 1)
{
    printf ("hello, world\n");
}
<!-- 세미콜론으로만 구분, 쉼표 안 씀 -->
for (int i = 0 ; i < 10 ;  i ++)
{
    printf ("개발 공부는 재미있다!\n");
} 

---

## 자료형, 형식 지정자, 연산자

- bool : True, False, 1, 0, yes, no
- char : 문자 하나. 'a', 'Z', '?', 'y', 'n'
- string : 문자열
- int : 특정 크기 또는 특정 비트까지의 정수 (대략 40억까지 셀 수 있음)
- long : 더 큰 크기의 정수
- float : 실수. 3.14, 0.0, -28.5
- double : 더 큰 실수

### get_자료형 함수
- get_char
- get_double
- get_float
- get_int
- get_long
- get_string

### 형식 지정자
- %c : char
- %f : float, double
- %i : int
- %li : long
- %s : string

## 기타 연산자
- + - * /(나누기) %(나머지) &&(그리고) ||(또는) //(주석)

// 주석은 이렇게 답니다.

```
# include <cs50.h>
# include <stdio.h>

int main(void)
{
    int age = get_int("What's your age?\n");
    printf("Your are at least %i days old.\n", age * 365);
}
```
```
# include <cs50.h>
# include <stdio.h>

int main(void)
{
    float price = get_float("What's the price?\n");
    printf("Your total is %f\n", price*1.0625);
}
```

짝수인지 홀수인지 알려주는 코드 짜기
```
# include <cs50.h>
# include <stdio.h>

int main(void)
{
    int n = get_int("n : ");

    if (n % 2 == 0)
    {
        printf("even\n");
    }

    else // 짝수가 아니면 홀수니까 else로만 적어도 된다.
    {
        printf("odd\n")
    }
}
```