# Questions
#question one :
想尝试一个转置函数

#include <stdio.h>

int transpose(int ,int,int );

int main(void)
{
	int i,j;
	int a[4][5]={
		{1,2,3,4,5},
		{5,4,3,2,1},
		{6,7,8,9,10},
		{10,9,8,7,6},
	};
	int aT[5][4]={};
	
	aT[5][4]=transpose(a[4][5],4,5);
	
	for (i=0;i<5;i++) {
		for (j=0;j<4;j++) {
			printf("%d",aT[i][j]);
			printf(" ");
		}
		printf("\n");
	}
	return 0;
}

int transpose (int b,int x,int y) 
{
	int i;
	int j;

	int bT[y][x]={0};
	
	for  (i=0;i<x;i++) {
		for (j=0;j<y;j++) {
			bT[i][j]=b[j][i];
			//printf("%d",aT[i][j]);
			//printf(" ");
		}
		//printf("\n");
	}

	return bT;
}

//为什么会出现这个报错？如何修改？
//[Error] invalid conversion from 'int (*)[x]' to 'int' [-fpermissive] 转换无效？ 
