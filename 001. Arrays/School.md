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

# [C++ array(print an element) | Set - 2](https://practice.geeksforgeeks.org/problems/c-array-print-an-element-set-25933/1/?category[]=Arrays&category[]=Arrays&problemStatus=solved&difficulty[]=-2&page=1&query=category[]ArraysproblemStatussolveddifficulty[]-2page1category[]Arrays)
```cpp
// { Driver Code Starts
#include <iostream>
using namespace std;

 // } Driver Code Ends


class Solution{
    public:
    int findElementAtIndex(int a[], int n, int key) 
    {
        // Your code goes here
        return a[key];
    }
};

// { Driver Code Starts.

int main() {
    int t;
    cin >> t;
    while (t--) {
        int n, key;
        cin >> n >> key;
        int a[n];
        for (int i = 0; i < n; i++) cin >> a[i];
        Solution ob;
        cout << ob.findElementAtIndex(a, n, key) << endl;
    }

    return 0;
}  // } Driver Code Ends
```

# [sum of array](https://practice.geeksforgeeks.org/problems/sum-of-array2326/1/?category[]=Arrays&category[]=Arrays&problemStatus=solved&difficulty[]=-2&page=1&query=category[]ArraysproblemStatussolveddifficulty[]-2page1category[]Arrays)
```cpp
// { Driver Code Starts
#include <bits/stdc++.h>

using namespace std;

 // } Driver Code Ends
//User function template for C++
class Solution{
public:
	// function to return sum of elements
	// in an array of size n
	int sum(int arr[], int n) {
	    // code here
	    int sum = 0;
	    for(int i = 0; i < n; i++){
	        sum = sum + arr[i];
    	}
	return sum;
	}
};

// { Driver Code Starts.

int main() {
    int t;
    cin >> t;
    while (t--) {
        int n, i;
        cin >> n;
        int arr[n];
        for (i = 0; i < n; i++) {
            cin >> arr[i];
        }
        Solution ob;
        auto ans = ob.sum(arr, n);
        cout << ans << "\n";
    }
    return 0;
}  // } Driver Code Ends
```

# [display longest name](https://practice.geeksforgeeks.org/problems/display-longest-name0853/1/?category[]=Arrays&category[]=Arrays&difficulty[]=-2&page=1&query=category[]Arraysdifficulty[]-2page1category[]Arrays)
```cpp
// { Driver Code Starts
//Initial Template for C++

#include <bits/stdc++.h>
using namespace std;


 // } Driver Code Ends
//User function Template for C++

class Solution{
    public:
    string longest(string names[], int n)
    {
        int count = 0, pos = 0;
        
        for(int i = 0; i < n; i++){
            if(names[i].length() > count){  // length at i greater than count
                count = names[i].length();
                pos = i;
            }
            
        }
        return names[pos];
    }
};

// { Driver Code Starts.

int main()
{
	int t;
	cin>>t;
	while(t--)
	{
		int n;
		cin>>n;
		string names[n];
		
		for(int i=0;i<n;i++)
			cin>>names[i];
		Solution ob;
		cout<< ob.longest(names, n) << endl;
	}
}
  // } Driver Code Ends
```

# [count of smaller elements](https://practice.geeksforgeeks.org/problems/count-of-smaller-elements5947/1/?category[]=Arrays&category[]=Arrays&difficulty[]=-2&page=1&query=category[]Arraysdifficulty[]-2page1category[]Arrays)
```cpp
// { Driver Code Starts
#include <bits/stdc++.h>
using namespace std;

int countOfElements(int arr[], int n, int x);

int main() {
    int t;
    cin >> t;
    while (t--) {
        int n, x;
        cin >> n;
        int arr[n];
        for (int i = 0; i < n; i++) cin >> arr[i];
        
        cin >> x;

        cout << countOfElements(arr, n, x) << endl;
    }
    return 0;
}// } Driver Code Ends


int countOfElements(int arr[], int n, int x) 
{
    int count = 0;
    
    for(int i = 0; i < n; i++){
        if(arr[i] <= x){
            count++;
        }
    }
    return count;
}
```

# [print elements of array](https://practice.geeksforgeeks.org/problems/print-elements-of-array4910/1/?category[]=Arrays&category[]=Arrays&difficulty[]=-2&page=1&query=category[]Arraysdifficulty[]-2page1category[]Arrays)
```cpp
// { Driver Code Starts
#include <bits/stdc++.h>

using namespace std;


 // } Driver Code Ends
//User function template for C++
class Solution{
public:
	void printArray(int arr[], int n) {
	    // code here
	    for(int i = 0; i < n; i++){
	        cout << arr[i] << " ";
	    }
	}
};

// { Driver Code Starts.

int main() {
    int t;
    cin >> t;
    while (t--) {
        int n, i;
        cin >> n;
        int arr[n];
        for (i = 0; i < n; i++) {
            cin >> arr[i];
        }
        Solution ob;
        ob.printArray(arr, n);
        cout << "\n";
    }
    return 0;
}
  // } Driver Code Ends
```

# [value equal to index value](https://practice.geeksforgeeks.org/problems/value-equal-to-index-value1330/1/?category[]=Arrays&category[]=Arrays&difficulty[]=-2&page=1&query=category[]Arraysdifficulty[]-2page1category[]Arrays)
```cpp
// { Driver Code Starts
#include<bits/stdc++.h>

using namespace std;


 // } Driver Code Ends
//User function template for C++
class Solution{
public:

	vector<int> valueEqualToIndex(int arr[], int n) {
	    // code here
	    vector<int> v;
	    
	    for(int i = 0; i < n; i++){
	        if(arr[i] == i + 1){ // since in the output indexing is 1-based not 0-based
	           v.push_back(arr[i]);
	        }
	    }
	    return v;
	}
};

// { Driver Code Starts.

int main() {
    int t;
    cin >> t;
    while (t--) {
        int n, i;
        cin >> n;
        int arr[n];
        for (i = 0; i < n; i++) {
            cin >> arr[i];
        }
        Solution ob;
        auto ans = ob.valueEqualToIndex(arr, n);
        if (ans.empty()) {
            cout << "Not Found";
        } else {
            for (int x: ans) {
                cout << x << " ";
            }
        }
        cout << "\n";
    }
    return 0;
}
  // } Driver Code Ends
```

# [swap kth elements](https://practice.geeksforgeeks.org/problems/swap-kth-elements5500/1/?category[]=Arrays&category[]=Arrays&difficulty[]=-2&page=1&query=category[]Arraysdifficulty[]-2page1category[]Arrays)
```cpp
// { Driver Code Starts
#include <bits/stdc++.h>

using namespace std;


 // } Driver Code Ends
//User function template for C++
class Solution{
public:	
	// swap k'th element from beginning and end
	void swapKth(int *arr, int n, int k) {
	    // code here
	    swap(arr[k - 1],arr[n - k]); // indexing starts from 1 instead 0
	    
	}
};

// { Driver Code Starts.

int main() {
    int t;
    cin >> t;
    while (t--) {
        int n, k;
        cin >> n >> k;
        int arr[n];
        for (int i = 0; i < n; i++) {
            cin >> arr[i];
        }
        Solution ob;
        ob.swapKth(arr, n, k);
        for (int i = 0; i < n; i++) {
            cout << arr[i] << " ";
        }
        cout << "\n";
    }
    return 0;
}
  // } Driver Code Ends
```

# [print alternate elements of an array](https://practice.geeksforgeeks.org/problems/print-alternate-elements-of-an-array/1/?category[]=Arrays&category[]=Arrays&difficulty[]=-2&page=1&query=category[]Arraysdifficulty[]-2page1category[]Arrays)
```cpp
// { Driver Code Starts
//Initial Template for C++

#include<bits/stdc++.h>
using namespace std;




 // } Driver Code Ends
//User function Template for C++

// ar[] is the array 
// n is the number of elements in array.
void print(int ar[], int n)
{
    // code here
    for(int i = 0; i < n; i++){
        if(i % 2 == 0){
            cout << ar[i] << " ";
        }
    }    
}

// { Driver Code Starts.
int main()
{
   int t;
   cin>>t;
  while(t--)
   {
     int ar[100001]={0};
     int n;
     cin>>n;
     for(int i=0;i<n;i++)
      cin>>ar[i];
      print(ar,n);
      cout<<endl;
     }

return 0;
}
  // } Driver code ends.
```

# [palindromic array](https://practice.geeksforgeeks.org/problems/palindromic-array-1587115620/1/?category[]=Arrays&category[]=Arrays&difficulty[]=-2&page=1&query=category[]Arraysdifficulty[]-2page1category[]Arrays)
```cpp
#include<string.h>
using namespace std;
int PalinArray(int a[], int n);
int main()
{
	int t;
	cin>>t;
	while(t--)
	{
		int n;
		cin>>n;
		int a[n];
		for(int i = 0; i < n; i++)
			cin>>a[i];
		cout<<PalinArray(a,n)<<endl;
	}
}// } Driver Code Ends

#include<algorithm>
/*Complete the function below*/
int PalinArray(int a[], int n)
{  //add code here.
   int count = 0;
   
   for(int i = 0; i < n; i++){
       string str1 = to_string(a[i]); // converting array to string
       
       string str2;
       for(int i = 0; i < str1.length(); i++){
           str2 += str1[i]; 
       }
       
       reverse(str2.begin(),str2.end());
       
       if(str1 == str2){
           count++;
       }
   }
   if(count == n){
       return 1;
   } else {
       return 0;
   }
}
```
