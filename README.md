# swap_max_and_min_of_array
// SWAP MAX AND MIN ELEMENTS OF AN ARRAY
#include <iostream>
using namespace std;

void swap(int arr[], int i, int j) {
    int temp = arr[i];
    arr[i] = arr[j];
    arr[j] = temp;
}

void max_min_swap(int arr[], int size) {
    int maxindex = 0;
    int minindex = 0;
    for (int i=0; i<size; i++) {
        if (arr[i]>arr[maxindex]) {
            maxindex = i;
        }
    }

    for (int i=0; i<size; i++) {
        if (arr[i]<arr[minindex]) {
            minindex = i;
        }
    }

    swap(arr, maxindex, minindex);    
}

int main() {
    int arr[] = {2,4,6,8};
    max_min_swap(arr, 4);
    for (int i=0; i<4; i++) {
        cout << arr[i] << endl;
    }
    return 0;
}
