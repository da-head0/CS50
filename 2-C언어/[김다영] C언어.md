
## 2. C

### 1) C 기초
- 아주 오래되고 전통적인 순수 텍스트 기반의 언어

```C
#include <stdio.h>

int main(void)
{
  printf("Hello World");
}
```
+ printf() : 형식화된 텍스트 출력
  + 괄호 안에 글자나 단어, 문장을 적을 때는 언제나 그 텍스트를 쌍따옴표(" ")로 감싸야 한다.
+ 코드를 마칠 때는 세미콜론(;)을 꼭 붙여야 한다.
+ 프로그램명.c : C언어 파일
+ \n : 줄바꿈

#### 컴파일러
- 작성한 소스코드를 2진수로 작성된 “머신 코드”로 변환해야 컴퓨터가 이해할 수 있는데 이 작업을 컴파일러가 수행한다.

### 2) 문자열
#### String
- 단어나 구절, 문장을 부르는 말(숫자와는 다른 종류의 데이터)

```C
string answer = get_string("What's your name?\n");
printf("hello, %s\n", answer);
```
+ get_string : 어떤 입력을 받기 위한 함수
+ answer : 데이터를 저장할 변수
+ C언어는 오래된 언어이기 때문에 변수가 저장하는 데이터의 종류를 정확하게 명시(string answer)해줘야 한다.
+ 프로그래밍에서 = 은 같다는 뜻이 아니라 지정한다라는 뜻 -> 오른쪽의 내용을 왼쪽에 저장한다.
+ %s : 입력값이 들어갈 형식 지정자

### 3) 조건문과 루프
```C
int counter = 0;
counter = counter + 1;
```
+ int : 정수형 변수 counter를 선언
+ int counter = 0 : counter 변수를 0으로 초기화
+ counter = counter + 1 : counter에 1을 더한 값을 다시 counter에 저장한다.
  + counter += 1;, counter++; 으로 간결하게 작성할 수 있다.

#### if 조건문
- == : 일치 연산자 (= 할당연산자와 다름)
- if, else if, else문
```C
if(x < y)
{
    printf("x is less than y\n");
}
else if(x > y)
{
    printf("x is greater than y\n");
}
else
{
    printf("x is equal to y\n");
}
```


#### 루프
##### while 반복문
```C
while(true)
{
    printf("hello world\n");
}
```
+ while(true) : 영원히 반복하는 무한루프

```C
int i = 0;

while(i < 50)
{
    printf("hello world\n");
    i = i + 1; (i++;)
}
```
+ while(i < 50) : i가 50미만이면 반복문을 계속 진행
+ i = i + 1 : i 값 1씩 증가 

##### for 반복문
- 주어진 일을 계속해서 반복하지만 훨씬 더 기계적
```C
for(int counter = 0; i < 50; i++)
{
    printf("hello world\n");
}
```
### 4) 자료형, 형식 지정자, 연산자 
##### 데이터 타입
- bool : 불리언 표현, 예) True, False, 1, 0, Yes, No
- char : 문자 하나, 예) 'a', 'z'
- string : 문자열
- int : 특정 크기 또는 특정 비트까지의 정수, 예) 5, 28, -3, 0
- long : 더 큰 크기의 정수
- float : 부동소수점을 갖는 실수, 예) 3.14, 0.0
- double : 부동소수점을 포함한 더 큰 실수

##### 형식 지정자
- %c : char
- %f : float, double
- %i : int
- %li : long
- %s : string

##### 연산자
- '+' : 더하기
- '-' : 빼기
- '*' : 곱하기
- '/' : 나누기
- '%' : 나머지
- '&&' : 그리고
- '||' : 또는
- '//' : 주석

### 5) 사용자 정의 함수, 중첩 루프
##### 사용자 정의 함수
- printf 반복
```C
#include <stdio.h>

int main(void)
{
    printf("cough\n");
    printf("cough\n");
    printf("cough\n");
}
```
- 루프 for 사용
```C
#include <stdio.h>

int main(void)
{
    for (int i = 0; i < 3; i++)
    {
        printf("cough\n")
    }
}
```
- 함수를 만들어 사용
```C
#include <stdio.h>
void cough(void);

int main(void)
{
    for (int i = 0; i < 3; i++)
    {
        cough();
    }
}

void cough(void)
{
    printf("cough\n")
}

```
+ C언어는 위에서 아래로 실행을 하기 때문에 함수를 main문 아래에 구현하면 위에 선언을 해줘야한다.
+ main문을 아래에 쓰는 것보다 위에 쓰는 것이 좋음.

##### 중첩 루프

```C
#include <stdio.h>

int main(void)
{
    int n;

    do
    {
        n = get_int("Size: ");
    }
    while (n < 1);

    for (int i = 0; i < n; i++)
    {
        for (int j = 0; j < n; j++)
        {
            printf("#");
        }
        printf("\n");
    }
}
```
+ for 루프를 두 번 중첩해서 돌면서 "#"을 출력.
+ 첫 번째 루프에서는 변수 i를 기준으로 n번 반복하고, 그 안의 내부 루프에서는 변수 j를 기준으로 n번 반복
+ 내부 루프에서는 “#”을 출력하고, 내부 루프가 끝날 때마다 줄바꿈을 수행.
+ 결과적으로, 가로가 n개, 세로가 n개인 “#”이 출력.
