#include <iostream>
#include <climits>

using namespace std;

int findBestIndex(int arr[], int n) {
    int maxSpecialSum = INT_MIN;
    int bestIndex = -1;

    for (int i = 0; i < n; i++) {
        int specialSum = 0;
        int count = 1;
        int j = i;

        // Calculate the special sum starting from index i
        while (j + count <= n) {
            for (int k = 0; k < count; k++) {
                specialSum += arr[j + k];
            }
            j += count;
            count++;
        }

        // Check if the current special sum is the maximum
        if (specialSum > maxSpecialSum) {
            maxSpecialSum = specialSum;
            bestIndex = i;
        }
    }

    return maxSpecialSum;
}

int main() {
    int n;
    cout << "Enter the number of elements in the array: ";
    cin >> n;

    int arr[n];
    cout << "Enter the elements of the array: ";
    for (int i = 0; i < n; i++) {
        cin >> arr[i];
    }

    int result = findBestIndex(arr, n);
    cout << "The maximum special sum is: " << result << endl;

    return 0;
}
