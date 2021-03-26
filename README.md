# 程式設計作業
## 2021/2/26

 NO.1 找零錢
```c
int a,b,c,d;
scanf("%d",&a);
printf("%d=",a);

b = a / 50; a = a % 50; c = a / 5; d = a % 5;
printf("50*%d+5*%d+1*%d\n",b,c,d);
```

 NO.2 找因數
```c
int a,ans=0;
scanf("%d",&a);
for(int i=1; i<=a; i++){
	int b=1;
	b = a % i;
	if(b == 0) ans+=1;
	}
printf("%d\n",ans);
```

 NO.3 找倍數
```c
int a,ans=0;
for(int i =0; i < 10; i++){
	scanf("%d",&a);
	if(a % 3 == 0) ans+=1;
}
printf("%d\n",ans);
```

 NO.4 成績等級
```c
int a,ans=0;
for(int i =0; i < 10; i++){
	scanf("%d",&a);
	if(a % 3 == 0) ans+=1;
}
printf("%d\n",ans);
```

 NO.5 分式化簡 (考試)
```c
int m,s,q=1;
scanf("%d%d",&s,&m);

for(int i=1; i<=s; i++){
	if(s % i == 0){
		if(m % i == 0) q=i;
	}
}

printf("%d %d\n",s/q,m/q);
```

## 2021/3/5

NO.1


## TEXT
大小月不分QQ

```c
#include <stdio.h>
int s[366];
int main()
{
    int N,M,D,q;
    scanf("%d",&N);
    //1.6 2.7 3.1 4.2 5.3 6.4 7.5
    for(int i=0; i<N; i++){
        scanf("%d",&M);
        if(M == 2 ){
            scanf("%d",&D);
            q=31+D;
            s[i]=q%7;

        }else if(M%2 == 0){
            scanf("%d",&D);
            q=59+D+((M-3)*30)+(M/2-1);
            s[i]=q%7;

        }else if(M == 1){
            scanf("%d",&D);
            s[i]=D%7;

        }else{
            scanf("%d",&D);
            q=59+D+((M-3)*30)+(M/2-1);
            s[i]=q%7;
        }
    }

    for(int i=0; i<N;i++){
        if(s[i]==1) printf("Saturday6\n");
        else if(s[i]==2) printf("Sunday7\n");
        else if(s[i]==3) printf("Monday1\n");
        else if(s[i]==4) printf("Tuesday2\n");
        else if(s[i]==5) printf("Wednesday3\n");
        else if(s[i]==6) printf("Thursday4\n");
        else printf("Friday5\n");
    }
}

```


