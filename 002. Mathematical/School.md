1. [The dice problem](https://practice.geeksforgeeks.org/problems/the-dice-problem2316/1/?category[]=Mathematical&category[]=Mathematical&difficulty[]=-2&page=1&query=category[]Mathematicaldifficulty[]-2page1category[]Mathematical)
```cpp
// { Driver Code Starts
#include<bits/stdc++.h> 
using namespace std; 

 // } Driver Code Ends
//User function Template for C++
class Solution
{
public:
    int oppositeFaceOfDice(int N)
    {
        // Write Your Code here
        switch(N){
            case 1: return 6;
            break;
            
            case 2: return 5;
            break;
            
            case 3: return 4;
            break;
            
            case 4: return 3;
            break;
            
            case 5: return 2;
            break;
            
            case 6: return 1;
            break;
            
        }
    }
};

// { Driver Code Starts.
int main()
{
    int t;
    cin >> t;
    while (t--)
    {
        int N;
        cin>>N;
        Solution ob;
        int ans  = ob.oppositeFaceOfDice(N);
        cout<<ans<<endl;
    }
    return 0;
}  // } Driver Code Ends
```

2. [Addition of Two Numbers ](https://practice.geeksforgeeks.org/problems/addition-of-two-numbers0812/1/?category[]=Mathematical&category[]=Mathematical&difficulty[]=-2&page=1&query=category[]Mathematicaldifficulty[]-2page1category[]Mathematical)
```cpp

 // } Driver Code Ends
class Solution{   
public:
    int addition(int A, int B){
        // code here 
        return A + B;
    }
};

// { Driver Code Starts.
int main() 
{ 
    int t;
    cin>>t;
    while(t--)
    {
        int A, B;
        cin >> A >> B;
        Solution ob;
        cout << ob.addition(A,B) << endl;
    }
    return 0; 
} 
  // } Driver Code Ends
```

3. [Swap two numbers ](https://practice.geeksforgeeks.org/problems/swap-two-numbers3844/1/?category[]=Mathematical&category[]=Mathematical&problemStatus=unsolved&difficulty[]=-2&page=1&query=category[]MathematicalproblemStatusunsolveddifficulty[]-2page1category[]Mathematical)
```cpp
// { Driver Code Starts
//Initial template for c++

#include<bits/stdc++.h> 
using namespace std; 

 // } Driver Code Ends
//User function Template for C++

class Solution{   
public:
    pair<int, int> get(int a, int b){
        //complete the function here
        pair<int,int> p(b,a);
        return p;
    }
};

// { Driver Code Starts.

int main() 
{ 
    int t;
    cin>>t;
    while(t--)
    {
        int a, b;
        cin >> a >> b;
        
        Solution ob;
        pair<int, int>p = ob.get(a, b);
        cout << p.first << ' ' << p.second << endl;
    
    }
    return 0; 
} 
  // } Driver Code Ends
```

4. [Mean](https://practice.geeksforgeeks.org/problems/mean0021/1/?category[]=Mathematical&category[]=Mathematical&problemStatus=unsolved&difficulty[]=-2&page=1&query=category[]MathematicalproblemStatusunsolveddifficulty[]-2page1category[]Mathematical)
```cpp
// { Driver Code Starts
#include <bits/stdc++.h>
using namespace std;

 // } Driver Code Ends
class Solution {
  public:
    int mean(int N , int A[]) {
        // code here
        int sum = 0, mean;
        for(int i = 0; i < N; i++){
            sum += A[i];
        }
        return (sum / N);
    }
};

// { Driver Code Starts.
int main() {
    int t;
    cin >> t;
    while (t--) {
        int N;
        cin>>N;
        int A[N];
        for(int i=0 ; i<N ; i++)
            cin>>A[i];

        Solution ob;
        cout << ob.mean(N,A) << endl;
    }
    return 0;
}  // } Driver Code Ends
```

5. [Multiplication Table](https://practice.geeksforgeeks.org/problems/print-table0303/1/?category[]=Mathematical&category[]=Mathematical&problemStatus=unsolved&difficulty[]=-2&page=1&query=category[]MathematicalproblemStatusunsolveddifficulty[]-2page1category[]Mathematical#)
```cpp
// { Driver Code Starts
#include<bits/stdc++.h> 
using namespace std; 

 // } Driver Code Ends
//User function Template for C++
class Solution
{
public:
    vector<int> getTable(int N)
    {
        // Write Your Code here
        vector<int> v(10);
        for(int i = 1; i <= 10; i++){
            v[i - 1] = N * i;
        }
        return v;
    }
};

// { Driver Code Starts.
int main()
{
    int t;
    cin >> t;
    while (t--)
    {
        int N;
        cin>>N;
        Solution ob;
        vector<int> ans = ob.getTable(N);
        for(int i=0; i<ans.size(); i++)
        cout<<ans[i]<<" ";
        cout<<"\n";
    }
    return 0;
}  // } Driver Code Ends
```

6. [Odd or Even](https://practice.geeksforgeeks.org/problems/odd-or-even3618/1/?category[]=Mathematical&category[]=Mathematical&problemStatus=unsolved&difficulty[]=-2&page=1&query=category[]MathematicalproblemStatusunsolveddifficulty[]-2page1category[]Mathematical)
```cpp
// { Driver Code Starts
#include<bits/stdc++.h> 
using namespace std; 

 // } Driver Code Ends
class Solution{   
public:
    string oddEven(int N){
        // code here
        return N % 2 == 0 ? "even" : "odd";
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
        cin >> N;
        Solution ob;
        cout << ob.oddEven(N) << endl;
    }
    return 0; 
}   // } Driver Code Ends
```

7. [Find n-th term of series 1, 3, 6, 10, 15, 21](https://practice.geeksforgeeks.org/problems/find-n-th-term-of-series-1-3-6-10-15-215506/1/?category[]=Mathematical&category[]=Mathematical&problemStatus=unsolved&difficulty[]=-2&page=1&query=category[]MathematicalproblemStatusunsolveddifficulty[]-2page1category[]Mathematical)
```cpp
// { Driver Code Starts
#include <bits/stdc++.h>
using namespace std;

 // } Driver Code Ends
class Solution {
  public:
    int findNthTerm(int N) {
        // code here
        return (N * (N + 1)) / 2;
    }
};

// { Driver Code Starts.
int main() {
    int t;
    cin >> t;
    while (t--) {
        int N;
        
        cin>>N;

        Solution ob;
        cout << ob.findNthTerm(N) << endl;
    }
    return 0;
}  // } Driver Code Ends
```

8. [Series AP](https://practice.geeksforgeeks.org/problems/series-ap5310/1/?category[]=Mathematical&category[]=Mathematical&problemStatus=unsolved&difficulty[]=-2&page=1&query=category[]MathematicalproblemStatusunsolveddifficulty[]-2page1category[]Mathematical)
```cpp
// { Driver Code Starts
// Initial Template for C++

#include <bits/stdc++.h>
using namespace std;

 // } Driver Code Ends
// User function template for C++

class Solution {
  public:
    int nthTermOfAP(int A1, int A2, int N) {
        // code here
        return A1 + (N - 1) * (A2 - A1); // first term + (no. of terms - 1) * common difference
    }
};

// { Driver Code Starts.
int main() {
    int t;
    cin >> t;
    while (t--) {
        int A1, A2, N;
        cin >> A1 >> A2 >> N;
        Solution ob;
        cout << ob.nthTermOfAP(A1, A2, N) << "\n";
    }
}
  // } Driver Code Ends
```

9. [Floyd's triangle](https://practice.geeksforgeeks.org/problems/floyds-triangle1222/1/?category[]=Mathematical&category[]=Mathematical&problemStatus=unsolved&difficulty[]=-2&page=1&query=category[]MathematicalproblemStatusunsolveddifficulty[]-2page1category[]Mathematical)
```cpp
// { Driver Code Starts
#include<bits/stdc++.h> 
using namespace std; 

 // } Driver Code Ends
class Solution
{
public:
    void printFloydTriangle(int N)
    {
        // Write Your Code here
        int count = 1;
        
        for(int i = 1; i <= N; i++){
            for(int j = 1; j <= i; j ++){
                cout << count++ << " ";
            }
            cout << endl;
        }
    }
};

// { Driver Code Starts.
int main()
{
    int t;
    cin >> t;
    while (t--)
    {
        int N;
        cin >> N;
        Solution ob;
        ob.printFloydTriangle(N);
    }
    return 0;
}  // } Driver Code Ends
```

10. [Armstrong Numbers](https://practice.geeksforgeeks.org/problems/armstrong-numbers2727/1/?category[]=Mathematical&category[]=Mathematical&problemStatus=unsolved&difficulty[]=-2&page=1&query=category[]MathematicalproblemStatusunsolveddifficulty[]-2page1category[]Mathematical)
```cpp
// { Driver Code Starts
// Initial Template for C++
#include <bits/stdc++.h>
using namespace std;

 // } Driver Code Ends
// User function Template for C++
class Solution {
  public:
    string armstrongNumber(int n){
        // code here
        int sumCubeDigit = 0;
        int originalNum = n;
        while(n != 0){
            int digit = n % 10;
            sumCubeDigit += digit * digit * digit;
            n /= 10;
        }
        return sumCubeDigit == originalNum ? "Yes" : "No";
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
        cout << ob.armstrongNumber(n) << endl;
    }
    return 0;
}
  // } Driver Code Ends
```

11. [Area of Rectange, Right Angled Triangle and Circle](https://practice.geeksforgeeks.org/problems/area-of-rectange-right-angled-triangle-and-circle2600/1/?category[]=Mathematical&category[]=Mathematical&problemStatus=unsolved&difficulty[]=-2&page=1&query=category[]MathematicalproblemStatusunsolveddifficulty[]-2page1category[]Mathematical)
```cpp
// { Driver Code Starts
#include <bits/stdc++.h>
using namespace std;

 // } Driver Code Ends
class Solution {
  public:
    vector<int> getAreas(int L , int W , int B , int H , int R) {
        // code here
        vector<int> area;
        
        area.push_back(L * W); // rectangle area
        area.push_back(0.5 * B * H); // rt. angled triangle area
        area.push_back(3.14 * R * R); // circle area
        
        return area;
    }
};

// { Driver Code Starts.
int main() {
    int t;
    cin >> t;
    while (t--) {
        int L,W,B,H,R;
        
        cin>>L>>W>>B>>H>>R;
        
        Solution ob;
        vector<int> ans = ob.getAreas(L,W,B,H,R);
        cout<<ans[0]<<" "<<ans[1]<<" "<<ans[2]<<endl;
    }
    return 0;
}  // } Driver Code Ends
```

12. [Small Factorial](https://practice.geeksforgeeks.org/problems/small-factorial0854/1/?category[]=Mathematical&category[]=Mathematical&problemStatus=unsolved&difficulty[]=-2&page=1&query=category[]MathematicalproblemStatusunsolveddifficulty[]-2page1category[]Mathematical)
```cpp
// { Driver Code Starts


#include<bits/stdc++.h>
using namespace std;

 // } Driver Code Ends

class Solution
{
	public:
		long long int find_fact(int n)
		{
		    // Code here.
		    if(n == 0 || n == 1) return 1;
		    else return n * find_fact(n - 1);
		}
};

// { Driver Code Starts.
int main(){
    int T;
    cin >> T;
    while(T--)
    {
    	int n; 
    	cin >> n;
    	Solution ob;
    	long long int ans = ob.find_fact(n);
    	cout << ans <<"\n";
    }
	return 0;
}  // } Driver Code Ends
```

13. [Reverse digits](https://practice.geeksforgeeks.org/problems/reverse-digit0316/1/?category[]=Mathematical&category[]=Mathematical&problemStatus=unsolved&difficulty[]=-2&page=1&query=category[]MathematicalproblemStatusunsolveddifficulty[]-2page1category[]Mathematical)
*For palindrome add two lines to code below :
long temp=n;
return temp==rev ? "Yes" : "No" ;*

```cpp
// { Driver Code Starts

#include<bits/stdc++.h>
using namespace std;

 // } Driver Code Ends
class Solution
{
	public:
		long long int reverse_digit(long long int n)
		{
		    // Code here
		    long long int rev = 0;
                    while(n != 0){
                       long long int r = n % 10;
                       rev = rev * 10 + r;
                        n = n / 10;
                
                    }
                 return rev;
		}
};

// { Driver Code Starts.
int main(){
    int T;
    cin >> T;
    while(T--)
    {
    	long long int n;
    	cin >> n;
    	Solution ob;
    	long long int  ans = ob.reverse_digit(n);
    	cout << ans <<"\n";
    }
	return 0;
}  // } Driver Code Ends
```
14. [Sum of an AP](https://practice.geeksforgeeks.org/problems/sum-of-an-ap1025/1/?category[]=Mathematical&category[]=Mathematical&problemStatus=unsolved&difficulty[]=-2&page=1&query=category[]MathematicalproblemStatusunsolveddifficulty[]-2page1category[]Mathematical)
```cpp
// { Driver Code Starts


#include<bits/stdc++.h>
using namespace std;

 // } Driver Code Ends

class Solution
{
	public:
		int sum_of_ap(int n,int a, int d)
		{
		    // Code here.
		    return n * (2 * a + (n - 1) * d) / 2; 
		}
};

// { Driver Code Starts.
int main(){
    int T;
    cin >> T;
    while(T--)
    {
    	int n, a, d;
    	cin >> n >> a >> d;
    	Solution ob;
    	int ans = ob.sum_of_ap(n, a, d);
    	cout << ans << "\n";
    }
	return 0;
}  // } Driver Code Ends
```

15. [Sum of Digit is Pallindrome or not](https://practice.geeksforgeeks.org/problems/sum-of-digit-is-pallindrome-or-not2751/1/?category[]=Mathematical&category[]=Mathematical&problemStatus=unsolved&difficulty[]=-2&page=1&query=category[]MathematicalproblemStatusunsolveddifficulty[]-2page1category[]Mathematical)
```cpp
// { Driver Code Starts
// Initial Template for C++

#include <bits/stdc++.h>
using namespace std;

 // } Driver Code Ends
// User function Template for C++

class Solution {
  public:
    int isDigitSumPalindrome(int N) {
        // code here
        
        int sum = 0;
        while(N > 0){ // to calculate sum of digits
            int r = N % 10;
            sum += r;
            N = N / 10;
        }
        
        int x = sum;
        int rev = 0;
        while(x > 0){ // to reverse the sum of digits
            int rem = x % 10;
            rev = rev * 10 + rem;
            x = x / 10;
        }
        
        if(sum == rev) return 1;
        else return 0;
    }
};

// { Driver Code Starts.
int main() {
    int t;
    cin >> t;
    while (t--) {
        int N;
        cin >> N;
        Solution ob;
        cout << ob.isDigitSumPalindrome(N) << "\n";
    }
}
  // } Driver Code Ends
```

16. [Replace all 0's with 5](https://practice.geeksforgeeks.org/problems/replace-all-0-with-5-in-an-input-integer/1/?category[]=Mathematical&category[]=Mathematical&problemStatus=unsolved&difficulty[]=-2&page=1&query=category[]MathematicalproblemStatusunsolveddifficulty[]-2page1category[]Mathematical)
```cpp
// { Driver Code Starts
#include<bits/stdc++.h>
using namespace std;
 
// Driver program to test above function

 // } Driver Code Ends

class Solution{
  public:
    /*you are required to complete this method*/
    int convertFive(int n)
    {
    //Your code here
    
    // convert int n to string str
    string str = to_string(n);
    
    // replace all 0's with 5's
    for(int i = 0; i < str.length(); i++){
        if(str[i] == '0'){
            str[i] = '5';
        }
    }
    
    // covert string to int
    int ans = stoi(str);
    
     return ans;
    }
};

// { Driver Code Starts.
int main()
{
    int T;
    cin>>T;
    while(T--)
    {
    	int n;
    	cin>>n;
    	Solution obj;
    	cout<<obj.convertFive(n)<<endl;
    }
}  // } Driver Code Ends
```

17. [Power of Pow | Even Number](https://practice.geeksforgeeks.org/problems/power-of-pow-even-number5440/1/?category[]=Mathematical&category[]=Mathematical&problemStatus=unsolved&difficulty[]=-2&page=1&query=category[]MathematicalproblemStatusunsolveddifficulty[]-2page1category[]Mathematical#)
```cpp
// { Driver Code Starts

#include<bits/stdc++.h>
using namespace std;

 // } Driver Code Ends
class Solution
{
	public:
		long long int sum_of_square_evenNumbers(long long int n)
		{
		    // Code here
		    return (2 * n * (n + 1) * ((2 * n) + 1)) /3; 
		}
};

// { Driver Code Starts.
int main(){
    int T;
    cin >> T;
    while(T--)
    {
    	long long int n;
    	cin >> n;
    	Solution ob;
    	long long int  ans = ob.sum_of_square_evenNumbers(n);
    	cout << ans <<"\n";
    }
	return 0;
}  // } Driver Code Ends
```

18. [Sum Palindrome](https://practice.geeksforgeeks.org/problems/sum-palindrome3857/1/?category[]=Mathematical&category[]=Mathematical&problemStatus=unsolved&difficulty[]=-2&page=2&query=category[]MathematicalproblemStatusunsolveddifficulty[]-2page2category[]Mathematical#)
```cpp

```

19. [Number of divisors](https://practice.geeksforgeeks.org/problems/number-of-divisors1631/1/?category[]=Mathematical&category[]=Mathematical&problemStatus=unsolved&difficulty[]=-2&page=2&query=category[]MathematicalproblemStatusunsolveddifficulty[]-2page2category[]Mathematical#)
```cpp
// { Driver Code Starts
//Initial Template for C++


#include<bits/stdc++.h>
using namespace std;

 // } Driver Code Ends
//User function Template for C++

class Solution
{
	public:
		int count_divisors(int n)
		{
		    //Code here.
		    int count = 0, divisors;
		    for(divisors = 1; divisors <= sqrt(n); divisors++){
		        if( n % divisors == 0){
		            if(divisors % 3 == 0) count++;
		            if((n / divisors) % 3 == 0) count++;
		        }
		    }
		    divisors--;
		    
		    if((divisors * divisors == n) && (divisors % 3 == 0)){
		        count--;
		    }
		    return count;
		}
};

// { Driver Code Starts.
int main(){
    int T;
    cin >> T;
    while(T--)
    {
    	int n;
    	cin >> n;
    	Solution ob;
    	int ans = ob.count_divisors(n);
    	cout << ans << "\n";
    }
	return 0;
}  // } Driver Code Ends
```

20. [Power of Pow | Odd Numbers](https://practice.geeksforgeeks.org/problems/power-of-pow-odd-numbers1103/1/?category[]=Mathematical&category[]=Mathematical&problemStatus=unsolved&difficulty[]=-2&page=1&query=category[]MathematicalproblemStatusunsolveddifficulty[]-2page1category[]Mathematical)
```cpp
// { Driver Code Starts



#include<bits/stdc++.h>
using namespace std;

 // } Driver Code Ends


class Solution
{
	public:
		long long int sum_of_square_oddNumbers(long long int n)
		{
		    // Code here.
		    return (4 * n * n * n - n) / 3;
		}
};

// { Driver Code Starts.
int main(){
    int T;
    cin >> T;
    while(T--)
    {
    	long long int n;
    	cin >> n;
    	Solution ob;
    	long long int  ans = ob.sum_of_square_oddNumbers(n);
    	cout << ans <<"\n";
    }
	return 0;
}  // } Driver Code Ends
```

21. [GCD of two numbers](https://practice.geeksforgeeks.org/problems/gcd-of-two-numbers3459/1/?category[]=Mathematical&category[]=Mathematical&problemStatus=unsolved&difficulty[]=-2&page=1&query=category[]MathematicalproblemStatusunsolveddifficulty[]-2page1category[]Mathematical)
```cpp
// { Driver Code Starts
#include <bits/stdc++.h>
using namespace std;

 // } Driver Code Ends
//User function Template for C++
class Solution
{
	public:
    int gcd(int A, int B) 
	{ 
	    // code here
	    if(A == 0) return B;
	    else return gcd(B % A,A);
	      
	} 
};

// { Driver Code Starts.

int main() 
{
   	int t;
    cin >> t;
    while (t--)
    {
        int A, B;
        cin >> A >> B;
        Solution ob;
       	cout <<  ob.gcd(A, B) << "\n";
    }
    return 0;
}  // } Driver Code Ends
```

22. [Distance between 2 points](https://practice.geeksforgeeks.org/problems/distance-between-2-points3200/1/?category[]=Mathematical&category[]=Mathematical&problemStatus=unsolved&difficulty[]=-2&page=1&query=category[]MathematicalproblemStatusunsolveddifficulty[]-2page1category[]Mathematical#)
```cpp
// { Driver Code Starts

#include<bits/stdc++.h>
using namespace std;

 // } Driver Code Ends
class Solution
{
	public:
		int distance(int x1, int y1, int x2, int y2)
		{
		    // Code herereturn 
		    return round(sqrt(pow((x2 - x1),2) + pow((y2 - y1),2)));
		}
};

// { Driver Code Starts.
int main(){
    int T;
    cin >> T;
    while(T--)
    {
    	int x1, y1, x2, y2;
    	cin >> x1 >> y1 >> x2 >> y2;
    	Solution ob;
    	int  ans = ob.distance(x1, y1, x2, y2);
    	cout << ans <<"\n";
    }
	return 0;
}  // } Driver Code Ends
```

23. [Cube root of a number](https://practice.geeksforgeeks.org/problems/cube-root-of-a-number0915/1/?category[]=Mathematical&category[]=Mathematical&problemStatus=unsolved&difficulty[]=-2&page=1&query=category[]MathematicalproblemStatusunsolveddifficulty[]-2page1category[]Mathematical#)
```cpp
// { Driver Code Starts
#include <bits/stdc++.h>
using namespace std;

 // } Driver Code Ends
class Solution {
  public:
    int cubeRoot(int N) {
        // code here
        return cbrt(N);
    }
};

// { Driver Code Starts.
int main() {
    int t;
    cin >> t;
    while (t--) {
        int N;

        cin>>N;

        Solution ob;
        cout << ob.cubeRoot(N) << endl;
    }
    return 0;
}  // } Driver Code Ends
```

24. [C++ Operators | Set 1 (Arithmetic)](https://practice.geeksforgeeks.org/problems/c-operators4602/1/?category[]=Mathematical&category[]=Mathematical&problemStatus=unsolved&difficulty[]=-2&page=1&query=category[]MathematicalproblemStatusunsolveddifficulty[]-2page1category[]Mathematical#)
```cpp
// { Driver Code Starts
#include <bits/stdc++.h>
using namespace std;

 // } Driver Code Ends
class Solution {
  public:
    vector<int> cppOperators(int A, int B) {
        // code here
        if(A < B){
            return {B+A,B*A,B-A,B/A};
        }
        return {A+B,A*B,A-B,A/B};
    }
};

// { Driver Code Starts.
int main() {
    int t;
    cin >> t;
    while (t--) {
        int A, B;
        cin >> A >> B;
        Solution ob;
        vector<int> ans = ob.cppOperators(A, B);
        for (int u : ans) cout << u << "\n";
    }
}  // } Driver Code Ends
```

25. [Sum of AP series](https://practice.geeksforgeeks.org/problems/sum-of-ap-series4512/1/?category[]=Mathematical&category[]=Mathematical&problemStatus=unsolved&difficulty[]=-2&page=1&query=category[]MathematicalproblemStatusunsolveddifficulty[]-2page1category[]Mathematical)
```cpp
// { Driver Code Starts


#include<bits/stdc++.h>
using namespace std;

 // } Driver Code Ends

class Solution
{
	public:
		long sum_of_ap(long n,long a, long d)
		{
		    // Code here.
		    return n * (2 * a + (n - 1) * d) / 2;
		}
};

// { Driver Code Starts.
int main(){
    int T;
    cin >> T;
    while(T--)
    {
    	long n, a, d;
    	cin >> n >> a >> d;
    	Solution ob;
    	long ans = ob.sum_of_ap(n, a, d);
    	cout << ans <<"\n";
    }
	return 0;
}  // } Driver Code Ends
```

26. [Sum of odd and even elements](https://practice.geeksforgeeks.org/problems/sum-of-odd-and-even-elements3033/1/?category[]=Mathematical&category[]=Mathematical&problemStatus=unsolved&difficulty[]=-2&page=1&query=category[]MathematicalproblemStatusunsolveddifficulty[]-2page1category[]Mathematical#)
```cpp
// { Driver Code Starts


#include<bits/stdc++.h>
using namespace std;

 // } Driver Code Ends

class Solution
{
	public:
		vector<int> find_sum(int n)
		{
		    // Code here
		    
		    int sum = (n * (n + 1)) / 2;
		    n = n / 2;
		    int sumEven = n * (n + 1);
		    int sumOdd = sum - sumEven;
		    
		    return {sumOdd,sumEven}; // returned as array of two elements
		    
		    

		}
};

// { Driver Code Starts.
int main(){
    int T;
    cin >> T;
    while(T--)
    {
    	int n;
    	cin >> n;
    	Solution ob;
    	vector<int> ans = ob.find_sum(n);
    	for(auto i: ans)
    		cout << i << " ";
    	cout<<"\n";
    }
	return 0;
}  // } Driver Code Ends
```

27. [Surface Area and Volume of Cuboid](https://practice.geeksforgeeks.org/problems/surface-area-and-volume-of-cuboid0522/1/?category[]=Mathematical&category[]=Mathematical&problemStatus=unsolved&difficulty[]=-2&page=1&query=category[]MathematicalproblemStatusunsolveddifficulty[]-2page1category[]Mathematical)
```cpp
// { Driver Code Starts


#include<bits/stdc++.h>
using namespace std;

 // } Driver Code Ends


class Solution{
	public:
	vector<long long int> find(int l, int b, int h)
	{
	    // Code here
	    long long int L = l, B = b, H = h;
		long long int area = 2*(L*H + B*H + L*B);
		long long int volume = (L*B*H);
		vector<long long int >res;
		res.push_back(area);
		res.push_back(volume);
		return res;
	}  
};

// { Driver Code Starts.
int main(){
	int tc;
	cin >> tc;
	while(tc--){
		int l, b, h;
		cin >> l >> b >> h;
		Solution ob;
		vector<long long int> ans = ob.find(l, b, h);
		for(auto i: ans)cout << i <<" ";
		cout << "\n";
	}  
	return 0;
}  // } Driver Code Ends
```

28. [Greatest of three numbers](https://practice.geeksforgeeks.org/problems/greatest-of-three-numbers2520/1/?category[]=Mathematical&category[]=Mathematical&problemStatus=unsolved&difficulty[]=-2&page=1&query=category[]MathematicalproblemStatusunsolveddifficulty[]-2page1category[]Mathematical)
```cpp
// { Driver Code Starts
// Initial Template for C++

#include <bits/stdc++.h>
using namespace std;

 // } Driver Code Ends
// User function Template for C++

class Solution {
  public:
    int greatestOfThree(int A, int B, int C) {
        // code here
        if(A>=B && A>=C) return A;
        else if(B>=A && B>=C) return B;
        else return C;

    }
};

// { Driver Code Starts.
int main() {
    int t;
    cin >> t;
    while (t--) {
        int A, B, C;
        cin >> A >> B >> C;
        Solution ob;
        cout << ob.greatestOfThree(A, B, C) << "\n";
    }
}
  // } Driver Code Ends
```

29. []()
```cpp

```
