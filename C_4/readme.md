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
