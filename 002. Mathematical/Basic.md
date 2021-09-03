[Matching Pair](https://practice.geeksforgeeks.org/problems/matching-pair5320/1/?category[]=Mathematical&category[]=Mathematical&problemStatus=unsolved&difficulty[]=-1&page=1&query=category[]MathematicalproblemStatusunsolveddifficulty[]-1page1category[]Mathematical)
```cpp
 Code Ends
class Solution{
public:
    int find(int N){ 
        // code here
        return N + 1;
    }
};

// { Driver Code Starts.
int main() 
{ 
    int t;
    cin>>t;
    while(t--)
    {
        int N;
        cin>>N;
        Solution ob;
        cout << ob.find(N) << endl;
    }
    return 0; 
}  // } Driver Code Ends
```

[Sum of product of x and y with floor(n/x) = y](https://practice.geeksforgeeks.org/problems/sum-of-product-of-x-and-y-with-floornx-y3711/1/?category[]=Mathematical&category[]=Mathematical&problemStatus=unsolved&difficulty[]=-1&page=1&query=category[]MathematicalproblemStatusunsolveddifficulty[]-1page1category[]Mathematical#)
```cpp
// { Driver Code Starts

#include<bits/stdc++.h>
using namespace std;

 // } Driver Code Ends

class Solution{
	public:
	long long int sumofproduct(int n)
	{
	    // Code here
	    long long int sum = 0;
	    for(int x = 1; x <= n; x++){
	        int y = n / x;
	        sum += x * y;
	    }
	    return sum;
	}  
};

// { Driver Code Starts.
int main(){
	int tc;
	cin >> tc;
	while(tc--){
		int n;
		cin >> n;
		Solution ob;
		long long int ans = ob.sumofproduct(n);
		cout << ans <<"\n";
	}  
	return 0;
}  // } Driver Code Ends
```

[Find N-th term in the series](https://practice.geeksforgeeks.org/problems/find-n-th-term-in-the-series3926/1/?category[]=Mathematical&category[]=Mathematical&problemStatus=unsolved&difficulty[]=-1&page=1&query=category[]MathematicalproblemStatusunsolveddifficulty[]-1page1category[]Mathematical)
```cpp
// { Driver Code Starts
// Initial Template for C++
#include <bits/stdc++.h>
using namespace std;

 // } Driver Code Ends
// User function Template for C++
class Solution {
  public:
    long long int nthOfSeries(long long int n){
        // code here
        return (8 * n * n) + 1;
    }
};

// { Driver Code Starts.
int main() {
    int t;
    cin >> t;
    while (t--) {
        long long int n;
        cin >> n;
        Solution ob;
        cout << ob.nthOfSeries(n) << endl;
    }
    return 0;
}
  // } Driver Code Ends
```

[Mind Game](https://practice.geeksforgeeks.org/problems/mind-game3637/1/?category[]=Mathematical&category[]=Mathematical&problemStatus=unsolved&difficulty[]=-1&page=1&query=category[]MathematicalproblemStatusunsolveddifficulty[]-1page1category[]Mathematical#)
```cpp
// { Driver Code Starts
#include <bits/stdc++.h>
using namespace std;

 // } Driver Code Ends
class Solution {
  public:
    int mindGame(int K) {
        // code here
/*
initially: N
Step 1: 2*N
Step 2: (2*N + K)
Step 3: (2*N + K)/2
Step 4: (2*N + K)/2 - N
=> (2*N + K - 2*N)/2
=> K/2
*/
     return K / 2;
        
    }
};

// { Driver Code Starts.
int main() {
    int t;
    cin >> t;
    while (t--) {
        int K;
        
        cin>>K;

        Solution ob;
        cout << ob.mindGame(K) << endl;
    }
    return 0;
}  // } Driver Code Ends
```

[Maximum Area](https://practice.geeksforgeeks.org/problems/maximum-area2642/1/?category[]=Mathematical&category[]=Mathematical&problemStatus=unsolved&difficulty[]=-1&page=1&query=category[]MathematicalproblemStatusunsolveddifficulty[]-1page1category[]Mathematical)
```cpp
// { Driver Code Starts
#include <bits/stdc++.h>
using namespace std;

 // } Driver Code Ends
class Solution {
  public:
    int getHypotenuse(long long N) {
        // code here
        /*
            Area:
            N = (A * B)/2 [A = B : to maximize the area]
            2*N = (A^2)
            
            Hypotenuse
            C = sqrt(A^2 + B^2) [A = B : to maximize the area]
            C = sqrt(2 * A^2)
            C = sqrt(2 * 2 * N) [(A^2) = 2*N]
            C = sqrt(4 * N)
        */
        return floor(sqrt(4 * N));
    }
};

// { Driver Code Starts.
int main() {
    int t;
    cin >> t;
    while (t--) {
        long long N;

        cin>>N;

        Solution ob;
        cout << ob.getHypotenuse(N) << endl;
    }
    return 0;
}  // } Driver Code Ends
```

[The Lazy Caterer's Problem](https://practice.geeksforgeeks.org/problems/the-lazy-caterers-problem2527/1/?category[]=Mathematical&category[]=Mathematical&problemStatus=unsolved&difficulty[]=-1&page=1&query=category[]MathematicalproblemStatusunsolveddifficulty[]-1page1category[]Mathematical)
```cpp
// { Driver Code Starts

#include<bits/stdc++.h>
using namespace std;

 // } Driver Code Ends

class Solution{
	public:
   	int maximum_Cuts(int n){
   	    // Code here
   	    return (n * (n + 1)) / 2 + 1;
   	}    
};

// { Driver Code Starts.
int main(){
	int tc;
	cin >> tc;
	while(tc--){
		int n;
		cin >> n;
		Solution ob;
		int ans = ob.maximum_Cuts(n);
		cout << ans <<"\n";
	}  
	return 0;
}  // } Driver Code Ends
```

[Maximum money](https://practice.geeksforgeeks.org/problems/maximum-money2855/1/?category[]=Mathematical&category[]=Mathematical&problemStatus=unsolved&difficulty[]=-1&page=1&query=category[]MathematicalproblemStatusunsolveddifficulty[]-1page1category[]Mathematical#)
```cpp
// { Driver Code Starts
#include <bits/stdc++.h>
using namespace std;

 // } Driver Code Ends
class Solution {
  public:
    int maximizeMoney(int N , int K) {
        // code here 
        int sum = 0;
        for(int i = 0; i < N; i = i + 2){
            sum += K;
        }
        return sum;
    }
};

// { Driver Code Starts.
int main() {
    int t;
    cin >> t;
    while (t--) {
        int N,K;

        cin>>N>>K;

        Solution ob;
        cout << ob.maximizeMoney(N,K) << endl;
    }
    return 0;
}  // } Driver Code Ends
```

[]()
```cpp

```
