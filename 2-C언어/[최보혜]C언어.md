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