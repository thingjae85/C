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
int main(void)
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
