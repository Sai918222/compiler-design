#include <stdio.h>
int main()
{
    char str[100];//input string with size 100

    int words=0,newline=0,characters=0; // counter variables

    scanf("%[^~]",&str);//scanf formatting    

    for(int i=0;str[i]!='\0';i++)
     { 
         if(str[i] == ' ')
         { 
              words++;
         }
         else if(str[i] == '\n')
         {
             newline++;
              words++;//since with every next line new words start. corner case 1
         }
         else if(str[i] != ' ' && str[i] != '\n'){
         characters++;
         }
     }
    if(characters > 0)//Corner case 2,3.
    {
        words++;
        newline++;
    }
     printf("Total number of words : %d\n",words);
     printf("Total number of lines : %d\n",newline);
     printf("Total number of characters : %d\n",characters);
    return 0;
}

![Screenshot 2024-01-29 132911](https://github.com/Sai918222/compiler-design/assets/113423387/8ab6f7ff-2f1b-41be-be4a-466abf3b299b)
