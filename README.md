# NON-REPEATING-ELEMENT-IN-C
EX:- ARR[]={6,5,5,1,2,2}  OUTPUT SHOULD BE:-6,1
```
#include<stdio.h>
void nonrepeating(int arr[], int size) {
    printf("Non-repeating elements: ");
    for (int i = 0; i < size; i++) {
        int single = 1; // Assume element is unique initially
        for (int j = 0; j < size; j++) {
            if (i != j && arr[i] == arr[j]) {
                 single= 0; // Found a duplicate
                break;
            }
        }
        if (single) {
            printf("%d ", arr[i]);
        }
    }
    printf("\n");
}
int main() {
    int n,i;
    printf("Enter the size: ");
    scanf("%d",&n);
    int arr[n];
    for(i=0;i<n;i++) {
        scanf("%d",&arr[i]);
    }
    nonrepeating(arr,n);
    return 0;
}
```
    //
// Created by Suprakash Ghosh on 25-07-2025.
//
