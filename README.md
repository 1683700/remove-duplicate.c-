#include <stdio.h>  
#include <conio.h>  
int main ()  
{  
     
    int arr[]={1, 2,3,2,1}; 
	int i, j, k, n;  
    n=sizeof(arr)/sizeof(arr[0]) ; 
    for ( i = 0; i < n; i ++)  
    {  
        for ( j = i + 1; j < n; j++)  
        {  
            // use if statement to check duplicate element  
            if ( arr[i] == arr[j])  
            {  
                // delete the current position of the duplicate element  
                for ( k = j; k < n - 1; k++)  
                {  
                    arr[k] = arr [k + 1];  
                }  
                
                n--;  
                  
            // if the position of the elements is changes, don't increase the index j  
                j--;      
            }  
        }  
    }  
      
      
    /* display an array after deletion or removing of the duplicate elements */  
    printf (" \n Array elements after deletion of the duplicate elements: ");  
      
    // for loop to print the array  
    for ( i = 0; i < n; i++)  
    {  
        printf (" %d \t", arr[i]);  
    }  
    return 0;  
}
