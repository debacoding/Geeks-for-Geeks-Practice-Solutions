# [C++ arrays (sum of array) | Set - 1](https://practice.geeksforgeeks.org/problems/c-arrays-sum-of-array-set-14805/1/?category[]=Arrays&category[]=Arrays&problemStatus=solved&difficulty[]=-2&page=1&query=category[]ArraysproblemStatussolveddifficulty[]-2page1category[]Arrays)
```cpp
// { Driver Code Starts
#include <iostream>
using namespace std;

 // } Driver Code Ends


class Solution{
    public:
    int getSum(int a[], int n) {
        // Your code goes here
        int sum = 0;
        for(int i = 0; i < n; i++){
            sum = sum + a[i];
        }
        return sum;
    }   
};

// { Driver Code Starts.
int main() {
    int t;
    cin >> t;
    while (t--) {
        int n;
        cin >> n;
        int a[n];
        for (int i = 0; i < n; i++) cin >> a[i];
        Solution ob;
        cout << ob.getSum(a, n) << endl;
    }

    return 0;
}  // } Driver Code Ends
```

# 
