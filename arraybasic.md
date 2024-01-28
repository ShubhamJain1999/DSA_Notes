#include <iostream>
#include <algorithm>

// Function to reverse an array in-place using std::swap
void reverseArrayUsingSwap(int arr[], int n) {
    for (int i = 0; i < n / 2; i++) {
        // Swap elements at index i and its corresponding index from the end
        std::swap(arr[i], arr[n - 1 - i]);
    }
}

// Function to print an array
void printArray(int arr[], int n) {
    for (int i = 0; i < n; i++) {
        std::cout << arr[i] << " ";
    }
    std::cout << std::endl;
}

int main() {
    int arr[] = {1, 2, 3, 4, 5};
    int n = sizeof(arr) / sizeof(arr[0]);

    // Reverse in-place using std::swap
    reverseArrayUsingSwap(arr, n);
    std::cout << "Reversed array (using std::swap): ";
    printArray(arr, n);

    return 0;
}
In this example, the reverseArrayUsingSwap function iterates through the array, swapping elements from the beginning with their corresponding elements from the end. This approach has a time complexity of O(n) and a space complexity of O(1), making it an efficient in-place reversal method.

