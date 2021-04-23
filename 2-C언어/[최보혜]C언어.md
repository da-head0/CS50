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

## 6. 사용자 정의 함수, 중첩 루프

## 7. 하드웨어의 한계