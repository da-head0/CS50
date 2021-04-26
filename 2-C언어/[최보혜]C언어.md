# C언어

## 1. 기본형식
```C
#include <stdio.h>

int main(void)
{
    printf("hello, world\n"); # printf에서 f는 형식화된 출력을 하겠다는 의미
}
```
- 글자나 단어, 문장을 적을 때는 언제나 텍스트에 "" 쌍따옴표를 감싸야 한다. (e.g "hello,world")
- 한 줄의 코드를 마칠 때마다 ;(세미콜론) 붙이기
- \n은 줄바꿈 기능
- python파일이 .py 인것처럼 C는 .c

## 2. Compiler
우리가 작성한 코드를 실제 실행시켜주는 작업을 'Compiler(컴파일러)'라고 한다.
![](2021-04-20-20-51-50.png)
- 파이썬 파일을 실행할 때, cmd창에서 'python 파일명.py'를 했던 것처럼 c 파일을 실행할 때에는 'clang 파일명.c'를 하면 된다.

## 3. 문자열과 숫자형
- String: 단어나 구절, 문장을 부르는 말
- C에서 변수를 저장할 때 데이터의 종류를 아주 정확하게 명시해야 한다.
- string을 변수에 저장할 때, string을 **형식지정자**라고 한다.
- 사용자의 이름을 입력으로 받아 변수에 저장하고 출력하는 방법
    ```C
    #include <stdio.h>

    int main(void)
    {
        string answer = get_string("What's your name?\n");
        printf("hello, %s\n", answer)
    }
    ```

- 변수에 숫자를 저장하고 싶을 때, ```int 변수명 = 숫자;```
  ```C
  #include <stdio.h>
  
  int main(void)
  {
      int counter = 0;
  }
  ```
- counter에 +1을 하고 싶을 때 방법
  1. counter = counter + 1;
  2. counter += 1;
  3. counter++;

## 4. 조건문과 루프
- 조건문을 작성할 때 끝에 세미콜론을 붙이지 않는다.
```C
# include <stdio.h>

int main(void)
{
    if (x<y)
    {
        printf("x is less than y\n");
    }
    else if (x==y)
    {
        printf("x if equal to y\n")
    }
    else
    {
        printf("x is not less than y\n")
    }
}
```

- while이나 for문을 통해 loop를 구현할 수 있다.
```C
# include <stdio.h>

int main(void)
{
    int i = 0;
    while (i<50)
    {
        printf("Yes!\n")
        i +=1
    }

    for (int j=100; j>50; j = j-1 )
    {
        print("hello, world\n")
    }
}
```

## 5. 자료형, 형식 지정자, 연산자
### 데이터 타입
- bool: 불리언 표현, (예) True, False, 1, 0, yes, no
- char: 문자 하나 (예) 'a', 'Z', '?'
- string: 문자열
- int: 특정 크기 또는 특정 비트까지의 정수 (예) 5, 28, -3, 0
- long: 더 큰 크기의 정수
- float: 부동소수점을 갖는 실수 (예) 3.14, 0.0, -28.56
- double: 부동소수점을 포함한 더 큰 실수

### 형식 지정자
- %c : char
- %f : float, double
- %i : int
- %li : long
- %s : string

### Get 함수
- get_char
- get_double
- get_float
- get_int
- get_long
- get_string

## 6. 사용자 정의 함수
- 사용자 정의 함수는 사용자가 원하는 특정기능을 구현시킨 함수이다.
- 사용자 정의 함수를 통해 가독성을 높일 수 있다.
- 사용자 정의 함수는 보통 main함수 아래에 사용한다. 단, 함수명을 맨 위에 적어줘야 한다.

```C
#include <stdio.h>
void cough(void)
int get_positive_int(void)

int main void()
{
    for (int i=0; i<3; i++)
    {
        cough();
    }
}

//첫번째 사용자 정의 함수
void cough(void)
{
    printf("cough\n");
}

//두번째 사용자 정의 함수
int get_positive_int(void) //입력은 없으나 output으로 int형식 출력
{
    int n;
    do
    {
        n = get_int("Positive Integer: ");
    }
    while (n<1);
    return n;
}
```

## 7. 하드웨어의 한계