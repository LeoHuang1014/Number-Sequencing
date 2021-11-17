# Number-Sequencing
Sequence the number 


int main()
{
    int A[10] = {5,4,7,9,2,1,3,10,8,6}; //list the 10 numbers 
    int i,x,j;

    for (i=1;i<10;i++)  /*i round, 9 round*/
     {
          x=A[i];
         for (j=i-1;j>=0;j--)
         {
              if (A[j]>x)
                A[j+1]=A[j];
         
            else
              {
                  A[j+1]=x;
                  break;
              }
         }
         if(j<0)
               A[0]=x;     
    } 
     for (i=0;i<10;i++)
         printf("%d", A[i]);
     printf("\n");    
     return 0; 
}
