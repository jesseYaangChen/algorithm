# algorithm
算法
#include<stdlib.h>
#include <stdio.h>
void swap(int *a, int *b)
{
	int temp;
	temp = *a;
	*a = *b;
	*b = temp;

}
////效率低的冒泡排序
//void main1()
//{
//	int a[10] = { 5,8,9,11,22,55,3,556,7,70 };
//	for (int i =0; i < 10; i++)
//		for (int j = i+1; j < 10; j++)
//		{
//			if (a[i] > a[j])
//			{
//				swap(&a[i], &a[j]);
//			}
//		}
//	for (int i = 0; i < 10; i++)
//	{
//		printf("%d ", a[i]);
//	}
//	printf("\n");
//	system("pause");
//}

////优化1
//void main()
//{
//	int a[10] = { 5,8,9,11,22,55,3,556,7,70 };
//	for (int i = 0; i < 10; i++)
//		for (int j = 8 ; j >= i; j--)
//		{
//			if (a[j] > a[j+1])
//			{
//				swap(&a[j], &a[j+1]);
//			}
//		}
//	for (int i = 0; i < 10; i++)
//	{
//		printf("%d ", a[i]);
//	}
//	printf("\n");
//	system("pause");
//}

//更优化，解决原本排好顺序

void main()
{
	//int a[10] = { 5,8,9,11,22,55,3,556,7,70 };
	//int a[10] = { 2,1,3,4,5,6,7,8,9,10 };
	int a[10] = { 2,3,1,4,5,6,7,8,9,10 };
	bool A = true;
	for (int i = 0; i < 10&&A; i++)
	{
		A = false;
		for (int j = 8; j >= i; j--)
		{
			if (a[j] > a[j + 1])
			{
				swap(&a[j], &a[j + 1]);
				A = true;
			}
		}
	}
		
	for (int i = 0; i < 10; i++)
	{
		printf("%d ", a[i]);
	}
	printf("\n");
	system("pause");

}
