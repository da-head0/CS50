# 2. C언어
## 1) C 기초
- `#include <stdio.h>`
  - 컴퓨터에게 함수가 어디에 구현되어있는지 혹은 어디에 저장되어 있는지를 알려줘야 하는데, 이 함수에 접근하기 위해서는 stdio.h라는 파일에 접근해야한다는 것을 알려주는 코드.

- 컴파일러
  - clang : 코드를 컴파일하는 프로그램 중 하나
  - 소스코드(프로그래밍 언어를 통해 작성한 코드)를 머신코드(2진수)로 변경해준다. 

## 2) 문자열
- 형식지정자
  > %d : 정수(10진수)<br>
  > %ld : 변수형 중 long형<br>
  > %c : 문자(문자 하나)<br>
  > %s : 문자열("apple" 같이 여러문자)<br>
  > %f : 실수(10진수, 11.34와 같이 소수점 이하에 값이 있는경우)<br>
  > %lf : 변수형 중 double형(8byte)<br>
  > %u : unsigned int 와 같이 부호없는 정수(10진수)<br>
  > %lu : unsigned long<br>
  > %x, %X, %lx, %lX : 부호없는(unsigned) 16진수<br>
  > %o, %lo : 부호없는 8진수<br>

-  C는 오래된 언어이기 때문에 변수가 저장하는 데이터의 종류를 아주 정확하게 명시해줘야 한다.
    -  string : 문자열
    -  ```string answer = get_string("What's your name?\n"); ```
    -  ```printf("hello, %s\n", answer);```


<img width="785" alt="Screen Shot 2021-04-24 at 1 43 39 PM" src="https://user-images.githubusercontent.com/69139242/115947516-17571500-a503-11eb-8dea-f7421f8b05e7.png">

    - `#include <cs50.h>` : get_string() 함수를 가져오기 위한 코드

- 컴파일
  > $ clang -o string string.c -lcs50
  - -lcs50은 “link”라는 의미를 지닌 -l 이라는 인자에 추가로 포함한 “cs50” 파일을 합친 것입니다. 이를 통해 컴파일시 cs50 파일을 연결하도록 알려줄 수 있다.<br><br>


  > $make string
  - 위의 명령어를 통해 간단하게 컴파일을 수행할 수도 있다.



## 3) 조건문과 루프
- int
  `int counter = 0;`
  - 변수가 정수형일 때

- if
```c
if (x < y)
{
  printf("x is less than y\n");
}
else if (x > y)
{
  printf("x is greater than y\n");
{
else
{
  printf("x is equal to y\n");
}
```

- while
```c
while (true)
{
  printf("hello, world\n");
}
```
```c
int i = 0;
while (i < 50(
{
  printf("hello, world\n");
  i++;
}
```

- for
```c
for (int i = 0; i < 50; i++)
{
  printf("hello, world\n");
}
```
  - for (①; ②; ④) { ③ }
  - 이 순서로 진행된다.



## 4) 자료형, 형식 지정자, 연산자
- datatype(자료형)
  - bool: 불리언 표현, (예) True, False, 1, 0, yes, no
  - char: 문자 하나 (예) 'a', 'Z', '?'
  - string: 문자열
  - int: 특정 크기 또는 특정 비트까지의 정수 (예) 5, 28, -3, 0
  - long: 더 큰 크기의 정수
  - float: 부동소수점을 갖는 실수 (예) 3.14, 0.0, -28.56
  - double: 부동소수점을 포함한 더 큰 실수

- int.c
```c
#include <cs50.h>
#include <stdio.h>

int main(void)
{
  int age = get_int("What's your age?\n");
  printf("You are at least %i days old.\n", age * 365);
}
```

- float.c
```c
#include <cs50.h>
#include <stdio.h>

int main(void)
{
  float price = get_int("What's the price?\n");
  printf("Your total is %.2f.\n", price * 1.0625);
}
```

- parity.c
```c
#include <cs50.h>
#include <stdio.h>

int main(void)
{
  int n = get_int("n: ");
  
  if (n % 2 == 0)
  {
    printf("even\n"); // 짝수
  }
  else
  {
    printf("odd\n"); // 홀수
  }
}
```

- 연산자
  - +:  더하기
  - -: 빼기
  - *: 곱하기
  - /: 나누기
  - %: 나머지
  - &&: 그리고
  - ||: 또는

- //: 주석

## 5) 사용자 정의 함수, 중첩 루프
## 6) 하드웨어의 한계
