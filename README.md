#define _CRT_SECURE_NO_WARNINGS
#include <stdio.h>
#include <stdlib.h>

/*
int main()

{
	int i,n,x,v[100];
	scanf("%d", &n);
	scanf("%d", &x);
	for (i=0;i<n;i++)
	{
		scanf("%d",&v[i]);
		if (v[i] == x)
		{
			printf("Nr. se afla in vector \n");
			break;
		}
	}
	system("Pause");
	return 0;

}
*/
int main()
{
	int i, st = 0, v[100], n, x,dr,mij=0;
	scanf("%d", &n);
	scanf("%d", &x);
	
	for (i = 0;i < n;i++)
		scanf("%d", &v[i]);
	dr = n;
	i = 0;
	while (st < dr)
	{
		mij = (st + dr) / 2;
		if (v[mij] == x)
		{
			printf("Nr. se afla in vector \n");
			break;
		}
		if (v[mij] > x)
			dr = mij-1;
		else
			st = mij+1;
	}
	
	system("Pause");
	return 0;

}
