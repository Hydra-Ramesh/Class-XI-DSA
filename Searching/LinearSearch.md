
```c
// You are given one 1D Array and one key, you have to find that the key is present or not and if present in which index.

// We will match every element
// We will print the idx and break the Loop
// We should print unsuccess message outside the loop.
#include<stdio.h>
void linearSearch(int arr[],int n,int key){
    int present = 0;
    for(int i=0;i<n;i++){
        if(arr[i]==key){
            printf("Present at %dth Index",i);
            present = 1;
            break;
        }
    }
    if(present==0){
        printf("The key %d is not Present Here",key);
    }
}
int main(){
    int n;
    printf("Enter the Size of Array: ");
    scanf("%d",&n);
    int arr[n];
    for(int i=0;i<n;i++){
        scanf("%d",&arr[i]);
    }
    int key;
    printf("Enter the Number what you want to Search: ");
    scanf("%d",&key);
    linearSearch(arr,n,key);
    return 0;
}
```