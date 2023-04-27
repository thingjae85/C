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
```c
#include<stdio.h>
int main()
{
   int a,b,c;
   scanf_s("%d",&a);
   for(int i=1;i<=a;i++){
    scanf_s("%d %d",&b,&c);
    printf("Case #%d:%d + %d = %d\n",i,b,c,b+c);
   }
}
```
# 2023-04-27 C언어 교안 연습문제들

```c
#include<stdio.h>

int main()
{   double light=300000;
    double d=1496000000;
    printf("빛의 속도는 %lfkm/s\n",light);
    printf("태양과 지구와의 거리 %lfkm\n",d);
    printf("도달 시간은 %lf초",d/light);
    return 0;
    
}

```
```c
#include<stdio.h>

int main()
{   
    int price,money,don;
    
    printf("물건 값을 입력하시오:");
    scanf_s("%d",&price);
    printf("투입한 금액을 입력하시오:");
    scanf_s("%d",&money);
    don=money-price;
    printf("천원권 %d장\n",don/1000);
    don=don%1000;
    printf("오백원 동전 %d개\n",don/500);
    don=don%500;
    printf("백원동전 %d개",don/100);
    return 0;
}
```
```c
#include <stdio.h>
int main()
{   
   int i=1;
   int n;

   printf("출력하고 싶은 단을 입력하시오: ");
   scanf_s("%d",&n);
   while (i<=9)
   {
     printf("%d * %d = %d\n",n,i,n*i);
     i++;
   }
   return 0;  
}
```
```C
#include<stdio.h>

int main()
{   

    int i, n, sum; 
    printf("정수를 입력하시오:"); 
    scanf_s("%d", &n);
    i = 1;
    sum = 0;
    while(i <= n)
    {  if(i%2==0){
        sum += i;
    }
            i++; 
    }
printf("1부터 %d까지의 합은 %d입니다\n", n, sum);
return 0; 
   
}
```
```c
#include<stdio.h>

int main()3
{   

    int i,n,sum; 
    i=0;
    sum=0;
   while (i<5)
   {
    printf("값을 입력하시오:");
    scanf_s("%d",&n);
    sum=sum+n;
    i++;
   }
   printf("합계는 %d입니다.",sum);
   return 0;
}

```
```c
#include<stdio.h>

int main()
{   

    int i,n,sum; 
    i=0;
    sum=0;
    n=1;
    printf("종료하려면 음수를 입력하시오\n");
   while (n>0)
   {
    printf("성적은 입력하시오:");
    scanf_s("%d",&n);
    sum=sum+n;
    i++;
   }
   sum=(sum-n)/(i-1);
   printf("평균은 %d입니다.",sum);
   return 0;
}
```
