# 2021week-2
##第一題
讀入整數反序列印 : 設計一個程式，該程式可以連續讀入正整數(輸入0表示結束，至多不超過10個正整數)，之後將所輸入的正整數以相反序顯示在畫面上。 
數字範圍：整數 1 – 1000 
```C
#include <stdio.h>
int a[50];
int main()
{
	int n=0;
	for(int i=0;i<11;i++)
	{
	
		scanf("%d",&a[i]);
		
		
		if(a[i]==0)
		{
			n=i;
			break;
		}	
	}
	
	for(int i=n-1 ; i>=0 ; i--) 
	{
		printf("%d ", a[i]);
	}
			
	printf("\n");
	
}
```
##第二題
A的B次方函數 : 
題目名稱：A的B次方函數
題目內容：請撰寫一個函數MYPOWER(A,B)，可以計算A^B結果。
數字範圍：整數 1 – 9。
程式限制：不得使用power()函數。不得變更已給定的主程式。
主程式：
```C
int main(void)
{
	int a,b;
	scanf("%d%d",&a,&b);
	printf("[%d]",MYPOWER(a,b));
	return 0;
}
```

```C
#include <stdio.h>
int MYPOWER(int a,int b);
int main(void)
{
	int a,b;
	scanf("%d%d",&a,&b);
	printf("[%d]",MYPOWER(a,b));
	return 0;
}

int a,b,i;	
int MYPOWER(int a,int b)
{
	int s;
	for(i=1;i<=b;i++)
	{
		//a=a*a;
		if(i==b)
		break;
		s*=a;
	}
	
	
		
	return s;
}
```
##第三題
漸增數列相加 : 輸入正整數n，計算1*2+2*3+3*4+…+(n-1)*n之和。 
數字範圍：整數1 – 1000 
```C
#include <stdio.h>
int main()
{
	int n,q,i,s,w=0;
	scanf("%d",&n);
	for(i=1;i<=n-1;i++)
	{
		q=i+1;
		s=i*q;
		w+=s;
	}
	printf("%d\n",w);
	
	
	
	return 0;
}
```

##第四題
判別正方形 : 撰寫一個程式要求使用者輸入矩形的長與寬，然後讀進這兩個整數。假如長與寬相同則印出訊息「It is a square」，否則印出訊息「It is not a square」。只能使用本章所學到的單一if敘述式。
```C
#include <stdio.h>
int main()
{
	int a,b;
	scanf("%d %d",&a,&b);
	printf("Enter two numbers: ");
	if(a==b)
	{
		printf(" It is a square ");
	}
	else
		printf(" It is not a square ");
	
	
	return 0;
}
```

##第五題
2進位轉10進位 : 讀入一個0000 ~ 1111的2進位整數(固定4位數)，請顯示出對應的10進位數字。 
數字範圍：0000 – 1111 
```C
#include <stdio.h>
int main()
{
	int a,s=0;
	scanf("%d",&a);
	if(a%10==1)
	{
		s+=1;
	}	
	a/=10;
	if(a%10==1)
	{
		s+=2;
	}	
	a/=10;
	if(a%10==1)
	{
		s+=4;
	}	
	a/=10;
	if(a%10==1)
	{
		s+=8;
	}	
	printf("%d\n",s);
	
		
	
	
}
```

##第六題
均標與前標計算 : 輸入整數N, 再輸入N個同學的分數, 計算並且輸出均標(float 小數點後一位數), 均標是全部學生的平均分數, 再計算並且輸出前標(float 小數點後一位數), 本題的前標是大於或等於均標的同學的平均分數.
```C
#include <stdio.h>
int a[80],n,i,j;
double q,t,r,e,x;
int main()
{
	
	scanf("%d",&n); 
	for(i;i<n;i++)
	{
		scanf("%d ",&a[i]);
		x+=a[i];
		
	}
	q=x/n;
	for(j=0;j<n;j++)
	{
		if(a[j]>=q)
		{
			r+=a[j];
			e++;
		}
			
	}
	t=r/e;

	
	printf("均標:%.1f\n",q);
	printf("前標:%.1f\n",t);
	
	return 0;
}
```
