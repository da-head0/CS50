## c언어 기초

int main(void) ### 시작한다
{
    prinf("hello, world");
}

출력은 printf를 사용! 
#include<stdio.h>는 "stdio.h라는 이름의 파일을 찾아서 "printf" 함수에 접근할 수 있도록 해준다. 

### 컴파일러
source code -> complier -> machine code
우리가 직접 작성한 코드는 "소스 코드" 라고 불리며, 머신 코드로 변환해야 컴퓨터가 이해할 수 있는데. 이러한 작업을 컴파일러라는 프로그램이 수행해준다. 

## 문자열

string answer = get_string("What's your name?\n");

변수는 마음대로 정해도 무관.
하지만, 데이터의 종류를 정확하게 명시해주어야 한다. 
printf("hello, %s\n", answer);
-> answer변수에 저장한 사용자 이름을 출력하기 위해 %를 써주어야 하며,
string 의 s자를 따서 %s로 적어준다. 

