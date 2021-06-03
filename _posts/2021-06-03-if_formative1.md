--- 
layout: single 
title: "조건문" 
toc: true 
toc_sticky: true 
toc_label: "페이지 주요 목차" 
--- 
### 01. 사주보기 
![saju](/assets/images/사주보기.jpg) 
~~~c
#include <stdio.h> 
int main(void) 
{ int year,month,day,result; 
  
 printf("당신의 사주를 봐드립니다.\n"); 
 printf("연도 월 일을 차례대로 입력하세요 : "); 
 scanf("%d,%d,%d",&year,&month,&day); 
  
 result=(year-month+day)%10; 
 if(result==0) 
 printf("당신의 사주는 대박입니다.\n");

 else 
 printf("당신의 사주는 그럭저럭입니다.\n"); 
 return 0; 
}
~~~ 
### 02. 3개의 터널 통과 
![tunnul](/assets/images/터널.jpg) 
~~~c 
#include <stdio.h> 
int main(void) 
{ int tunnul_1, tunnul_2, tunnul_3; 
 printf("세 터널의 높이를 차례대로 입력하세요 : "); 
 scanf("%d,%d,%d",&tunnul_1,&tunnul_2,&tunnul_3); 
 if(tunnul_1<=170) 
 printf("충돌 %d", tunnul_1); 
 else if(tunnul_2<=170) 
 printf("충돌 %d", tunnul_2); 
 else if(tunnul_3<=170) 
 printf("충돌 %d", tunnul_3); 
 else 
 printf("무사 통과"); 
 return 0; 
}
~~~ 
### 03. 이 달은 며칠까지 있을까? 
![callenderl](/assets/images/이달은.jpg) 
~~~c 
#include <stdio.h> 
int main(void) 
{ int year, month; 
  
 printf("연도와 월을 입력하세요 : "); 
 scanf("%d%d", &year, &month); 
 printf("%d년 %d월의 마지막날은 ", year, month); 
  
 if(month==1||month==3||month==5||month==7||month==8||month==10||month==12)  printf("31일"); 
 else if(month==4||month==6||month==9||month==11) 
 printf("30일"); 
 else 
 { 
 if((year%4==0 && year%100!=0) || year%400==0)

 printf("29일"); 
 else 
 printf("28일"); 
 } 
 printf("입니다.\n"); 
 return 0; 
}
~~~ 
### 04. 30분전
![time](/assets/images/형성평가4.jpg) 
~~~c 
#include <stdio.h>

int main(void) 
{
  int hour, min;
  printf("시간과 분을 입력하세요: ");
  scanf("%d %d", &hour, &min);
  printf("입력한 시간의 30분 전의 시간은 ");
  if(min>=30)
  printf("%d시 %d분\n", hour, min-30);
  else 
  {
    if(hour==0)
    printf("%d시 %d분\n", 23, min+30);

    else
    printf("%d시 %d분", hour-1, min+30);
  }
  //가장 먼저 기준을 잡아야 할것이 분이고 시간을 나눠서 들어갈 수 있어야 함
  
}
~~~
### 05. 중단원 정리 1번
![jungri](/assets/images/형성평가5.jpg) 
~~~c 
#include <stdio.h>

int main(void) 
{
  int money, remain;
  int book = 15000;
  
  printf("책의 가격은 15000원입니다.\n");
  printf("현재 용돈은?: ");
  scanf("%d", &money);
  if(money>=book)
  {printf("책 구입 성공\n나머지: %d", money-book);}
  else 
  printf("책 구입 실패");

}
~~~
