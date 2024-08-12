# DATA-STRUCTURE-AN-ALGORITHEM



#include <stdio.h>
#include<stdlib.h>
#define MAX_SIZE 5 //SIZE OF std::array<, N> ;

int top =-1;
int stack[MAX_SIZE];

void push(int item) {
	if(item==MAX_SIZE-1) {
		printf("overflowed! & Exit\n");
	} else {
		stack[++top]=item;

		printf("%d item inserted\n",item);
	}
}
void pop() {
	if(top==-1) {
		printf("stack is underflow\n");
	} else {
		int item = stack[top--];
		printf("%d item deleted\n",item);
	}
}

void peek() {
	if(top==-1) {
		printf("stack is empty\n");

	} else {
		for(int i =0; i<=top; i++) {
			printf("%d is element of stack\n",stack[i]);
		}
		printf("\n");

	}
}


int main()
{
	int choice,item ;
	printf("1.push\n2,pop\n3.display\n4.exit\n");
	
	while(1) {

		printf("enter the choice");
		scanf("%d",&choice);

		switch(choice) {
		case 1:
			printf("enter value to push");
			scanf("%d",&item);
			push(item);
			break;

		case 2:
			pop();
			break;

		case 3:
			peek();
			break;

		case 4:
		printf("program exit");
			return 0;
			break;

		default:
			printf("invalid input");
		}

	}



	return 0;
}
