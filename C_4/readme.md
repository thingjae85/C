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
