#include<stdio.h>
#include<conio.h>
main()
{
	int m, n, i, j, a[100][100], b[100][100], say, topla, k, c[100][100];
	printf("kacar satir:"); scanf("%d", &m);
	printf("kacar sütun:"); scanf("%d", &n);
	printf("A matrisini gir: ");
	for (i = 1;i <= m;i = i + 1)

	{
		for (j = 1;j <= n;j = j + 1) scanf("%d" &a[i][j]);
	}
	printf("B matrisini gir: ");
	for (i = 1;i <= m;i = i + 1)
	{
		for (j = 1;j <= n;j = j + 1) scanf("%d" &a[i][j]);
	}
	for (i = 1;i <= m;i = i + 1)
	{
		say = 0;
		for (j = 1;j <= n;j = j + 1)
		{
			topla = 0;
			for (k = 1; k <= 2; k = k + 1) topla = topla + a[i][k] * b[k][j];
			c[i][j] = topla;
			printf("%d", c[i][j]); say = say + 1;
			if (say == 2) printf("/n");
		}
	}
	getch();
}
