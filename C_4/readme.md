# 2023-03-23 4주차 c언어 수업
```c
#include<stdio.h>
int main()
{
    int x,y,a;
    scanf_s("%d",&x);
    scanf_s("%d",&y);
    a=x*(y%10);
    printf("%d\n",a);
    a=x*((y/10)%10);
    printf("%d\n",a);
    a=x*(y/100);
    printf("%d\n",a);
    printf("%d",x*y);
    return 0;
}
```
# 2023-03-30 5주차 c언어 수업
```c
#include <stdio.h>
int main()
{
 int a,b;
 scanf("%d %d",&a,&b);
 if(a>b){
    printf(">");
 }
 else if(a<b){
    printf("<");
 }

 else if(a==b){
    printf("==");
 }

 return 0; 
}
```
```c
#include <stdio.h>
int main(void)
{   int a,b,d;
    char c;
    printf("수식을 입력하시오(예2 + 5)>>");
    scanf("%d %c %d",&a,&c,&b);
    switch (c)
    {
    case'+':
        d=a+b;
        break;
    case'/':
        d=a/b;
        break;
    case'-':
        d=a-b;
        break;
    case'*':
        d=a*b;
        break;
    case'%':
        d=a%b;
        break;                
    default:
        printf("지원되지 않는 수식입니다.");
        break;
    }
    printf("%d %c %d = %d \n", a, c, b,d);

return 0; 
    }
```
# 2023-04-06 6주차 c언어 수업
```c
#include<stdio.h>
#include <stdlib.h>
int main()
{
    int a,b,c;
    srand((unsigned)time(NULL)); 
    int answer = rand()%100;
    do{
       printf("예상 숫자를 입력하십시오: ");
       scanf_s("%d",&a);
         b++;
       if(a<answer){
         printf( "숫자가 낮습니다.\n");
       }
       if(a>answer){
        printf("숫자가 높습니다.\n");
       }
    }while (a!=answer);

    printf("축하합니다! 정답입니다.\n");
    printf("당신의 시도 횟수: %d",b);

    return 0;

}
```
```c
#include<stdio.h>
int main()
{
   int a,b,c;
   scanf_s("%d",&a);
   for(int i=0;i<a;i++){
    scanf_s("%d %d",&b,&c);
    printf("%d\n",b+c);
   }
  return 0; 
}
```
