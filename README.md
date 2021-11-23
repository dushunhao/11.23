#define _CRT_SECURE_NO_WARNINGS

#include<stdio.h>

int main()

{

	const char* pstr = "hello bit.";
	printf("%s\n", pstr);
	return 0;
  
}

int main()

{

	int a[5] = { 1,2,3,4,5 };
	int b[] = { 2,3,4,5,6 };
	int c[] = { 3,4,5,6,7 };

	int* arr[] = { a,b,c };
	int i = 0;
	int j = 0;
	for (i = 0; i < 3; i++)
	{
		for (j = 0; j < 5; j++)
		{
			//printf("%d ", *(arr[i] + j));
			printf("%d ", arr[i][j]);
		}
		printf("\n");
	}
	return 0;
  
}

void print(int(*p)[5], int r, int c)

{

	int i = 0;
	int j = 0;
	for (i = 0; i < 3; i++)
	{
		for (j = 0; j < 5; j++)
		{
			printf("%d ", *(*(p + i) + j));
		}
		printf("\n");
	}
}
int main()

{

	int arr[3][5] = { {1,2,3,4,5},{2,3,4,5,6},{3,4,5,6,7} };
	print(arr, 3, 5);
	return 0;
  
}

void print(int* p, int sz)

{

	int i = 0;
	for (i = 0; i < sz - 1; i++)
	{
		printf("%d ", *(p + i));
	}
}
int main()

{

	int arr[10] = { 1,2,3,4,5,6,7,8,9 };
	int* p = arr;
	int sz = sizeof(arr) / sizeof(arr[0]);
	print(p, sz);
	return 0;
  
}

#include<stdio.h>

int main()

{

    int r = 0;
    int c = 0;
    scanf("%d %d", &r, &c);
    int i = 0;
    int j = 0;
    int arr[100][100];
    for (i = 0; i < r; i++)
    {
        for (j = 0; j < c; j++)
        {
            scanf("%d", &arr[i][j]);
        }
    }
    int sum = 0;
    for (i = 0; i < r; i++)
    {
        for (j = 0; j < c; j++)
        {
            if (arr[i][j] >= 0)
            {
                sum += arr[i][j];
            }
        }
    }
    printf("%d\n", sum);
    
    return 0;
    
}
