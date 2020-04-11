#include<stdio.h>

#include<stdlib.h>

#include <time.h>



struct Object

{

	int pno;

}frames[7];



int faults=0;			

int i,p;

int n;	

int pno;		

int flag=0;




int page_found(int pno)

{

	for(i=0;i<n;i++)

	{

		if(frames[i].pno == pno)

			return i;	
      
	}

	return 'a';
  
}



int main()

{

	int len;					
  
	srand ( time(NULL));
  
	printf("Enter number of pages (b/w 0 to 9) :");

	scanf("%d",&len);

	if(len<0 || len>9)

	{

		printf("\nInput out of bounds.\n");

		exit(0);

	}



	int *arr = (int *)malloc(len*sizeof(int));
  
	

	for (int i=0;i<len;i++)

	{

		arr[i] = ( rand()%9 )+1 ;

	}

	printf("\nEnter no of frames (b/w 1 to 7) :");

	scanf("%d",&n);

	if(n<1 || n>7)

	{

		printf("\nInput out of bounds.\n");

		exit(0);

	}



	printf("Length:%d",len);



	for (i=0;i<n;i++)

	{

		frames[i].pno = -1;		
    
    
	}



	printf("\n Page no     page frames     page faults     fault count");

	printf("\n-----------------------------------------------------------");

	for(p=0;p<len;p++)

	{

		pno = arr[p];

		flag=0;
    
		if(page_found(pno) == 'a')			
    
		{
    
			frames[faults%n].pno = pno;

			faults++;

			flag=1;

		}

		printf("\n%5d\t",pno);

		printf("\t");

		for(i=0;i<n;i++)

			printf("%d ",frames[i]);



		if(flag==1)

			printf("\t\t YES");

		else

			printf("\t\t NO");



		printf("\t\t%d",faults);

	}

	printf("\n------------------------------------------------------------");

	printf("\nTotal page faults:%d", faults);

	printf("\n\n Exiting...\n\n");



	free(arr);
  
	return 0;

}
