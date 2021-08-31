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

# [max and min of array elements](https://practice.geeksforgeeks.org/problems/maximum-and-minimum-of-array-elements/0/?category[]=Arrays&category[]=Arrays&difficulty[]=-2&page=1&query=category[]Arraysdifficulty[]-2page1category[]Arrays)
```cpp
#include<bits/stdc++.h>
using namespace std;
int main()
 {
	//code
	int testCases, size;
    cin >> testCases;
    int arr[100];

    while (testCases--)
    {
        cin >> size; // array size
        for (int i = 0; i < size; i++)
        {
            cin >> arr[i]; // enter array elements
        }

        int MAX = arr[0], MIN = arr[0]; // initially element at first index is considered max and min
        for (int i = 0; i < size; i++)
        {
            if (arr[i] >= MAX)
            {
                MAX = arr[i];
            }
            else if (arr[i] <= MIN)
            {
                MIN = arr[i];
            }
        }
        cout << MAX << " " << MIN << endl;
    }
	
	return 0;
}
```

# [reverse an array](https://practice.geeksforgeeks.org/problems/reverse-an-array/0/?category[]=Arrays&category[]=Arrays&difficulty[]=-2&page=1&query=category[]Arraysdifficulty[]-2page1category[]Arrays)
```cpp
#include<bits/stdc++.h>
using namespace std;
int main()
 {
	//code
	int T;
	cin >> T;
	
	int A[100];
	
    while(T--){
    int N;
    cin >> N;
    
    for(int i = 0; i < N; i++){
        cin >> A[i];
    }
    
    for(int i = N - 1; i >= 0; i-- ){
        cout << A[i] << " ";
    }
    
    cout << endl;
    
    } 
    
	return 0;
}
```

# [perfect arrays](https://practice.geeksforgeeks.org/problems/perfect-arrays4645/1/?category[]=Arrays&category[]=Arrays&difficulty[]=-2&page=1&query=category[]Arraysdifficulty[]-2page1category[]Arrays)
```cpp
// { Driver Code Starts
//Initial Template for C++

#include <bits/stdc++.h>
using namespace std;

 // } Driver Code Ends
//User function Template for C++

class Solution{
    public:
    bool IsPerfect(int a[],int n)
    {
        // Complete the function
        int start = 0;
        int end = n - 1;
        
        while(start < end){
            if(a[start] == a[end]){
                start ++; // increment from start
                end--; // decrement from end
            } else {
                return 0;
            }
           
        }
       return 1; 
    }
};




// { Driver Code Starts.
int main()
{
    int t;cin>>t;
    while(t--)
    {
        int n;cin>>n;
        int a[n];
        
        for(int i=0;i<n;i++)
            cin>>a[i];
        Solution ob;
        if(ob.IsPerfect(a,n))
            cout<<"PERFECT\n";
        else
            cout<<"NOT PERFECT\n";
        
    }
    
}  // } Driver Code Ends
```

# [print the left element](https://practice.geeksforgeeks.org/problems/print-the-left-element2009/1/?category[]=Arrays&category[]=Arrays&difficulty[]=-2&page=1&query=category[]Arraysdifficulty[]-2page1category[]Arrays)
```cpp
// { Driver Code Starts
#include <bits/stdc++.h>
using namespace std;

 // } Driver Code Ends

class Solution{
    public:
    int leftElement(int a[], int n) {
        // Your code goes here 
        sort(a, a+n);
        return a[(n-1)/2];
    }
};

// { Driver Code Starts.
int main() {
    int t;
    cin >> t;
    while (t--) {
        int n;
        cin >> n;
        int a[n], i;
        for (i = 0; i < n; i++) cin >> a[i];
        Solution ob;
        cout << ob.leftElement(a, n) << endl;
    }
}
  // } Driver Code End
```

# [smaller and larger](https://practice.geeksforgeeks.org/problems/smaller-and-larger4005/1/?category[]=Arrays&category[]=Arrays&difficulty[]=-2&page=1&query=category[]Arraysdifficulty[]-2page1category[]Arrays)
```cpp
// { Driver Code Starts
#include <bits/stdc++.h>

using namespace std;


 // } Driver Code Ends
//User function template for C++
class Solution{
public:	
	vector<int> getMoreAndLess(int arr[], int n, int x) {
	    // code here
	    vector<int> v;
	    int count1 = 0, count2 = 0; // count1 counts for elements <= x, count2 counts for elements >= x
	    
	    for(int i = 0; i < n; i++){
	        if(arr[i] <= x)
	            count1++;
	        if(arr[i] >= x)
	            count2++;
	    }
	    v.push_back(count1);
	    v.push_back(count2);
	    return v;
	}
};

// { Driver Code Starts.

int main() {
    int t;
    cin >> t;
    while (t--) {
        int n, x;
        cin >> n >> x;
        int arr[n];
        for (int i = 0; i < n; i++) {
            cin >> arr[i];
        }
        Solution ob;
        auto ans = ob.getMoreAndLess(arr, n, x);
        cout << ans[0] << " " << ans[1] << "\n";
    }
    return 0;
}
```

# [compete the skills](https://practice.geeksforgeeks.org/problems/compete-the-skills5807/1/?category[]=Arrays&category[]=Arrays&difficulty[]=-2&page=1&query=category[]Arraysdifficulty[]-2page1category[]Arrays)
```cpp
// { Driver Code Starts
#include<bits/stdc++.h>
using namespace std;

 // } Driver Code Ends
class Solution{
    public:
    void scores(long long a[], long long b[], int &ca, int &cb)
    {
        // Your code goes here
        for(int i = 0; i < 3; i++){
            if(a[i] > b[i]){
                ca++;
            }else if(a[i] < b[i]){
                cb++;
            }
        }
    }
};

// { Driver Code Starts.
int main()
{
    int t=0;
    cin>>t;
    while(t--)
    {
        long long int a[5], b[5], i=0;
        int ca=0, cb=0;
        for(i=0; i<3; i++)
            cin>>a[i];
    
        for(i=0; i<3; i++)
            cin>>b[i];
        Solution ob;
        ob.scores(a, b, ca, cb);
        
        cout<<ca<<" "<<cb<<endl;
    }
    return 0 ;
}  // } Driver Code Ends
```

# [find index](https://practice.geeksforgeeks.org/problems/find-index4752/1/?category[]=Arrays&category[]=Arrays&difficulty[]=-2&page=1&query=category[]Arraysdifficulty[]-2page1category[]Arrays)
```cpp
// { Driver Code Starts
#include <iostream>
#include <bits/stdc++.h> 
#include <vector> 
using namespace std; 

 // } Driver Code Ends
class Solution
{
  public:
    vector<int> findIndex(int a[], int n, int key)
    {
        //code here.
        vector<int> v;
        
        // start index( index where the element 
        // is first found from left in the array )
        for(int i = 0; i < n; i++){
            if(a[i] == key){
                v.push_back(i);
                break;
            }else{
                continue;
            }
        }
        
        
        
        // end index( index where the element 
        // is first found from right in the array )
        for(int i = n - 1; i >= 0; i++){
            if(a[i] == key){
                v.push_back(i);
                break;
            }else{
                continue;
            }
        }
        
        // If the key does not exist in the array then 
        // return -1 for both start and end index in this case.
        if(v.size() == 0){
            v.push_back(-1);
            v.push_back(-1);
        }
        
        return v;
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
        vector<int> res;
        cin>>n;
        int arr[n];
        for(int i=0;i<n;i++)
            cin>>arr[i];
        int key;
        cin>>key;
        Solution ob;
        res=ob.findIndex(arr, n, key);
        for (int i = 0; i < res.size(); i++) 
        cout << res[i] << " ";
        cout << "\n";
    }
    
    return 0;
}
  // } Driver Code Ends
```

# [atleast two greatest elements](https://practice.geeksforgeeks.org/problems/at-least-two-greater-elements4625/1/?category[]=Arrays&category[]=Arrays&difficulty[]=-2&page=1&query=category[]Arraysdifficulty[]-2page1category[]Arrays)
```cpp
// { Driver Code Starts
#include<bits/stdc++.h>
using namespace std;


 // } Driver Code Ends
class Solution{
    public:
        vector<int> findElements(int a[], int n)
    {
        // Your code goes here  
        sort(a, a+n); // sort the array first
        
        vector<int> v;
        for(int i = 0; i < (n - 2); i++){ // (n - 2) to remove two largest nos.
            v.push_back(a[i]);
        }
        return v;
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
        int a[n];
        for(int i=0;i<n;i++)
        cin>>a[i];
        Solution ob;
        vector <int> res = ob.findElements(a,n);
        
        for(int i=0;i<res.size();i++)
        cout<<res[i]<<" ";
        cout<<endl;
    }
}  // } Driver Code Ends
```

# [C++ 2D arrays | set-1](https://practice.geeksforgeeks.org/problems/c-2-d-arrays0708/1/?category[]=Arrays&category[]=Arrays&difficulty[]=-2&page=1&query=category[]Arraysdifficulty[]-2page1category[]Arrays)
```cpp
// { Driver Code Starts

#include<bits/stdc++.h>
using namespace std;
#define M 101

vector<vector<int>> transpose(int a[][M], int n);

int main()
{
    int t;
    cin>>t;
    int a[M][M];
    while(t--)
    {
        int n;
        cin>>n;
        for(int i=0;i<n;i++)
        {
            for(int j=0;j<n;j++)
            {
                cin>>a[i][j];
            }
        }
        vector<vector<int>> b;
        b = transpose(a, n);
        for(int i=0;i < n;i++)
        {
            for(int j=0;j<n;j++){
                cout << b[i][j] << " ";
            }
        }
        cout<<endl;
    }
}


// } Driver Code Ends



vector<vector<int>> transpose(int a[][M], int n)
{
    // Code here
    vector<vector<int>> v;
    
    int temp;
    
    for(int i = 0; i < n; i++){ // rows
        vector<int> v1;
        for(int j = 0; j < M; j++){ // columns
            if(i < j){
                temp = a[i][j];
                a[i][j] = a[j][i];
                a[j][i] = temp;
            }
            v1. push_back(a[i][j]);
        }
        v.push_back(v1);  
    }
    return v;
}
```

# [second largest](https://practice.geeksforgeeks.org/problems/second-largest3735/1/?category[]=Arrays&category[]=Arrays&difficulty[]=-2&page=1&query=category[]Arraysdifficulty[]-2page1category[]Arrays)
```cpp
// { Driver Code Starts
#include <bits/stdc++.h>

using namespace std;

 // } Driver Code Ends
//User function template for C++
class Solution{
public:	
	// Function returns the second
	// largest elements
	int print2largest(int arr[], int n) {
	    // code here
	    int max = -1, second_max = -1;
	    
	    for(int i = 0; i < n; i++){
	        if(arr[i] > max && arr[i] > second_max){ 
	            second_max = max;
	            max = arr[i]; 
	        }  else if(arr[i] < max && arr[i] > second_max){
	                second_max = arr[i];
	        }
	        
	          
	    }
	    return second_max;
	}
};

// { Driver Code Starts.

int main() {
    int t;
    cin >> t;
    while (t--) {
        int n;
        cin >> n;
        int arr[n];
        for (int i = 0; i < n; i++) {
            cin >> arr[i];
        }
        Solution ob;
        auto ans = ob.print2largest(arr, n);
        cout << ans << "\n";
    }
    return 0;
}
  // } Driver Code Ends
```

# [fascinating number](https://practice.geeksforgeeks.org/problems/fascinating-number3751/1/?category[]=Arrays&category[]=Arrays&difficulty[]=-2&page=2&query=category[]Arraysdifficulty[]-2page2category[]Arrays)
```cpp
// { Driver Code Starts
// Initial Template for C++

#include <bits/stdc++.h>

using namespace std;


 // } Driver Code Ends
//User function template for C++
class Solution{
public:
	
	bool fascinating(int n) {
	    // code here
	     int one = 0, two = 0, three = 0, four = 0, five = 0, six = 0, seven = 0, eight = 0, nine = 0;
	    // number is multiplied by 2 and 3 
	    // and concatenated with original number
	    string str = to_string(n) + to_string(n*2) + to_string(n*3);

        
       for(int i=0; i<=str.length(); i++){
            if(str[i] == '1')
               one ++;
            if(str[i] == '2')
               two ++; 
            if(str[i] == '3')
               three ++; 
            if(str[i] == '4')
               four ++; 
            if(str[i] == '5')
               five ++; 
            if(str[i] == '6')
               six ++;
            if(str[i] == '7')
               seven ++;
            if(str[i] == '8')
               eight ++;
            if(str[i] == '9')
               nine ++;   
        }
        // concatenated number must have all digits 
        // from 1 to 9 exactly once
        if(one == 1 && two == 1 && three == 1 && four == 1 && five == 1 && six == 1 && seven == 1 && eight == 1 && nine == 1)
           return true;
        else
           return false;
	}
};

// { Driver Code Starts.

int main() {
    int t;
    cin >> t;
    while (t--) {
        int n;
        cin >> n;
        Solution ob;
        auto ans = ob.fascinating(n);
        if (ans) {
            cout << "Fascinating\n";
        } else {
            cout << "Not Fascinating\n";
        }
    }
    return 0;
}  // } Driver Code Ends
```

# [sum of series](https://practice.geeksforgeeks.org/problems/sum-of-series2811/1/?category[]=Arrays&category[]=Arrays&difficulty[]=-2&page=2&query=category[]Arraysdifficulty[]-2page2category[]Arrays)
```cpp
// { Driver Code Starts
#include <bits/stdc++.h>

using namespace std;

 // } Driver Code Ends
//User function template for C++
class Solution{
public:
	// function to return sum of  1, 2, ... n
	long long seriesSum(long long n) {
	    // code here
	    
	    // sum of n natural numbers formula
	    
	    return (n * (n + 1)) / 2;
	}
};

// { Driver Code Starts.

int main() {
    int t;
    cin >> t;
    while (t--) {
        int n;
        cin >> n;
        Solution ob;
        auto ans = ob.seriesSum(n);
        cout << ans << "\n";
    }
    return 0;
}  // } Driver Code Ends
```

# [average in a stream](https://practice.geeksforgeeks.org/problems/average4856/1/?category[]=Arrays&category[]=Arrays&difficulty[]=-2&page=2&query=category[]Arraysdifficulty[]-2page2category[]Arrays)
```cpp
// { Driver Code Starts
#include <bits/stdc++.h>
using namespace std;

 // } Driver Code Ends
//User function template for C++

class Solution{
public:	
	vector<float> streamAvg(int arr[], int n) {
	    // code here
	    float sum = 0;
	    vector<float> avg;
	    
	    for(int i = 0; i < n; i++){
	        sum += arr[i]; // calculates sum
	        float avg1 = sum / (i + 1); // calculates average
	        avg.push_back(avg1); // average pushed into vector "avg"
	    }
	    
	    return avg;
	}
};

// { Driver Code Starts.
int main() {
    int t;
    cin >> t;
    while (t--) {
        int n;
        cin >> n;
        int arr[n];
        for (int i = 0; i < n; i++) {
            cin >> arr[i];
        }
        Solution ob;
        auto ans = ob.streamAvg(arr, n);
        cout << fixed<< setprecision(2);
        for (auto x : ans) {
            cout <<x<<" ";
        }
        cout << "\n";
    }
    return 0;
```
