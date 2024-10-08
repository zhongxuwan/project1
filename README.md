# project1
```
#include<stdio.h>
#include<stdint.h>
#include<inttypes.h>
int main(void) {

	//指针的算术运算一般用于数组之中
	int32_t arrays[] = { 10, 20 ,30,40,50,60,70,80,90,100 };

	int32_t* ptr = arrays;					//此时不加下标意味着将数组中的一个数的地址给它
	
	//size_t为无符号整型，专门用来表示长度，大小
	size_t arrays_size = sizeof(arrays) / sizeof(arrays[0]);

	puts("输出原始数据：");
	for (size_t i = 0; i < arrays_size; ++i)
	{
		printf("%" PRId32 " ", arrays[i]);

	}
	printf("\n");

	//通过指针增加数组每个元素的值
	for (size_t i = 0; i < arrays_size; ++i)
	{
		*(ptr + i) += 5;
	}
	printf("修改后的数组:\n");
	for (size_t i = 0; i < arrays_size; ++i)
	{
		printf("%" PRId32 " ", *(ptr + i));

	}
	printf("\n");
	return 0;
}
```
