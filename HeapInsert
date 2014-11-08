#include<stdio.h>
typedef struct node
{
	int size;
	int elements[100];
}priorityQueue;
typedef priorityQueue *pq;
int main()
{
	int a;
	pq H;
	H = (priorityQueue *)malloc(sizeof(priorityQueue));
	H->size = 0;
	
	printf("Please insert a series of numbers:\n");
	
	while(scanf("%d", &a)!=EOF)
		insert(a, H);
	for(a = 1; a <= H->size; a++)
		printf("%d ", H->elements[a]);
	return 0;
}
int insert(int x, pq Hi)
{
	int i;
	i = 0;
	
	for( i = ++Hi->size; Hi->elements[i/2]>x; i/=2)
	{
		Hi->elements[i] = Hi->elements[i/2];
		if (i == 1)
			break;
	}
	Hi->elements[i] = x;
	
	return 0;
}
