#include<stdio.h> 
#include<conio.h> 
int main()
{
	char com[30]; 
	int i=2,a=0; 
	printf("\n Enter comment:");
	gets(com); 
	if(com[0]=='/') 
	{
		if(com[1]=='/')
			printf("\n It is a comment"); 
		else if(com[1]=='*') 
		{		
			for(i=2;i<=30;i++)
			{
				if(com[i]=='*'&&com[i+1]=='/')
				{
					printf("\n It is a comment"); 
					a=1; 
					break;	
				}
				else 
					continue; 
			} 
			if(a==0)
				printf("\n It is not a comment");
		}
		else
			printf("\n It is not a comment");
	}
	else 
		printf("\n It is not a comment");
}![Screenshot 2024-01-29 130818](https://github.com/Sai918222/compiler-design/assets/113423387/d09480cd-3d5a-413d-9841-5ca04660b722)

