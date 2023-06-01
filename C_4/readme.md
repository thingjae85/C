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
# 2023-05-04 10주차 C언어 수업
```c
#include <stdio.h>
int main(){
    for(int i=1;i<=5;i++){
        for(int k=5;k>i;k--){
            printf(" ");
        }
        for(int x=0;x<i;x++){
            printf("*");
        }
        printf("\n");
    }
    return 0;
}
```
```c
#include<stdio.h>
int get_integer(void)
{
int value;
printf("정수를 입력하시오: ");
scanf_s("%d", &value);
return value;
}
int add(int x, int y){
    return x+y;
}
int minus(int x, int y){
    return x-y;
}
int div(int x, int y){
    return x/y;
}
int multi(int x, int y){
    return x*y;
}
int main(){
    int x=get_integer();
    int y=get_integer();
    int z=add(x,y);
    printf("두수의 합은 %d입니다.\n",z);
    z=minus(x,y);
    printf("두수의 차는 %d입니다.\n",z);
    z=multi(x,y);
    printf("두수의 곱은 %d입니다.\n",z);
    z=div(x,y);
    printf("두수를 나눈값은 %d입니다.",z);
    return 0;
}
```
```c
#include<stdio.h>
int main(){
    int x,y;
    int z=1;
    printf("알고싶은 팩토리얼의 값은?:");
    scanf_s("%d",&x);
    for(y=1;y<=x;y++){
        z*=y;
    }
    printf("%d!의 값은 %d 입니다.",x,z);
    return 0;
}
```
```c
#include<stdio.h>
int wornl(int x){
    if(x==1){
        return 1;
    }
    else{
        return x * wornl(x-1);
    }
}
int main(){
    int x;
    printf("알고싶은 팩토리얼의 값은?:");
    scanf_s("%d",&x);
    int z=wornl(x);
    printf("%d!의 값은 %d 입니다.",x,z);
    return 0;
}
```
# 2023-05-11 11주차 c언어 수업
```c
#include<stdio.h>
int solution(int x, char *y){
    int answer=0;
if(y=="S"){
    answer=x*0.95;
}
if(y=="G"){
    answer=x*0.9;
}
if (y=="V")
{
   answer=x*0.85;
}

return answer;
}

int main(){
    int price=96900;
    char *grade="S";
    int rkqt=solution(price, grade);
    printf("할인된 값은: %d입니다.",rkqt);

}
```
# 2023-05-18 12주차 c언어 수업
```c
//미완성임 집가서 완성시키기.
#include<stdio.h>
int main()
{  
    int a,b,c;
    while(1){
   printf("구간의 처음과 끝을 입력하세요:");
   scanf_s("%d %d",&a,&b);
   if((a>=2&&a<=9)&&(b>=2&&b<=9)){  
       break;    
   }
   else{
    printf("INPUT ERROR!\n");
   }
    }
    if(a<b){
   for(int i=1;i<=9;i++){
    for{

    }
   } 
    }
}
```
# 2023-05-25 13주차 c언어 수업
```c
#include <stdio.h> 
int main() {
  int a, b, c;
  int sum;
  int count;
  int ar[10] = {0};
  printf("값을 입력하세요: ");
  scanf("%d %d %d", &a, &b, &c);
  sum = a * b * c;
  while (1) {
    count = sum % 10;
    ar[count] += 1;
    sum /= 10;
    if (sum == 0) {
      break;
    }
  }
  for (int i = 0; i < 10; i++)
    printf("%d\n", ar[i]);

  return 0;
}
```
```c
#include <stdio.h> 
int main() {
  int i = 10;
char c = 69;
float f = 12.3;
printf("i의 주소: %p\n", &i); 
printf("c의 주소: %p\n", &c); 
printf("f의 주소: %p\n", &f); 
return 0;
}
```
```c
#include <stdio.h> 
int main() {
int i = 10;
double f = 12.3;
int* pi = NULL;
double* pf = NULL;
pi = &i;
pf = &f;
printf("%p %p \n", pi, &i);
printf("%p %p \n", pf, &f);
return 0;
}
```
# 2023-06-01 14주차 c언어 수업
```c
#include <stdio.h>
#include <string.h>
int main() {
  char arr[10000];
  int a=0;
  int b=0;
  scanf_s("%s", arr);
  for (int x = 0; x < strlen(arr); x++) {
    if (arr[x] == 'K' && arr[x + 1] == 'O' && arr[x + 2] == 'I') {
      a++;
    }
    if (arr[x] == 'I' && arr[x + 1] == 'O' && arr[x + 2] == 'I') {
      b++;
    }
  }
  printf("%d\n", a);
  printf("%d",b);
}
```
