# [largest element in array](https://practice.geeksforgeeks.org/problems/largest-element-in-array4009/1/?category[]=Arrays&category[]=Arrays&difficulty[]=-1&page=1&query=category[]Arraysdifficulty[]-1page1category[]Arrays)
```cpp
// { Driver Code Starts
//Initial Template for C++

#include <bits/stdc++.h>
using namespace std;

 // } Driver Code Ends
//User function Template for C++

class Solution
{
public:
    int largest(vector<int> &arr, int n)
    {
       sort(arr.begin(),arr.end());
       return arr[n - 1];
    }
};


// { Driver Code Starts.
int main()
{
    int t;
    cin >> t;
    while (t--)
    {
        int n;
        cin >> n;
        vector<int>arr(n);
        for (int i = 0; i < n; i++)
        {
            cin >> arr[i];
        }
        Solution ob;
        cout << ob.largest(arr, n) << "\n";
    }
    return 0;
}
  // } Driver Code Ends
```

# [game with nos.](https://practice.geeksforgeeks.org/problems/game-with-nos3123/1/?category[]=Arrays&category[]=Arrays&difficulty[]=-1&page=1&query=category[]Arraysdifficulty[]-1page1category[]Arrays)
```cpp
// { Driver Code Starts
#include<bits/stdc++.h>
using namespace std;


int* game_with_number(int arr[], int n);

int main()
{
    
    int t;
    cin>> t;
    while(t--)
    {
        int n;
        cin >> n;
        int arr[n];
        
        for(int i=0;i<n;i++)
            cin>>arr[i];
        
        int *arr2;
        
        arr2 = game_with_number(arr, n);
        for(int i = 0;i < n; i++)
            cout << arr2[i] << " ";
        
        cout << endl;
        
    }

}
// } Driver Code Ends


int* game_with_number(int arr[], int n)
{
    
    // Complete the function
    for(int i = 0; i < n - 1; i++){
        arr[i] = arr[i] ^ arr[i + 1];
    }
    
     return arr;
    
}
```

# [play with OR](https://practice.geeksforgeeks.org/problems/play-with-or5515/1/?category[]=Arrays&category[]=Arrays&difficulty[]=-1&page=1&query=category[]Arraysdifficulty[]-1page1category[]Arrays)
```cpp
// { Driver Code Starts
#include<bits/stdc++.h>
using namespace std;


int* game_with_number(int arr[], int n);

int main()
{
    
    int t;cin>> t;
    while(t--)
    {
        int n;
        cin >> n;
        int arr[n];
        
        for(int i=0;i<n;i++)
            cin>>arr[i];
        
        int *arr2;
        
        arr2 = game_with_number(arr, n);
        for(int i = 0;i < n; i++)
            cout << arr2[i] << " ";
        
        cout << endl;
        
    }

}
// } Driver Code Ends


int* game_with_number(int arr[], int n)
{
    
    // Complete the function
    for(int i = 0; i < n - 1; i++){
        arr[i] = arr[i] | arr[i + 1];
    }
    return arr;
    
}
```

# [find min and max in an array](https://practice.geeksforgeeks.org/problems/find-minimum-and-maximum-element-in-an-array4428/1/?category[]=Arrays&category[]=Arrays&difficulty[]=-1&page=1&query=category[]Arraysdifficulty[]-1page1category[]Arrays)
```cpp
// { Driver Code Starts
#include <bits/stdc++.h>
using namespace std;
#define ll long long

pair<long long, long long> getMinMax(long long a[], int n) ;

int main() {
    int t;
    cin >> t;
    while (t--) {
        int n;
        cin >> n;
        ll a[n];
        for (int i = 0; i < n; i++) cin >> a[i];

        pair<ll, ll> pp = getMinMax(a, n);

        cout << pp.first << " " << pp.second << endl;
    }
    return 0;
}// } Driver Code Ends


pair<long long, long long> getMinMax(long long a[], int n) {
    pair<int,int> k;
    
    sort(a,a + n); // after sorting first no. is smallest and last no. is largest
    
    k.first = a[0]; // min. element
    k.second = a[n - 1]; // max. element
    
    return k;
    
}

```

# [cyclically rotate an array by one](https://practice.geeksforgeeks.org/problems/cyclically-rotate-an-array-by-one2614/1/?category[]=Arrays&category[]=Arrays&difficulty[]=-1&page=1&query=category[]Arraysdifficulty[]-1page1category[]Arrays)
```cpp
// { Driver Code Starts
//Initial Template for C++

#include <bits/stdc++.h>
using namespace std;
void rotate(int arr[], int n);

int main()
{
    int t;
    scanf("%d",&t);
    while(t--)
    {
        int n;
        scanf("%d",&n);
        int a[n] , i;
        for(i=0;i<n;i++)
        scanf("%d",&a[i]);
        rotate(a, n);
        for (i = 0; i < n; i++)
            printf("%d ", a[i]);
        printf("\n");
    }
        return 0;
}
// } Driver Code Ends


//User function Template for C++

void rotate(int arr[], int n)
{
    int temp = arr[n - 1]; // initially temp stores last element
    
    for(int i = n - 1; i > 0; i--){
        arr[i] = arr[i - 1];
        arr[i - 1] = temp; // last comes to first
    }
    
}

```

# [multiply left and right array sum](https://practice.geeksforgeeks.org/problems/multiply-left-and-right-array-sum1555/1/?category[]=Arrays&category[]=Arrays&difficulty[]=-1&page=1&query=category[]Arraysdifficulty[]-1page1category[]Arrays)
```cpp
// { Driver Code Starts
//Initial Template for C++

#include <bits/stdc++.h>
using namespace std;

int multiply(int arr[], int n);


int main() {
	//code
	int t;
	cin>>t;
	while (t--)
	{
	    int n,sum1=0,sum2=0;
	    cin>>n;
	    int a[n];
	    for(int i=0;i<n;i++)
	        cin>>a[i];
	    
	    cout << multiply(a, n) << endl;
	    
	}
	return 0;
}// } Driver Code Ends


//User function Template for C++

int multiply(int arr[], int n)
{
    // Complete the function
    int sumLeft = 0, sumRight = 0;
    
    for(int i = 0; i < n / 2; i++){
       sumLeft +=  arr[i]; // sum of left sub-array
    }
    
    for(int i = n / 2; i < n; i++){
        sumRight += arr[i]; // sum of right sub-array
    }
    
    return (sumLeft * sumRight); // product of sums of left and right sub-arries
}

```

# [ishaan love chocolates](https://practice.geeksforgeeks.org/problems/ishaan-loves-chocolates2156/1/?category[]=Arrays&category[]=Arrays&problemStatus=solved&difficulty[]=-1&page=1&query=category[]ArraysproblemStatussolveddifficulty[]-1page1category[]Arrays)
```cpp
// { Driver Code Starts
#include<bits/stdc++.h>
using namespace std;


int chocolates(int arr[], int n);


int main()
{
    
    int t;cin>> t;
    while(t--)
    {
        int n;
        cin >> n;
        int arr[n];
        
        for(int i=0;i<n;i++)
            cin>>arr[i];
        
        
        cout << chocolates(arr, n);
        cout << endl;
        
    }

}
// } Driver Code Ends


int chocolates(int arr[], int n)
{
    // Complete the function
    sort(arr,arr + n);
    return arr[0]; // min. element is ans.
    
}

```

# [product of max in first array and min in second](https://practice.geeksforgeeks.org/problems/product-of-maximum-in-first-array-and-minimum-in-second3943/1/?category[]=Arrays&category[]=Arrays&problemStatus=solved&difficulty[]=-1&page=1&query=category[]ArraysproblemStatussolveddifficulty[]-1page1category[]Arrays)
```cpp
// { Driver Code Starts
#include <bits/stdc++.h>
using namespace std;

 // } Driver Code Ends
class Solution{
    public:
        long long find_multiplication(int a[], int b[], int n, int m)
    {
        // Complete the function
        sort(a,a + n);
        long long max = a[n - 1]; // max element in array a
        
        sort(b,b + m);
        long long min = b[0]; // min element in array b
        
        return max * min;    
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
        for(int i=0;i<n;i++)    cin>>a[i];
        
        int m;
        cin>>m;
        int b[m];
        for(int i=0;i<m;i++)    cin>>b[i];
        
        
        Solution ob;
        cout<<ob.find_multiplication(a, b, n, m)<<endl;

    }
    return 0;

```

# [rotate array](https://practice.geeksforgeeks.org/problems/rotate-array-by-n-elements/0/?category[]=Arrays&category[]=Arrays&problemStatus=solved&difficulty[]=-1&page=1&query=category[]ArraysproblemStatussolveddifficulty[]-1page1category[]Arrays)
```cpp
#include<iostream>
using namespace std;
int main()
 {
	//code
	int t;
	cin >> t; // test cases
	
	while(t--){
	    unsigned int n,d;
	    cin >> n >> d; // n : size of array, d : rotate by d elements
	    
	    int a[n];
	    for(unsigned int i = 0; i < n; i++){
	        cin >> a[(i + n - d) % n];
	    }
	    
	    for(unsigned int i = 0; i < n; i++){
	        cout << a[i] << " ";
	    }
	    
	    cout << endl;
	}
	
	return 0;
}

```

# [min no. to form the sum even](https://practice.geeksforgeeks.org/problems/minimum-number-to-form-the-sum-even0326/1/?category[]=Arrays&category[]=Arrays&problemStatus=solved&difficulty[]=-1&page=1&query=category[]ArraysproblemStatussolveddifficulty[]-1page1category[]Arrays)
```cpp
// { Driver Code Starts
#include <bits/stdc++.h>
using namespace std;

 // } Driver Code Ends
class Solution{


	public:
	int minNum(long long int arr[],int n)
	{
	    // Your code goes here
	    long long int sum = 0;
	    
	    for(int i = 0; i < n; i++){
	        sum += arr[i];
	    }
	    
	    if(sum % 2 == 0)
	       return 2; // to make sum even min. no added is 2
	    else
	       return 1; // if sum is odd min. no added is 1
  }		 

};
	

// { Driver Code Starts.


int main() 
{
   	
   	int t;
    cin >> t;
    while (t--)
    {
    	 int n;
        cin>>n;
        
        long long a[n];
        for(int i=0; i<n; i++)
            cin>>a[i];
        
        
        
      
        Solution ob;
		cout << ob.minNum(a, n);
        
	    cout << "\n";
	     
    }
    return 0;
}
  // } Driver Code Ends
```

# [balanced array](https://practice.geeksforgeeks.org/problems/balanced-array07200720/1/?category[]=Arrays&category[]=Arrays&problemStatus=solved&difficulty[]=-1&page=1&query=category[]ArraysproblemStatussolveddifficulty[]-1page1category[]Arrays)
```cpp
// { Driver Code Starts
#include <bits/stdc++.h>
#include<stdio.h>
#include<math.h>
using namespace std;

 // } Driver Code Ends
class Solution
{
public:
    int minValueToBalance(int a[], int n)
    {
       //code here.
       int sumLeft = 0, sumRight = 0;
       
        for(int i = 0; i < n/2; i++){
               sumLeft += a[i];
        }
        for(int i = n/2; i < n; i++){
               sumRight += a[i];
        }
       
    return abs(sumLeft - sumRight); // min. no added to each element to make array balanced
       
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
		for(int i=0;i<n;++i)
			cin>>a[i];
		Solution ob;	
		cout<<ob.minValueToBalance(a,n)<<endl;
	}
	return 0;
}  // } Driver Code Ends
```

# [fighting the darkness](https://practice.geeksforgeeks.org/problems/fighting-the-darkness3949/1/?category[]=Arrays&category[]=Arrays&problemStatus=solved&difficulty[]=-1&page=1&query=category[]ArraysproblemStatussolveddifficulty[]-1page1category[]Arrays)
```cpp
// { Driver Code Starts
//Initial template for C++

#include <bits/stdc++.h>
using namespace std;

 // } Driver Code Ends
//User function template for C++

class Solution{   
public:
    int maxDays(int arr[],int n){
        // code here
        return *max_element(arr,arr + n);
    }
};

// { Driver Code Starts.

int main() 
{
    int t;
    cin >> t;
    while (t--)
    {
        int n;
        cin>>n;
        int arr[n];
        for(int i=0;i<n;i++)
            cin>>arr[i];
        Solution ob;
        cout << ob.maxDays(arr, n) << "\n";
    }
    return 0;
}  // } Driver Code Ends
```

# [max in struct array](https://practice.geeksforgeeks.org/problems/maximum-in-struct-array/1/?category[]=Arrays&category[]=Arrays&problemStatus=solved&difficulty[]=-1&page=1&query=category[]ArraysproblemStatussolveddifficulty[]-1page1category[]Arrays)
```cpp
// { Driver Code Starts
#include <bits/stdc++.h>
using namespace std;

struct Height {
	int feet;
	int inches;
};

int findMax(Height arr[], int n);

// driver program
int main()
{
	int t;
	cin>>t;
	while(t--)
	{
	    int n, tmp1, tmp2;
	    cin>>n;
	    Height arr[n];
	    for(int i=0; i<n; i++)
	    {
	        cin>>tmp1>>tmp2;
	        arr[i].feet = tmp1;
	        arr[i].inches = tmp2;
	    }
	    int res = findMax(arr, n);
	    cout<<res<<endl;
	}
	return 0;
}// } Driver Code Ends


/*
Structure of the element of the array is as
struct Height {
	int feet;
	int inches;
};
*/
// function must return the maximum Height
// return the height in inches
int findMax(Height arr[], int n)
{
    // Code here
    int res = INT_MIN;
    
    for(int i = 0; i < n; i++){
        res = max(res, arr[i].feet * 12 + arr[i].inches); // since 1 feet = 12 inches
    }
    
    return res;
    
}
```

# [no. of occurrence](https://practice.geeksforgeeks.org/problems/number-of-occurrence2259/1/?category[]=Arrays&category[]=Arrays&problemStatus=solved&difficulty[]=-1&page=1&query=category[]ArraysproblemStatussolveddifficulty[]-1page1category[]Arrays)
```cpp
/ { Driver Code Starts


#include<bits/stdc++.h>

using namespace std;


 // } Driver Code Ends
//User function template for C++
class Solution{
public:	
	/* if x is present in arr[] then returns the count
		of occurrences of x, otherwise returns 0. */
	int count(int arr[], int n, int x) {
	    // code here
	    int count = 0;
	    for(int i = 0; i < n; i++){
	        if(arr[i] == x){
	            count++;
	        }
	    }
	    return count;
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
        auto ans = ob.count(arr, n, x);
        cout << ans << "\n";
    }
    return 0;
```

# [k largest elements](https://practice.geeksforgeeks.org/problems/k-largest-elements4206/1/?category[]=Arrays&category[]=Arrays&problemStatus=solved&difficulty[]=-1&page=1&query=category[]ArraysproblemStatussolveddifficulty[]-1page1category[]Arrays)
```cpp
// { Driver Code Starts
#include <bits/stdc++.h>

using namespace std;


 // } Driver Code Ends
//User function template for C++
class Solution{
public:	
	vector<int> kLargest(int arr[], int n, int k) {
	    // code here
	    sort(arr,arr + n); // after sorting smallest element at first and largest element at last 
	    reverse(arr,arr + n); // after reverse largest element at first and then next largest and so on
	    vector<int> num;
	    for(int i = 0; i < k; i++){ // run from 0 to kth element
	        num.push_back(arr[i]);
	        
	    }
	    return num;
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
        auto ans = ob.kLargest(arr, n, k);
        for (auto x : ans) {
            cout << x << " ";
        }
        cout << "\n";
    }
    return 0;
}
  // } Driver Code Ends
```

# [total count](https://practice.geeksforgeeks.org/problems/total-count2415/1/?category[]=Arrays&category[]=Arrays&problemStatus=solved&difficulty[]=-1&page=1&query=category[]ArraysproblemStatussolveddifficulty[]-1page1category[]Arrays)
```cpp
// { Driver Code Starts
//Initial template for C++

#include <bits/stdc++.h>
using namespace std;

 // } Driver Code Ends
//User function template for C++

class Solution{   
public:
    int totalCount(int arr[], int n, int k) {
        // code here
        int sum = 0;
        
        for(int i = 0; i < n; i++)
        { 
           if(arr[i]%k == 0)
            {
                sum += arr[i]/k;
            }
            else
            {
                sum += (arr[i]/k) + 1;
            }
        }
        
        return sum;
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
        auto ans = ob.totalCount(arr, n, k);
        cout << ans << "\n";
    }
    return 0;
}

  // } Driver Code Ends
```

# [play with an array](https://practice.geeksforgeeks.org/problems/play-with-an-array/1/?category[]=Arrays&category[]=Arrays&problemStatus=solved&difficulty[]=-1&page=1&query=category[]ArraysproblemStatussolveddifficulty[]-1page1category[]Arrays)
```cpp
// { Driver Code Starts
#include<bits/stdc++.h>
using namespace std;
vector<int> formatArray(vector<int> a,int n);
int main(){
	int t;
	cin>>t;
	while(t--){
		int n;
		cin>>n;
		vector<int> a(n);
		for(int i=0;i<n;i++)
			cin>>a[i];
		vector<int>  b;
		b=formatArray(a,n);
		int flag=1;
		if(b.size()==n){
			for(int i=1;i<n;i+=2)
				if(b[i]<b[i-1])
					flag=0;
			if(flag==0)
				cout<<"0\n";
			else{
				sort(a.begin(),a.end());
				sort(b.begin(),b.end());
				for(int i=0;i<n;i++){
					if(a[i]!=b[i])
						flag=0;
				}
				cout<<flag<<endl;
			}
		}
		else
			cout<<"0\n";
	}
}// } Driver Code Ends


/*Complete the function below*/
vector<int> formatArray(vector<int> a,int n)
{
//add code here.
 for(int i = 1; i < n; i += 2) // i = 1,3,5,...
    {
        if(a[i-1] > a[i]) // i = 0,2,4,... > i = 1,3,5,...
        {
            swap(a[i-1], a[i]); // since condition not satisfied swap
        }
    }
    
    return a;
}
```

# [replace all 0's with 5](https://practice.geeksforgeeks.org/problems/replace-all-0s-with-5/1/?category[]=Arrays&category[]=Arrays&problemStatus=solved&difficulty[]=-1&page=1&query=category[]ArraysproblemStatussolveddifficulty[]-1page1category[]Arrays)
```cpp
// { Driver Code Starts
#include <bits/stdc++.h>
using namespace std;

int convertFive(int n);

// Driver program to test above function
int main() {
    int T;
    cin >> T;
    while (T--) {
        int n;
        cin >> n;
        cout << convertFive(n) << endl;
    }
}// } Driver Code Ends


/*you are required to complete this method*/
int convertFive(int n) {
    // Your code here
    if(n == 0) return 0; // number is 0 
    
    int lastDigit = n % 10;
    if(lastDigit == 0) lastDigit = 5; // replace last digit with 5 if 0
    
    return convertFive(n / 10) * 10 + lastDigit; // now function takes another digit
}
```

# [binary array sorting](https://practice.geeksforgeeks.org/problems/binary-array-sorting5355/1/?category[]=Arrays&category[]=Arrays&problemStatus=solved&difficulty[]=-1&page=1&query=category[]ArraysproblemStatussolveddifficulty[]-1page1category[]Arrays)
```cpp
// { Driver Code Starts
//Initial template for C++

#include <bits/stdc++.h> 
using namespace std;

 // } Driver Code Ends
//User function template for C++

// binArray is an array that consists only 0s and 1s
// return sorted binary array 
class Solution{
    public:
    vector<int> SortBinaryArray(vector<int> binArray)
    {
        // Your code goes here 
        int j = 0;
        
        for(int i = 0; i < binArray.size(); i++){
            if(binArray[i] == 0){ 
                swap(binArray[i],binArray[j]);
                j++;
            }
        }
        return binArray;
    }
};

// { Driver Code Starts.
int main() {
	int t;
	cin>>t;
	
	while(t--)
	{
	    int n;
	    cin>>n;
	    vector<int> binArray(n);
	    
	    for(int i = 0; i  < n; i++)
	      cin>>binArray[i];
	    Solution ob;  
	  	vector<int> result = ob.SortBinaryArray(binArray);
	  	for(int i=0; i<n; i++)
	  	    cout<<result[i]<<" ";
	      
	    cout<<endl;
	}
	return 0;
}
```

# [reverse array in groups](https://practice.geeksforgeeks.org/problems/reverse-array-in-groups0255/1/?category[]=Arrays&category[]=Arrays&problemStatus=solved&difficulty[]=-1&page=2&query=category[]ArraysproblemStatussolveddifficulty[]-1page2category[]Arrays)
```cpp
// { Driver Code Starts
//Initial template for C++

#include <bits/stdc++.h>
using namespace std;


 // } Driver Code Ends
//User function template for C++

class Solution{
public:
    //Function to reverse every sub-array group of size k.
    void reverseInGroups(vector<long long>& arr, int n, int k){
        // code here
        for (int i = 0; i < n; i += k){
            int left = i;
            int right = min(i + k - 1, n - 1);
            
            while (left < right)
                  swap(arr[left++], arr[right--]);

        }
    }
};

// { Driver Code Starts.
int main() {
    int t; 
    cin >> t; 
    while(t--){ 
        int n;
        cin >> n; 
        vector<long long> arr; 
        int k;
        cin >> k; 

        for(long long i = 0; i<n; i++)
        {
            long long x;
            cin >> x; 
            arr.push_back(x); 
        }
        Solution ob;
        ob.reverseInGroups(arr, n, k);
        
        for(long long i = 0; i<n; i++){
            cout << arr[i] << " "; 
        }
        cout << endl;
    }
}

  // } Driver Code Ends
```

# [minimize the sum of product](https://practice.geeksforgeeks.org/problems/minimize-the-sum-of-product1525/1/?category[]=Arrays&category[]=Arrays&problemStatus=solved&difficulty[]=-1&page=1&query=category[]ArraysproblemStatussolveddifficulty[]-1page1category[]Arrays)
```cpp
// { Driver Code Starts
#include<bits/stdc++.h>
using namespace std;

 // } Driver Code Ends

class Solution{
    public:
    long long int minValue(int a[], int b[], int n)
    {
        // Your code goes here
        long long int sum = 0;
        
        sort(a,a + n); // smallest to largest since asc sort
        sort(b,b + n,greater<int>()); // largest to smallest since des sort
        for(int i = 0; i < n; i ++){
            sum += (a[i] * b[i]);
        }
        return sum;
    }
};

// { Driver Code Starts.
int main()
 {
     int t;
     cin>>t;
     while(t--)
     {
         int n, i;
         cin>>n;
         int a[n], b[n];
         for(i=0;i<n;i++)
         cin>>a[i];
         for(i=0;i<n;i++)
         cin>>b[i];
         Solution ob;
         cout<< ob.minValue(a, b, n) <<endl;
     }
	
	return 0;
}  // } Driver Code Ends
```

# [find no. of numbers](https://practice.geeksforgeeks.org/problems/find-number-of-numbers/1/?category[]=Arrays&category[]=Arrays&problemStatus=solved&difficulty[]=-1&page=2&query=category[]ArraysproblemStatussolveddifficulty[]-1page2category[]Arrays)
```cpp
// { Driver Code Starts
#include<iostream>
using namespace std;
int num(int a[], int n, int k);
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
		{
			cin>>a[i];
		}
		int k;
		cin>>k;
		cout<<num(a,n,k)<<endl;
	}
}// } Driver Code Ends


/*Complete the function given below*/
int num(int a[], int n, int k)
{
     //add code here.
     int count = 0;
     
     for(int i = 0; i < n; i++){
         
         while(a[i] > 0){ // while the number > 0
            
             
             if((a[i] % 10) == k) // if last digit i.e a[i] % 10 for each number in array is k then count increments
                count++;
                
             a[i] = a[i] / 10;  // we go to remaining digits of each element in array    
         }
     }
     return count;
}
```

# [index of first 1 in a sorted array of 0's and 1's](https://practice.geeksforgeeks.org/problems/index-of-first-1-in-a-sorted-array-of-0s-and-1s4048/1/?category[]=Arrays&category[]=Arrays&problemStatus=solved&difficulty[]=-1&page=2&query=category[]ArraysproblemStatussolveddifficulty[]-1page2category[]Arrays)
```cpp
// { Driver Code Starts
#include <bits/stdc++.h>
using namespace std;

 // } Driver Code Ends
class Solution{
    public:
    int firstIndex(int a[], int n) 
    {
        // Your code goes here
        
        for(int i = 0; i < n; i++){
            if(a[i] == 1){
                return i;
            }
               
        }        
        return -1;       
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
        cout << ob.firstIndex(a, n) << endl;
    }
}  // } Driver Code Ends
```

# [binary array sorting](https://practice.geeksforgeeks.org/problems/binary-array-sorting-1587115620/1/?category[]=Arrays&category[]=Arrays&problemStatus=solved&difficulty[]=-1&page=2&query=category[]ArraysproblemStatussolveddifficulty[]-1page2category[]Arrays)
```cpp
// { Driver Code Starts
// A Sample C++ program for beginners with Competitive Programming

#include <bits/stdc++.h>
using namespace std;

 // } Driver Code Ends
class Solution{
  public:
    
    // A[]: input array
    // N: input array
    //Function to sort the binary array.
    void binSort(int A[], int N)
    {
       //Your code here
       
       /**************
        * No need to print the array
        * ************/
        
        int count0 = 0;
        
        for(int i = 0; i < N; i++){
            if(A[i] == 0){
                count0++;
            }
        }
        
        for(int i = 0; i < count0; i++){
            A[i] = 0;
        }
        
        for(int i = count0; i < N; i++){
            A[i] = 1;
        }
    }
};

// { Driver Code Starts.
int main() {
	int T;
	cin>>T;
	// Input the number of testcases
	while(T--)
	{
	    int N;
	    cin>>N; //Input size of array N
	    int A[N]; 
	    
	    for(int i = 0; i  < N; i++)
	      cin>>A[i];
	      
	    Solution obj;
	    obj.binSort(A,N);
	    
	    for(int x:A)
	    cout<<x<<" ";
	      
	    cout<<endl;
	}
	return 0;
}



  // } Driver Code Ends
```

# [implement stack using array](https://practice.geeksforgeeks.org/problems/implement-stack-using-array/1/?category[]=Arrays&category[]=Arrays&problemStatus=solved&difficulty[]=-1&page=2&query=category[]ArraysproblemStatussolveddifficulty[]-1page2category[]Arrays)
```cpp
// { Driver Code Starts
#include<bits/stdc++.h>
using namespace std;

class MyStack
{
private:
    int arr[1000];
    int top;
public:
    MyStack(){top=-1;}
    int pop();
    void push(int);
};


int main()
{

    int T;
    cin>>T;
    while(T--)
    {
        MyStack *sq = new MyStack();

        int Q;
        cin>>Q;
        while(Q--){
        int QueryType=0;
        cin>>QueryType;
        if(QueryType==1)
        {
            int a;
            cin>>a;
            sq->push(a);
        }else if(QueryType==2){
            cout<<sq->pop()<<" ";

        }
        }
        cout<<endl;
    }
}
// } Driver Code Ends



//Function to push an integer into the stack.
void MyStack :: push(int x)
{
    // Your Code
    arr[++top] = x;
}

//Function to remove an item from top of the stack.
int MyStack :: pop()
{
    // Your Code 
    if(top != -1)
       return arr[top--];
    else
       return -1;
}
```

# [search an element in an array](https://practice.geeksforgeeks.org/problems/search-an-element-in-an-array-1587115621/1/?category[]=Arrays&category[]=Arrays&problemStatus=solved&difficulty[]=-1&page=2&query=category[]ArraysproblemStatussolveddifficulty[]-1page2category[]Arrays)
```cpp
// { Driver Code Starts
#include<bits/stdc++.h>
using namespace std;


 // } Driver Code Ends
class Solution{
    public:
    // Function to search x in arr
    // arr: input array
    // X: element to be searched for
    int search(int arr[], int N, int X)
    {
        
        // Your code here
        for(int i = 0; i < N; i++){
            if(arr[i] == X){
                return i;
            }
        }
        return -1;
        
    }

};

// { Driver Code Starts.

int main()
{
    int testcases;
    cin>>testcases;
    while(testcases--)
    {
        int sizeOfArray;
        cin>>sizeOfArray;
        int arr[sizeOfArray];
        int x;
        
        for(int i=0;i<sizeOfArray;i++)
        {
            cin>>arr[i];
        }
        cin>>x;
        Solution ob;
        cout<<ob.search(arr,sizeOfArray,x)<<endl; //Linear search
    }

    return 0;
    
}
  // } Driver Code Ends
```

# [check if two arrays are equal or not](https://practice.geeksforgeeks.org/problems/check-if-two-arrays-are-equal-or-not3847/1/?category[]=Arrays&category[]=Arrays&problemStatus=solved&difficulty[]=-1&page=2&query=category[]ArraysproblemStatussolveddifficulty[]-1page2category[]Arrays)
```cpp
// { Driver Code Starts
//Initial function template for C++

#include<bits/stdc++.h>
using namespace std;
#define ll long long 

 // } Driver Code Ends
//User function template for C++

class Solution{
    public:

    //Function to check if two arrays are equal or not.
    bool check(vector<ll> A, vector<ll> B, int N) {
        //code here
        sort(A.begin(),A.end());
        sort(B.begin(),B.end());
        
        if(A == B)
           return 1;
        else
           return 0;
    }
};

// { Driver Code Starts.
int main()
 {
    int t;
    cin>>t;
    while(t--) {
        int n;
        cin>>n;
        
        vector<ll> arr(n,0),brr(n,0);
        
        // increase the count of elements in first array
        for(ll i=0;i<n;i++)
            cin >> arr[i];
        
        
        // iterate through another array
        // and decrement the count of elements
        // in the map in which frequency of elements
        // is stored for first array
        for(ll i=0;i<n;i++)
            cin >> brr[i];
        Solution ob;
        cout << ob.check(arr,brr,n) << "\n";
    }
	return 0;
}  // } Driver Code Ends
```

# [convert array into zig-zag fashion](https://practice.geeksforgeeks.org/problems/convert-array-into-zig-zag-fashion1638/1/?category[]=Arrays&category[]=Arrays&problemStatus=solved&difficulty[]=-1&page=2&query=category[]ArraysproblemStatussolveddifficulty[]-1page2category[]Arrays)
```cpp
// { Driver Code Starts
#include <bits/stdc++.h>

using namespace std;


 // } Driver Code Ends
//User function template for C++
class Solution{
public:	
	// Program for zig-zag conversion of array
	void zigZag(int arr[], int n) {
	    // code here
	    for(int i = 0; i < n-1; i++)
        {
            if(i%2 == 0) // At any even index (0/2/4) , the value is lesser than its neighbours
            {
                if(arr[i] > arr[i+1]) // since the value is not lesser than its neighbours
                {
                    swap(arr[i], arr[i+1]); // swap
                }
            }
            else // At any odd index (1/3/5) , the value is greater than its neighbours
            {
                if(arr[i] < arr[i+1]) // since the value is not greater than its neighbours
                {
                    swap(arr[i], arr[i+1]); // swap
                }
            }
        }
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
        ob.zigZag(arr, n);
        for (int i = 0; i < n; i++) {
            cout << arr[i] << " ";
        }
        cout << "\n";
    }
    return 0;
}
  // } Driver Code Ends
```

# [last index of one](https://practice.geeksforgeeks.org/problems/last-index-of-15847/1/?category[]=Arrays&category[]=Arrays&problemStatus=solved&difficulty[]=-1&page=2&query=category[]ArraysproblemStatussolveddifficulty[]-1page2category[]Arrays)
```cpp
// { Driver Code Starts
#include <bits/stdc++.h>
using namespace std;


 // } Driver Code Ends

class Solution{
    public:
    int lastIndex(string s) 
    {
        for(int i = s.size() - 1; i >=0; i--){
            if(s[i] == '1'){
                return i;
            }
        }
        return -1;
    }

};

// { Driver Code Starts.

int main() {
    long long t;
    cin >> t;
    while (t--) {
        string s;
        cin >> s;
        Solution ob;
        cout << ob.lastIndex(s) << endl;
    }
    return 0;
}  // } Driver Code Ends
```

# [exceptionally odd](https://practice.geeksforgeeks.org/problems/find-the-odd-occurence4820/1/?category[]=Arrays&category[]=Arrays&problemStatus=solved&difficulty[]=-1&page=2&query=category[]ArraysproblemStatussolveddifficulty[]-1page2category[]Arrays)
```cpp
// { Driver Code Starts
//Initial template for C++

#include <bits/stdc++.h>
using namespace std;

 // } Driver Code Ends
//User function template for C++

class Solution{   
public:
    int getOddOccurrence(int arr[], int n) {
        // code here
        int res = arr[0];
        
        for(int i = 1; i < n; i++){
            res = res ^ arr[i]; // XOR of same element is 0
        }
        return res;
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
        auto ans = ob.getOddOccurrence(arr, n);
        cout << ans << "\n";
    }
    return 0;
}

  // } Driver Code Ends
```

# [implement queue using array](https://practice.geeksforgeeks.org/problems/implement-queue-using-array/1/?category[]=Arrays&category[]=Arrays&problemStatus=solved&difficulty[]=-1&page=2&query=category[]ArraysproblemStatussolveddifficulty[]-1page2category[]Arrays)
```cpp
// { Driver Code Starts
#include<bits/stdc++.h>
using namespace std;

struct QueueNode
{
    int data;
    QueueNode *next;
};

class MyQueue {
private:
    int arr[100005];
    int front;
    int rear;

public :
    MyQueue(){front=0;rear=0;}
    void push(int);
    int pop();
};

int main()
{
    int T;
    cin>>T;
    while(T--)
    {
        MyQueue *sq = new MyQueue();

        int Q;
        cin>>Q;
        while(Q--){
        int QueryType=0;
        cin>>QueryType;
        if(QueryType==1)
        {
            int a;
            cin>>a;
            sq->push(a);
        }else if(QueryType==2){
            cout<<sq->pop()<<" ";

        }
        }
        cout<<endl;
    }
    }
// } Driver Code Ends


/* 
The structure of the class is
class MyQueue {
private:
    int arr[100005];
    int front;
    int rear;
public :
    MyQueue(){front=0;rear=0;}
    void push(int);
    int pop();
};
 */

//Function to push an element x in a queue.
void MyQueue :: push(int x)
{
        // Your Code
        arr[rear++] = x; // new element "x" pushed at rear and move backward from rear
        
}

//Function to pop an element from queue and return that element.
int MyQueue :: pop()
{
        // Your Code 
        if(front >= rear){ // when queue is empty
            return -1;
        }
        return arr[front++]; // otherwise move forward from front
}
```

# [find triplets with zero sum](https://practice.geeksforgeeks.org/problems/find-triplets-with-zero-sum/1/?category[]=Arrays&category[]=Arrays&problemStatus=solved&difficulty[]=-1&page=2&query=category[]ArraysproblemStatussolveddifficulty[]-1page2category[]Arrays)
```cpp
// { Driver Code Starts
#include<bits/stdc++.h>
#include<stdlib.h>
#include<iostream>
using namespace std;

 // } Driver Code Ends
/* You are required to complete the function below
*  arr[]: input array
*  n: size of array
*/
class Solution{
  public:
    //Function to find triplets with zero sum.
    bool findTriplets(int arr[], int n)
    { 
        //Your code here
        sort(arr,arr + n);
        
        for(int i = 0; i < n; i++){
            int j = i + 1;
            int k = n - 1;
            
            while(j < k){ // next index < last index
                int tripletSum = arr[i] + arr[j] + arr[k];
                
                if(tripletSum == 0){
                    return 1;
                } else if(tripletSum < 0){
                    j++; // i + 1 further incremented
                } else{
                    k--; // n - 1 further decremented
                }
            }
        }
        return 0;
    }
};

// { Driver Code Starts.
int main()
{
    int t;
	cin>>t;
	while(t--){
    	int n;
    	cin>>n;
    	int arr[n]={0};
    	for(int i=0;i<n;i++)
    		cin>>arr[i];
    	Solution obj;
        if(obj.findTriplets(arr, n))
            cout<<"1"<<endl;
        else 
            cout<<"0"<<endl;
	}
    return 0;
}  // } Driver Code Ends
```

# [sum array puzzle](https://practice.geeksforgeeks.org/problems/sum-array-puzzle/1/?category[]=Arrays&category[]=Arrays&problemStatus=solved&difficulty[]=-1&page=2&query=category[]ArraysproblemStatussolveddifficulty[]-1page2category[]Arrays)
```cpp
// { Driver Code Starts
//Initial Template for C++

#include <bits/stdc++.h>
using namespace std;

void SumArray(int[], int);

 // } Driver Code Ends
//User function Template for C++

// arr is the array
// n is the number of element in array
void SumArray(int arr[], int n)
{
    // you code here
    int sum = 0;
    
    // accumulate(first, last, sum);
    // first, last : first and last elements of range whose elements are to be added
    // sum :  initial value of the sum
    sum = accumulate(arr,arr + n,sum);
    
    for(int i = 0; i < n; i++){
        arr[i] = sum - arr[i]; // sum of all elements - ith element from arr[i]
    }
}

// { Driver Code Starts.
int main()
{
    int t;
    cin>>t;

    while(t--)
    {
        int n;
        cin>>n;

        int arr[n];
        for(int i = 0; i < n; i++)
          cin>>arr[i];

         SumArray(arr, n);
         for(int i = 0; i < n; i++)
            cout << arr[i] <<" ";

             
        cout <<endl;
    }
    return 0;
}  // } Driver Code Ends
```

# [first and last occurrences of X](https://practice.geeksforgeeks.org/problems/first-and-last-occurrences-of-x2041/1/?category[]=Arrays&category[]=Arrays&problemStatus=solved&difficulty[]=-1&page=3&query=category[]ArraysproblemStatussolveddifficulty[]-1page3category[]Arrays)
```cpp
// { Driver Code Starts
#include <bits/stdc++.h>
using namespace std;

 // } Driver Code Ends
class Solution {
  public:
    vector<int> firstAndLast(vector<int> &arr, int n, int x) {
        // Code here
         if(binary_search(arr.begin(), arr.end(), x))
        {
            auto leftMost  = lower_bound(arr.begin(), arr.end(), x);
            auto rightMost = upper_bound(arr.begin(), arr.end(), x);
            
            return {leftMost - arr.begin(), rightMost - arr.begin() - 1};
        }
        
        return {-1};
    }
};

// { Driver Code Starts.

int main() {
    int t;
    cin >> t;
    while (t--) {
        int n, x;
        cin >> n >> x;
        vector<int> arr(n);
        for (int i = 0; i < n; i++) {
            cin >> arr[i];
        }

        Solution obj;
        vector<int> ans= obj.firstAndLast(arr, n, x) ;
        for(int i:ans){
            cout<<i<<" ";
        }
        cout<< endl;
    }
    return 0;
}
  // } Driver Code Ends
```

# [face off tournament](https://practice.geeksforgeeks.org/problems/multiple-in-table-tennis3310/1/?category[]=Arrays&category[]=Arrays&problemStatus=solved&difficulty[]=-1&page=3&query=category[]ArraysproblemStatussolveddifficulty[]-1page3category[]Arrays)
```cpp
// { Driver Code Starts
// Initial Template for C++

#include <bits/stdc++.h>
using namespace std;

 // } Driver Code Ends
// User function Template for C++

class Solution{
public:
    string winner(int x, int m, int n, long long int arr[])
    {
        // code here
        int countRam = 0,countRohan = 0;
        
        for(int i = 0; i < x; i++){
            if(arr[i] % m == 0){
                countRam++;
            }
            else if(arr[i] % n == 0){
                countRohan++;
            }
        }
        
        if(countRam > countRohan){
            return "Ram";
        }
        if(countRam < countRohan){
            return "Rohan";
        }
        if(countRam == countRohan){
            return "Both";
        }
    }
};

// { Driver Code Starts.

int main(){
    int t;
    cin>>t;
    while(t--){
        int x, m, n;
        cin>>x>>m>>n;
        long long arr[x];
        for(int i = 0;i < x;i++)
            cin>>arr[i];
        
        Solution ob;
        cout<<ob.winner(x, m, n, arr)<<"\n";
    }
    return 0;
}  // } Driver Code Ends
```

# [C++ 2D arrays | Set - 2](https://practice.geeksforgeeks.org/problems/c-2-d-arrays-set-22255/1/?category[]=Arrays&category[]=Arrays&problemStatus=solved&difficulty[]=-1&page=3&query=category[]ArraysproblemStatussolveddifficulty[]-1page3category[]Arrays)
```cpp
// { Driver Code Starts
#include<bits/stdc++.h>
using namespace std;



 // } Driver Code Ends


class Solution{
  public:
    vector<vector<int>> final_matrix(vector<vector<int>> &a, int n)
    {
        // Code here
        queue<pair<int,int>>q;
        for(int i=0;i<n;i++)
        {
            for(int j=0;j<n;j++)
            {
                if(a[i][j]==0)
                    q.push(make_pair(i,j));
            }
        }
        while(!q.empty())
        {   
            pair<int,int>p=q.front();
            q.pop();
            for(int i=0;i<n;i++)
                a[p.first][i]=0;
            for(int i=0;i<n;i++)
                a[i][p.second]=0;
        }
        vector<vector<int>> ans(a.size());
        for(int i=0;i<n;i++)
        {
            for(int j=0;j<n;j++)
                ans[i].push_back(a[i][j]);
        }
        return ans;
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
        vector<vector<int>> a(n, vector<int>(n));
        for(int i=0;i<n;i++){
            for(int j=0;j<n;j++){
                cin >> a[i][j];
            }
        }
        
        vector<vector<int>> ans;
        Solution obj;
        ans = obj.final_matrix(a, n);
        for(int i=0;i<n;i++){
            for(int j=0;j<n;j++){
                cout << ans[i][j]<<" ";
            }
            cout << endl;
        }
        
    }
}

  // } Driver Code Ends
```

# [permutations in array](https://practice.geeksforgeeks.org/problems/permutations-in-array1747/1/?category[]=Arrays&category[]=Arrays&problemStatus=solved&difficulty[]=-1&page=2&query=category[]ArraysproblemStatussolveddifficulty[]-1page2category[]Arrays)
```cpp
// { Driver Code Starts
#include <bits/stdc++.h>
using namespace std;

 // } Driver Code Ends

class Solution {
  public:
    bool isPossible(long long a[], long long b[], long long n, long long k) {
        // Your code goes here
        sort(a, a + n); // asc sort
        sort(b, b + n, greater<int>()); // desc sort
        
        for(int i = 0; i < n; i++)
        {
            if(a[i] + b[i] >= k)
            {
                return true;
            }
        }
        
        return false;
    }
};

// { Driver Code Starts.
int main() {
    long long t;
    cin >> t;
    while (t--) {
        long long n, k;
        cin >> n >> k;
        long long a[n + 2], b[n + 2];
        for (int i = 0; i < n; i++) cin >> a[i];
        for (int i = 0; i < n; i++) cin >> b[i];
        Solution ob;
        cout << ob.isPossible(a, b, n, k) << endl;
    }
    return 0;
}
  // } Driver Code Ends
```

# [rearrange the array](https://practice.geeksforgeeks.org/problems/rearrange-the-array5802/1/?category[]=Arrays&category[]=Arrays&problemStatus=solved&difficulty[]=-1&page=2&query=category[]ArraysproblemStatussolveddifficulty[]-1page2category[]Arrays)
```cpp
  
// { Driver Code Starts
#include <bits/stdc++.h>

using namespace std;



 // } Driver Code Ends

class Solution{
  public:
    void rearrangeArray(int arr[], int n) {
        // code here
        int temp[n];
        for(int i = 0; i < n; i++){
            temp[i] = arr[i];
        }
        
        sort(temp,temp + n); // smallest,largest,2nd smallest,2nd largest,...
        
        int start = 0;
        int end = n - 1;
        int count = 0;
        
        while(start <= end){
            arr[count++] = temp[start++];
            arr[count++] = temp[end--];
        }
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
        Solution obj;
        obj.rearrangeArray(arr, n);
        for (int i = 0; i < n; i++) {
            cout << arr[i] << " ";
        }
        cout << "\n";
    }
    return 0;
}
  // } Driver Code Ends
```

# [a guy with a mental problem](https://practice.geeksforgeeks.org/problems/a-guy-with-a-mental-problem1604/1/?category[]=Arrays&category[]=Arrays&problemStatus=solved&difficulty[]=-1&page=2&query=category[]ArraysproblemStatussolveddifficulty[]-1page2category[]Arrays)
```cpp
// { Driver Code Starts
#include <bits/stdc++.h>
using namespace std;

 // } Driver Code Ends

class Solution{
    public:
    long long minTime(long long a[], long long b[], long long n)
    {
        // Your code goes here
        long long sum1 = a[0],sum2 = b[0];
        
        for(long long i = 1; i < n; i++) {
            if(i % 2 == 0){ // ABAB...
                sum1 += a[i];
                sum2 += b[i];
            }
            else{          // BABA...
                sum1 += b[i]; 
                sum2 += a[i];
            }
            
        }
        
       return min(sum1,sum2);
    }
};

// { Driver Code Starts.
int main() {
    long long t;
    cin>>t;
    while(t--)
    {
        long long n;
        cin >> n;
        long long a[n], b[n];
        for(long long i=0;i<n;i++)
            cin >> a[i];
        for(long long i=0;i<n;i++)
            cin >> b[i];
        Solution ob;
        cout << ob.minTime(a, b, n) << endl;
    }
    return 0;
}
  // } Driver Code Ends
```

# [max triplet sum in array](https://practice.geeksforgeeks.org/problems/maximum-triplet-sum-in-array0129/1/?category[]=Arrays&category[]=Arrays&problemStatus=solved&difficulty[]=-1&page=2&query=category[]ArraysproblemStatussolveddifficulty[]-1page2category[]Arrays)
```cpp
// { Driver Code Starts
#include <bits/stdc++.h>
using namespace std;

 // } Driver Code Ends


class Solution{
    public:
    int maxTripletSum(int arr[], int n)
    {
    	// Complete the function
    	sort(arr,arr + n); // after sorting last three elements are largest
    	int sum = arr[n - 1] + arr[n - 2] + arr[n - 3]; // sum of three largest elements is largest
    	return sum;
    }
};

// { Driver Code Starts.
int main()
{
	int t;
	cin>>t;
	while(t--)
	{
	    int n,i;
	    cin>>n; int a[n];
	    for(i=0;i<n;i++)
	    cin>>a[i];
	    Solution ob;
	    cout <<ob.maxTripletSum(a, n);
	    cout<<"\n";
	}
return 0;
}  // } Driver Code Ends
```

# [third largest element](https://practice.geeksforgeeks.org/problems/third-largest-element/1/?category[]=Arrays&category[]=Arrays&problemStatus=solved&difficulty[]=-1&page=2&query=category[]ArraysproblemStatussolveddifficulty[]-1page2category[]Arrays)
```cpp
// { Driver Code Starts
#include<bits/stdc++.h>
using namespace std;

 // } Driver Code Ends
class Solution{
  public:
    int thirdLargest(int a[], int n)
    {
         //Your code here
         sort(a,a + n);
         
         if(n < 3)
            return -1;
         else    
            return a[n - 3]; // after sorting in asc order, 3rd largest is one third from end
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
	   Solution obj;
	    cout<<obj.thirdLargest(a,n)<<endl;
    }
}   
```

# [smallest no. repeating K times](https://practice.geeksforgeeks.org/problems/smallest-number-repeating-k-times3239/1/?category[]=Arrays&category[]=Arrays&problemStatus=solved&difficulty[]=-1&page=2&query=category[]ArraysproblemStatussolveddifficulty[]-1page2category[]Arrays)
```cpp
// { Driver Code Starts
//Initial Template for C++



#include <bits/stdc++.h>
using namespace std;

 // } Driver Code Ends
//User function Template for C++


class Solution{
    public:
    int findDuplicate(int arr[], int N, int K) 
    { 
        long long int count[100000] = {0};
        
        for(int i = 0; i < N; i++){
            count[arr[i]] = count[arr[i]] + 1;
        }
        
        for(int i = 0; i < 100000; i++){
            if(count[i] == K){
                return i;
            }
        }
        return -1;
    
    }
};

// { Driver Code Starts.

int main() {
	int t;
	
	cin >> t;
	
	while(t--){
	    int n;
	    cin >> n;
	    int k;
	    cin >> k;
	    int a[n];
	    for(int i = 0;i<n;i++){
	        cin >> a[i];
	    }
	    Solution ob;
	    cout << ob.findDuplicate(a,n,k) << endl;
	    }
	return 0;
}
  // } Driver Code Ends
```

# [sort in specific order](https://practice.geeksforgeeks.org/problems/sort-in-specific-order2422/1/?category[]=Arrays&category[]=Arrays&problemStatus=solved&difficulty[]=-1&page=2&query=category[]ArraysproblemStatussolveddifficulty[]-1page2category[]Arrays)
```cpp
// { Driver Code Starts
#include <bits/stdc++.h>
using namespace std;

 // } Driver Code Ends
class Solution
{
  public:
    void sortIt(long long arr[], long long n)
    {
        //code here.
        int i,j;
        vector<long long> even, odd;
        
        for(i = 0; i < n; i++){ // storing even and odd elements in even and odd vectors respectively
            if(arr[i] % 2 == 0)
                even.push_back(arr[i]);
            
            else
                odd.push_back(arr[i]);
            
        }
        
       sort(even.begin(),even.end());
       sort(odd.begin(),odd.end());
       
       reverse(odd.begin(),odd.end()); // since we need desc sort for odd
       
       i = 0;
       for(i = 0; i < odd.size(); i++)
           arr[i] = odd[i];
       
       
       for(j = 0; j < even.size(); j++, i++)
           arr[i] = even[j];
       
    }
};

// { Driver Code Starts.
int main() {
    long long t;
    cin >> t;
    while (t--) {
        long long n;
        cin >> n;
        long long arr[n];

        for (int i = 0; i < n; i++) 
            cin >> arr[i];
        
        Solution ob;
        ob.sortIt(arr, n);

        for (int i = 0; i < n; i++)
            cout << arr[i] << " ";
        cout << endl;
    }
    return 0;
}  // } Driver Code Ends
```

# [check arithmetic progression](https://practice.geeksforgeeks.org/problems/check-arithmetic-progression1842/1/?category[]=Arrays&category[]=Arrays&problemStatus=solved&difficulty[]=-1&page=3&query=category[]ArraysproblemStatussolveddifficulty[]-1page3category[]Arrays)
```cpp
// { Driver Code Starts
#include<bits/stdc++.h>
using namespace std;

 // } Driver Code Ends


class Solution{
    public:
    bool checkIsAP(int arr[], int n)
    {
        // code here
        sort(arr,arr + n);
        
        int d = arr[1] - arr[0]; // common difference
        
        for(int i = 0; i < n - 1; i++){
            int d1 = arr[i + 1] - arr[i];
            if(d1 != d){
                return false;
            }
        }
        return true;
        
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
        int arr[n];
        for(int i=0;i<n;i++)
            cin>>arr[i];
        
        Solution ob;
         (ob.checkIsAP(arr, n))? (cout << "YES" << endl) :
                       (cout << "NO" << endl);   
    }
 
  return 0;
}
  // } Driver Code Ends
```

# []()
```cpp

```

# []()
```cpp

```

# []()
```cpp

```

# []()
```cpp

```

# []()
```cpp

```

# []()
```cpp

```

# []()
```cpp

```

# []()
```cpp

```

v# []()
```cpp

```

# []()
```cpp

```

# []()
```cpp

```

# []()
```cpp

```

# []()
```cpp

```

# []()
```cpp

```

# []()
```cpp

```

# []()
```cpp

```

# []()
```cpp

```

# []()
```cpp

```

# []()
```cpp

```

# []()
```cpp

```

# []()
```cpp

```

# []()
```cpp

```

