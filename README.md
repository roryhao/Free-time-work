# Free-time-work
程式作品
## 1.分數計算
```c
#include <stdio.h>
int main()
{
    int a;
    scanf("%d",&a);
    if(a<=60 && a>30)printf("%d分 呵呵~該下去囉~",a);
    else if(a<=30 && a>0)printf("%d分 準備重補修",a);
    else if(a==0)printf("%d分 來世再相見...",a);
    else printf("%d分 恭喜你!!開心放假去",a);
}
```
## 2.列乘行
```c
#include <stdio.h>
int main()
{
    int a[10][10],b[10][10],c[10][10];
    int i,j,k,n;
    scanf("%d",&n);
    for(i=0;i<n;i++)
        for(j=0;j<n;j++)
            scanf("%d",&a[i][j]);
    for(i=0;i<n;i++)
        for(j=0;j<n;j++)
            scanf("%d",&b[i][j]);
    for(i=0;i<n;i++)
        for(j=0;j<n;j++)
            {
             c[i][j]=0;
             for(k=0;k<n;k++)
                c[i][j]+=a[i][k]*b[k][j];
            }
    for(i=0;i<n;i++)
    {
        for(j=0;j<n;j++)
            printf("%3d",c[i][j]);

        printf("\n");
    }
}
```
## 3.判斷閏年
```c
#include <stdio.h>
int main()
{
int a;
int year;
scanf("%d",&year);
a=(year % 400==0)||
(year % 4 ==0)&&(year % 100!=0);
printf("%d",a);
}
```
## 4.兩數相加
```c
#include <stdio.h>
int main()
{
 int a,b;
 printf("請輸入數字\n");
 scanf("%d%d",&a,&b);
 printf("a=%d,b=%d,a+b=%d\n",a,b,a+b);
}
```
## 5.泡泡排序法
```c
Q:輸入10位同學的成績(全整數)，並依照成績去計算由1到10計算排名
#include <stdio.h>
int main()
{
    printf("請輸入成績:");
    int a[10];
    for(int i=0;i<10;i++)
        scanf("%d",&a[i]);

    for(int j=0;j<10;j++)
    {
        for(int i=0;i<9;i++)
        {
            if(a[i]<a[i+1])
            {
                int temp=a[i];
                a[i]=a[i+1];
                a[i+1]=temp;
            }
        }
    }
    for(int i=0;i<10;i++)
    printf("第%2d名-%d分\n",i+1,a[i]);
}
```
## 6.計算三角體、錐體積與表面積
```c
#include <stdio.h>
int main()
{
    int a,b,c;
    scanf("%d%d%d",&a,&b,&c);
    printf("表面積:%d\n",(a*b)*4);
    printf("體積:  %d\n",(a*b)*c);
    printf("此為三角錐\n");
    printf("********************\n");
    printf("表面積:%d\n",(a*b)*2+(a*c)*3);
    printf("體積:  %d\n",(a*b)*c);
    printf("此為三角柱");
}
```
## 7.解碼器
```c
#include <stdio.h>
int main()
{
    char line[]="0100101101010101010011101000011010010000100100101000001010010000100000101001111";
    int ans=0;
    for(int i=0;i<80;i++)
    {
        char c=line[i];
        ans=ans*2;
        if(c=='1')ans+=1;
        if(c=='0')ans+=0;
        if(i%8==7)
        {
            printf("%c",ans);
            ans=0;
        }
    }
}
```
## 8.數字決定運勢
```c
#include <stdio.h>
int main()
{
    int a;
    printf("請在1~3當中選擇一個你喜歡的數字\n");
    a=getchar();

    switch(a)
    {
    case '1':
        printf("小吉\n");
        break;
    case '2':
        printf("中吉\n");
        break;
    case '3':
        printf("大吉 \n");
        break;
    default:
        printf("輸入錯誤!! = =\n");
    }
}
```
## 9.數值交換
```c
#include <stdio.h>
int main()
{
    int a,b;
    printf("請輸入數字\n");
    scanf("%d",&a);
    scanf("%d",&b);
    int temp=a;
    a=b;
    b=temp;
    printf("a:%d,b:%d\n",a,b);
}
```
## 10.簡答問題
```c
#include <stdio.h>
int main()
{
char a;
printf("張容齊是一個怎樣的人?\n");
printf("A 智障\n");
printf("B 白目\n");
printf("C 優雅\n");
printf("D 帥氣\n");
scanf("%c",&a);
if(a=='A')printf("請多多關照!");
else if(a=='B')printf("請多多包含!");
else if(a=='C')printf("你在跟我開玩笑嗎?");
else if(a=='D')printf("不要瞎掰好嗎!");
}
```
