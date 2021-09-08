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

[Anshuman's Favourite Number](https://practice.geeksforgeeks.org/problems/anshumans-favourite-number2029/1/?category[]=Mathematical&category[]=Mathematical&problemStatus=unsolved&difficulty[]=-1&page=1&query=category[]MathematicalproblemStatusunsolveddifficulty[]-1page1category[]Mathematical)
```cpp
// { Driver Code Starts
//Initial Template for C++
#include<bits/stdc++.h> 
using namespace std; 

 // } Driver Code Ends
//User function Template for C++
class Solution{   
public:
    string isValid(long long N){
        // code here 
        if(N % 5 == 0) return "YES";
        else return "NO";
    }
};

// { Driver Code Starts.
int main() 
{ 
    int t;
    cin>>t;
    while(t--)
    {
        long long N;
        cin >> N;
        Solution ob;
        cout << ob.isValid(N) << endl;
    }
    return 0; 
}   // } Driver Code Ends
```

[Half N by M](https://practice.geeksforgeeks.org/problems/geek-and-coffee-shop5721/1/?category[]=Mathematical&category[]=Mathematical&problemStatus=unsolved&difficulty[]=-1&page=1&query=category[]MathematicalproblemStatusunsolveddifficulty[]-1page1category[]Mathematical)
```cpp
// { Driver Code Starts
// Initial Template for C++

#include <bits/stdc++.h>
using namespace std;

 // } Driver Code Ends
// User function Template for C++

class Solution{
public:
    int mthHalf(int N, int M){
        // code here
        return N / pow(2,M - 1);
    }
};

// { Driver Code Starts.

int main(){
    int t;
    cin>>t;
    while(t--){
        int N, M;
        cin>>N>>M;
        
        Solution ob;
        cout<<ob.mthHalf(N, M)<<"\n";
    }
    return 0;
}  // } Driver Code Ends
```

[Check perfect square](https://practice.geeksforgeeks.org/problems/check-perfect-square2503/1/?category[]=Mathematical&category[]=Mathematical&problemStatus=unsolved&difficulty[]=-1&page=1&query=category[]MathematicalproblemStatusunsolveddifficulty[]-1page1category[]Mathematical#)
```cpp
 { Driver Code Starts
// Initial Template for C++
#include <bits/stdc++.h>
using namespace std;

 // } Driver Code Ends
// User function Template for C++
class Solution {
  public:
    long long int isPerfectSquare(long long int n){
        // code here
        return ((int)sqrt(n) * (int)sqrt(n) == n) ? 1 : 0;
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
        cout << ob.isPerfectSquare(n) << endl;
    }
    return 0;
}
  // } Driver Code Ends
```

[Change all even bits in a number to 0](https://practice.geeksforgeeks.org/problems/change-all-even-bits-in-a-number-to-03253/1/?category[]=Mathematical&category[]=Mathematical&problemStatus=unsolved&difficulty[]=-1&page=1&query=category[]MathematicalproblemStatusunsolveddifficulty[]-1page1category[]Mathematical)
```cpp
// { Driver Code Starts
// Initial Template for C++
#include <bits/stdc++.h>
using namespace std;

 // } Driver Code Ends
// User function Template for C++
class Solution {
  public:
    long long int convertEvenBitToZero(long long int n) {
        // code here
        
        /*
        n=10;
....10=> 00000000001010
....0xAAAAAAAA=> 01010101011010
n & 0xAAAAAAAA=> 00000000001010(Even bits changed (Indexing start with 0))
        */
         return (n & 0xAAAAAAAA);
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
        cout << ob.convertEvenBitToZero(n) << endl;
    }
    return 0;
}
  // } Driver Code Ends
```

[Check perfect square](https://practice.geeksforgeeks.org/problems/check-perfect-square5253/1/?category[]=Mathematical&category[]=Mathematical&problemStatus=unsolved&difficulty[]=-1&page=1&query=category[]MathematicalproblemStatusunsolveddifficulty[]-1page1category[]Mathematical#)
```cpp
Driver Code Ends
class Solution{   
public:
    int checkPerfectSquare(int N){
        // code here 
        return ceil(sqrt(N)) == floor(sqrt(N));
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
        cout << ob.checkPerfectSquare(N) << endl;
    }
    return 0; 
}   // } Driver Code Ends
```

[Parity of unsigned integer](https://practice.geeksforgeeks.org/problems/parity-of-unsigned-integer4247/1/?category[]=Mathematical&category[]=Mathematical&problemStatus=unsolved&difficulty[]=-1&page=1&query=category[]MathematicalproblemStatusunsolveddifficulty[]-1page1category[]Mathematical)
```cpp
/ } Driver Code Ends
class Solution {
  public:
    string computeParity(int N) {
        // code here
        int count1 = 0;
        
        while(N > 0)
        {
            if(N%2 == 1)
            {
                count1++;
            }
            
            N /= 2;
        }
        
        return count1%2 == 0 ? "even" : "odd";
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
        cout << ob.computeParity(N) << endl;
    }
    return 0;
}  // } Driver Code Ends
```

[Common Divisors](https://practice.geeksforgeeks.org/problems/common-divisors4712/1/?category[]=Mathematical&category[]=Mathematical&problemStatus=unsolved&difficulty[]=-1&page=1&query=category[]MathematicalproblemStatusunsolveddifficulty[]-1page1category[]Mathematical)
```cpp
// { Driver Code Starts
// Initial Template for C++
#include <bits/stdc++.h>
using namespace std;

 // } Driver Code Ends
// User function Template for C++
class Solution {
  public:
    long long int commDiv(long long int a,long long int b) {
        // code here
        int count = 0;
        for(int i = 1; i <= min(a,b); i++){
            if(a % i == 0 && b % i == 0){
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
        long long int a, b;
        cin >> a >> b;
        Solution ob;
        cout<<ob.commDiv(a, b)<<endl;
    }
    return 0;
}
  // } Driver Code Ends
```

[Strong Numbers](https://practice.geeksforgeeks.org/problems/strong-numbers3315/1/?category[]=Mathematical&category[]=Mathematical&problemStatus=unsolved&difficulty[]=-1&page=1&query=category[]MathematicalproblemStatusunsolveddifficulty[]-1page1category[]Mathematical)
```cpp
Driver Code Ends
class Solution {
  public:
    int isStrong(int N) {
        // code here
        int factorial[10];
        factorial[0] = factorial[1] = 1;
        
        for(int i = 2; i <= 9; i++){ // calculate factorial
            factorial[i] = factorial[i - 1] * i;
        }
        
        int num = N; // temporarily num stores original number
        int sum = 0;
        
        while(num > 0){ // calculate sum of factorial of digits
            sum += factorial[num % 10];
            num = num / 10;
        }
        
        return sum == N ? 1 : 0;
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
        cout << ob.isStrong(N) << endl;
    }
    return 0;
}  // } Driver Code Ends
```

[Krishnamurthy number](https://practice.geeksforgeeks.org/problems/krishnamurthy-number1323/1/?category[]=Mathematical&category[]=Mathematical&problemStatus=unsolved&difficulty[]=-1&page=1&query=category[]MathematicalproblemStatusunsolveddifficulty[]-1page1category[]Mathematical)
```cpp
// { Driver Code Starts
#include <bits/stdc++.h>
using namespace std;

 // } Driver Code Ends
class Solution {
  public:
    string isKrishnamurthy(int N) {
        // code here
        int factorial[10];
        factorial[0] = factorial[1] = 1;
        
        for(int i = 2; i <= 9; i++){ // calculate factorial
            factorial[i] = factorial[i - 1] * i;
        }
        
        int num = N; // temporarily num stores original number
        int sum = 0;
        
        while(num > 0){ // calculate sum of factorial of digits
            sum += factorial[num % 10];
            num = num / 10;
        }
        
        return sum == N ? "YES" : "NO";
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
        cout << ob.isKrishnamurthy(N) << endl;
    }
    return 0;
}  // } Driver Code Ends
```

[Disarium Number](https://practice.geeksforgeeks.org/problems/disarium-number1045/1/?category[]=Mathematical&category[]=Mathematical&problemStatus=unsolved&difficulty[]=-1&page=1&query=category[]MathematicalproblemStatusunsolveddifficulty[]-1page1category[]Mathematical)
```cpp
// { Driver Code Starts
#include <bits/stdc++.h>
using namespace std;

 // } Driver Code Ends
class Solution {
  public:
    int isDisarium(int N) {
        // code here
        int position = log10(N) + 1;
        
        int num = N;
        int sum = 0;
        while(num > 0)
        {
            sum += pow((num%10), position);
            position--;
            num /= 10;
        }
        
        return sum == N ? 1 : 0;
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
        cout << ob.isDisarium(N) << endl;
    }
    return 0;
}  // } Driver Code Ends
```

[Strong Numbers](https://practice.geeksforgeeks.org/problems/strong-numbers4336/1/?category[]=Mathematical&category[]=Mathematical&problemStatus=unsolved&difficulty[]=-1&page=1&query=category[]MathematicalproblemStatusunsolveddifficulty[]-1page1category[]Mathematical#)
```cpp
Driver Code Ends
class Solution
{
public:
	public:
		int is_StrongNumber(int n)
		{
		    // Code here.
		int factorial[10];
        factorial[0] = factorial[1] = 1;
        
        for(int i = 2; i <= 9; i++){ // calculate factorial
            factorial[i] = factorial[i - 1] * i;
        }
        
        int num = n; // temporarily num stores original number
        int sum = 0;
        
        while(num > 0){ // calculate sum of factorial of digits
            sum += factorial[num % 10];
            num = num / 10;
        }
        
        return sum == n ? 1 : 0;
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
    	int ans = ob.is_StrongNumber(n);
    	cout << ans <<"\n";
    }
	return 0;
}
  // } Driver Code Ends
```

[Base Conversion](https://practice.geeksforgeeks.org/problems/base-conversion0924/1/?category[]=Mathematical&category[]=Mathematical&problemStatus=unsolved&difficulty[]=-1&page=9&query=category[]MathematicalproblemStatusunsolveddifficulty[]-1page9category[]Mathematical)
```cpp
/ } Driver Code Ends
class Solution{
public:
    
    string Decimal_To_Binary(int a){
        string ans="";
        while(a)
        {
            ans.push_back('0'+(a%2));
            a/=2;
        }
        reverse(ans.begin(),ans.end());
        return ans;
    }
    
   string Binary_To_Decimal(int b){
        
         int nums=0;
         int cnt=0;
        while(b)
        {
           nums+=(b%10)*pow(2,cnt);
           b/=10;
           cnt++;
        }
        return to_string(nums);
       
       
    }
    
    string Decimal_To_Hexadecimal(int c)
    {
        string ans;
        while(c)
        {
            int rem=c%16;
            if(rem<10)
            {
                ans.push_back('0'+rem);
            }
            else
              ans.push_back('A'+(rem-10));
              c/=16;
        }
        reverse(ans.begin(),ans.end());
        return ans;
    }
    
    string Hexadecimal_To_Decimal(string d)
    {
        int ans=0;
        int cnt=0;
        for(int i=d.size()-1;i>=0;i--)
        {
            if(d[i]>='A'&&d[i]<='F')
            {
                ans+=(d[i]-'A'+10)*pow(16,cnt);
                
            }
            else
            {
                ans+=(d[i]-'0')*pow(16,cnt);
            }
            cnt++;
        }
        return to_string(ans);
        
    }
    vector<string> convert(int a,int b,int c,string d)
    {
        // code here
        vector<string>ans;
       ans.push_back( Decimal_To_Binary(a));
        ans.push_back(Binary_To_Decimal(b));
       ans.push_back( Decimal_To_Hexadecimal(c));
        ans.push_back(Hexadecimal_To_Decimal(d));
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
        int a,b,c;
        string d;
        cin>>a>>b>>c>>d;
        
        Solution ob;
        vector<string> ans = ob.convert(a,b,c,d);
        
        for(int i = 0;i<ans.size();i++)
        {
            cout<<ans[i]<<" ";
        }
        cout<<"\n";
    }
    return 0; 
}  // } Driver Code Ends
```

[Student record](https://practice.geeksforgeeks.org/problems/student-record1752/1/?category[]=Mathematical&category[]=Mathematical&problemStatus=unsolved&difficulty[]=-1&page=9&query=category[]MathematicalproblemStatusunsolveddifficulty[]-1page9category[]Mathematical)
```cpp
// { Driver Code Starts
#include <bits/stdc++.h>
using namespace std;

 // } Driver Code Ends
class Solution {
  public:
    string studentRecord(vector<vector<string>> S, int N) {
        // code here
        vector<string>v;
        int mx=-1;
        for(int i=0;i<N;i++){
            int avg=(stoi(S[i][1])+stoi(S[i][2])+stoi(S[i][3]))/3;
            if(avg>mx){
                v.clear();
                v.push_back(S[i][0]);
                mx=avg;
            }
            else if(avg == mx)
                v.push_back(S[i][0]);
        }
        string s;
        for(int i=0;i<v.size();i++){
            s+=v[i];
            s+=" ";
        }
        s+=to_string(mx);
        return s;
        
    }
};

// { Driver Code Starts.
int main() {
    int t;
    cin >> t;
    while (t--) {
        int N;
        cin>>N;

        string a,b,c,d;
        
        vector<vector<string>> S(N);
        
        for(int i=0; i<N; i++)
        {
            cin>>a>>b>>c>>d;
            S[i].push_back(a);
            S[i].push_back(b);
            S[i].push_back(c);
            S[i].push_back(d);
        }
        
        Solution ob;
        cout << ob.studentRecord(S,N) << endl;
    }
    return 0;
}  // } Driver Code Ends
```

[Human and the tower](https://practice.geeksforgeeks.org/problems/human-and-the-tower5254/1/?category[]=Mathematical&category[]=Mathematical&problemStatus=unsolved&difficulty[]=-1&page=9&query=category[]MathematicalproblemStatusunsolveddifficulty[]-1page9category[]Mathematical#)
```cpp
Driver Code Ends
// User function Template for C++

class Solution {
  public:
    int findHeightOrDistance(char type, double value, double angle) {
        // code here
        if(type == 'd'){
            return floor((double)(value * tan(angle * 3.14 / 180.0)));
        }  
        else if(type == 'h'){
            return floor((double)(value / tan(angle * 3.14 / 180.0)));
        }
    }
};


// { Driver Code Starts.

int main() {
    int t;
    cin >> t;
    while (t--) {
        char ch;
        double a, b;
        cin >> ch >> a >> b;
        Solution ob;
        cout << ob.findHeightOrDistance(ch, a, b) << "\n";
    }
}  // } Driver Code Ends
```

[The Remaining Cake](https://practice.geeksforgeeks.org/problems/the-remaining-cake1349/1/?category[]=Mathematical&category[]=Mathematical&problemStatus=unsolved&difficulty[]=-1&page=9&query=category[]MathematicalproblemStatusunsolveddifficulty[]-1page9category[]Mathematical#)
```cpp
 // } Driver Code Ends
// User function Template for C++

class Solution {
  public:
    double remainingCircle(double R, int N, int M) {
        // code here
        return (6.28*R*(M-N))/M;
    }
};

// { Driver Code Starts.

int main() {
    int t;
    cin >> t;
    cout << fixed << setprecision(2);
    while (t--) {
        int N, M;
        double R;
        cin >> R >> N >> M;
        Solution ob;
        cout << ob.remainingCircle(R, N, M) << "\n";
    }
}  // } Driver Code Ends
```

[Count the numbers satisfying (m + sum(m) + sum(sum(m))) equals to N](https://practice.geeksforgeeks.org/problems/count-the-numbers-satisfying-m-summ-sumsumm-equals-to-n2537/1/?category[]=Mathematical&category[]=Mathematical&problemStatus=unsolved&difficulty[]=-1&page=9&query=category[]MathematicalproblemStatusunsolveddifficulty[]-1page9category[]Mathematical#)
```cpp
ode Ends
// User function Template for C++

class Solution{
public:
    int sum(int temp){
        int sum = 0;
        while(temp > 0)
        {
           int rem = temp % 10;
           sum += rem;
           temp /= 10;
        }
    return sum;
    }
    
    int countOfNumbers(int n) {
        // code here
        int count = 0;
        for(int i = n - 97; i <= n; i++){
          if(i + sum(i) + sum(sum(i)) == n){
            count++;
          }
        }
        return count;
        
    }
};

// { Driver Code Starts.

int main(){
    int t;
    cin>>t;
    while(t--){
        int N;
        cin>>N;
        Solution ob;
        cout<<ob.countOfNumbers(N)<<endl;
    }
    return 0;
}  // } Driver Code Ends
```

[Minimum sum of factors](https://practice.geeksforgeeks.org/problems/minimum-sum-of-factors5829/1/?category[]=Mathematical&category[]=Mathematical&problemStatus=unsolved&difficulty[]=-1&page=9&query=category[]MathematicalproblemStatusunsolveddifficulty[]-1page9category[]Mathematical#)
```cpp
// { Driver Code Starts
// Initial Template for C++

#include <bits/stdc++.h>
using namespace std;

 // } Driver Code Ends
// User function Template for C++

class Solution {
  public:
    int isPrime(int N) {
        for (int i = 2; i * i <= N; i++) {
            if (N % i == 0) return 0;
        }
        return 1;
    }
    int sumOfFactors(int N) {
        int ans = 0;
        if (isPrime(N)) {
            ans++ ;
        }
        for (int i = 2; i * i <= N; i++) {
            while (N % i == 0) {
                ans += i;
                N /= i;
            }
        }
        if (N > 2) ans += N;
        return ans;
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
        int ans = ob.sumOfFactors(N);
        cout << ans << "\n";
    }
}  // } Driver Code Ends
```

[Convert floating point to natural number](https://practice.geeksforgeeks.org/problems/convert-floating-point-to-natural-number3049/1/?category[]=Mathematical&category[]=Mathematical&problemStatus=unsolved&difficulty[]=-1&page=9&query=category[]MathematicalproblemStatusunsolveddifficulty[]-1page9category[]Mathematical)
```cpp
// { Driver Code Starts

#include<bits/stdc++.h>
using namespace std;

 // } Driver Code Ends

class Solution{
	public:
	int findMinMultiple(string N){
	    // Code here
	    // Find size of string representing a
        	// floating point number.
        	int n = N.length();
        
        	// Below is used to find denominator in
        	// fraction form.
        	int count_after_dot = 0;
        
        	// Used to find value of count_after_dot
        	bool dot_seen = false;
        
        	// To find numerator in fraction form of
        	// given number. For example, for 30.25,
        	// numerator would be 3025.
        	int num = 0;
        	for (int i = 0; i < n; i++)
        	{
        		if (N[i] != '.')
        		{
        			num = num*10 + (N[i] - '0');
        			if (dot_seen == true)
        				count_after_dot++;
        		}
        		else
        			dot_seen = true;
        	}
        
        	// If there was no dot, then number
        	// is already a natural.
        	if (dot_seen == false)
        	return 1;
        
        	// Find denominator in fraction form. For example,
        	// for 30.25, denominator is 100
        	int dem = (int)pow(10, count_after_dot);
        
        	// Result is denominator divided by
        	// GCD-of-numerator-and-denominator. For example, for
        	// 30.25, result is 100 / GCD(3025,100) = 100/25 = 4
        	return (dem / __gcd(num, dem));
	    
	}
};

// { Driver Code Starts.
int main(){
	int tc;
	cin >> tc;
	while(tc--){
		string N;
		cin >> N;
		Solution ob;
		int ans = ob.findMinMultiple(N);
		cout << ans << "\n";
	}
	return 0;
}  // } Driver Code Ends
```

[Cricket Average](https://practice.geeksforgeeks.org/problems/cricket-average2031/1/?category[]=Mathematical&category[]=Mathematical&problemStatus=unsolved&difficulty[]=-1&page=9&query=category[]MathematicalproblemStatusunsolveddifficulty[]-1page9category[]Mathematical)
```cpp
er Code Ends


class Solution{
	public:
	int Average(vector<int>run, vector<string>status){
	    // Code here
	    int sum = 0;
        int out = 0;
        
        for(int i = 0; i < run.size(); i++)
        {
            sum += run[i];
            
            if(status[i] == "out")
            {
                out++;
            }
        }
        
        if(out == 0)
        {
            return -1;
        }
        
        return ceil(sum / (double) out);
	}
};

// { Driver Code Starts.
int main(){
	int tc;
	cin >> tc;
	while(tc--){
		int n;
		cin >> n;
		vector<int>run(n);
		vector<string>status(n);
		for(int i = 0; i < n; i++){
			cin >> run[i] >> status[i];
		}
		Solution ob;
		int ans = ob.Average(run, status);
		cout << ans << "\n";
	}
	return 0;
}  // } Driver Code Ends
```

[The Cycle Game](https://practice.geeksforgeeks.org/problems/the-cycle-game4441/1/?category[]=Mathematical&category[]=Mathematical&problemStatus=unsolved&difficulty[]=-1&page=9&query=category[]MathematicalproblemStatusunsolveddifficulty[]-1page9category[]Mathematical#)
```cpp
Ends


class Solution{
	public:
   	int find_division(int x, int y, int n){
   	    // Code here.
   	    if(n % 2 == 0){
   	        return max(x,y) / min(x,y);
   	    }
   	    else{
   	        x = x * 2;
   	        return max(x,y) / min(x,y);
   	    }
   	}    
};

// { Driver Code Starts.
int main(){
	int tc;
	cin >> tc;
	while(tc--){
		int x, y, n;
		cin >> x>> y >> n;
		Solution ob;
		int ans = ob.find_division(x, y, n);
		cout << ans <<"\n";
	}  
	return 0;
}  // } Driver Code Ends
```

[Long Long Decimal](https://practice.geeksforgeeks.org/problems/long-long-decimal4552/1/?category[]=Mathematical&category[]=Mathematical&problemStatus=unsolved&difficulty[]=-1&page=9&query=category[]MathematicalproblemStatusunsolveddifficulty[]-1page9category[]Mathematical)
```cpp
// { Driver Code Starts


#include<bits/stdc++.h>
using namespace std;

 // } Driver Code Ends


class Solution{
	public:
   	string upto_K_places(int k){
   	    // Code here
   	    int a = 355, b = 113;
   		string res = "";
   		for(int i = 0; i <= k; i++){
   			res += char((a/b) + '0');
   			if(i == 0 and k > 0)
   				res += '.';
   			a = (a%b)*10;
   		}
   		return res;
   	}    
};

// { Driver Code Starts.
int main(){
	int tc;
	cin >> tc;
	while(tc--){
		int k;
		cin >> k;
		Solution ob;
		string ans = ob.upto_K_places(k);
		cout << ans <<"\n";
	}  
	return 0;
}  // } Driver Code Ends
```

[Gray Code](https://practice.geeksforgeeks.org/problems/gray-code4907/1/?category[]=Mathematical&category[]=Mathematical&problemStatus=unsolved&difficulty[]=-1&page=1&query=category[]MathematicalproblemStatusunsolveddifficulty[]-1page1category[]Mathematical)
```cpp
de Ends
class Solution {
  public:
    int getGray(int n) {
        // code here
        return n ^ (n >> 1);
    }
};

// { Driver Code Starts.
int main() {
    int t;
    cin >> t;
    while (t--) {
        int n;
        
        cin>>n;

        Solution ob;
        cout << ob.getGray(n) << endl;
    }
    return 0;
}  // } Driver Code Ends
```

[Divide the number](https://practice.geeksforgeeks.org/problems/divide-the-number5320/1/?category[]=Mathematical&category[]=Mathematical&problemStatus=unsolved&difficulty[]=-1&page=1&query=category[]MathematicalproblemStatusunsolveddifficulty[]-1page1category[]Mathematical)
```cpp
// { Driver Code Starts
#include<bits/stdc++.h> 
using namespace std;

 // } Driver Code Ends
class Solution{
public:
    int countWays(int N){ 
        // code here
        int counter = 0;
        
        for(int i = 1; i < N; i++){
            for(int j = i; j < N; j++){
                for(int k = j; k < N; k++){
                    for(int l = k; l < N; l++){
                        if(i + j + k + l == N){
                            counter++;
                        }
                    }
                }
            }
        }
        return counter;
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
        cout << ob.countWays(N) << endl;
    }
    return 0; 
}  // } Driver Code Ends
```

[Number of Integer solutions](https://practice.geeksforgeeks.org/problems/number-of-integer-solutions2458/1/?category[]=Mathematical&category[]=Mathematical&problemStatus=unsolved&difficulty[]=-1&page=1&query=category[]MathematicalproblemStatusunsolveddifficulty[]-1page1category[]Mathematical#)
```cpp
Code Ends

class Solution {
  public:
    long long noOfIntSols(long long N) {
        // code here
        return ((N + 1) * (N + 2)) / 2;
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
        cout << ob.noOfIntSols(N) << endl;
    }
    return 0;
}  // } Driver Code Ends
```

[Factorial](https://practice.geeksforgeeks.org/problems/factorial5739/1/?category[]=Mathematical&category[]=Mathematical&problemStatus=unsolved&difficulty[]=-1&page=1&query=category[]MathematicalproblemStatusunsolveddifficulty[]-1page1category[]Mathematical#)
```cpp
Ends
class Solution{
public:
    long long int factorial(int N){
        //code here
        if(N == 0 || N == 1) return 1;
        else return N * factorial(N - 1);
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
        cout << ob.factorial(N) << endl;
    }
    return 0; 
}  // } Driver Code Ends
```

[Difference series](https://practice.geeksforgeeks.org/problems/difference-series4345/1/?category[]=Mathematical&category[]=Mathematical&problemStatus=unsolved&difficulty[]=-1&page=1&query=category[]MathematicalproblemStatusunsolveddifficulty[]-1page1category[]Mathematical)
```cpp
ode Ends
class Solution
{
public:
    int differenceSeries(int N)
    {
        // Write Your Code here
        return (N * (2 * N + 1));
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
        int ans = ob.differenceSeries(N);
        cout << ans << endl;
    }
    return 0;
}  // } Driver Code Ends
```

[Check if the number is Fibonacci](https://practice.geeksforgeeks.org/problems/check-if-the-number-is-fibonacci4654/1/?category[]=Mathematical&category[]=Mathematical&problemStatus=unsolved&difficulty[]=-1&page=1&query=category[]MathematicalproblemStatusunsolveddifficulty[]-1page1category[]Mathematical)
```cpp
ode Ends
class Solution{   
public:
    string checkFibonacci(int N){
        // code here 
        int n1 = N * N * 5 + 4;
        int n2 = N * N * 5 - 4;
        int n3 = sqrt(n1);
        int n4 = sqrt(n2);
        
        if(n3 * n3 == n1 || n4 * n4 == n2) return "Yes";
        else return "No";
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
        cout << ob.checkFibonacci(N) << endl;
    }
    return 0; 
}   // } Driver Code Ends
```

[Sum of Digits Divisibility](https://practice.geeksforgeeks.org/problems/sum-of-digits-divisibility5311/1/?category[]=Mathematical&category[]=Mathematical&problemStatus=unsolved&difficulty[]=-1&page=1&query=category[]MathematicalproblemStatusunsolveddifficulty[]-1page1category[]Mathematical#)
```cpp
} Driver Code Ends
// User function template for C++

class Solution {
  public:
    int isDivisible(int N) {
        // code here
        int num = N;
        int sum = 0;
        while(num > 0){
           sum += (num % 10);
           num /= 10;
        }
        if(N % sum == 0) return 1;
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
        cout << ob.isDivisible(N) << "\n";
    }
}  // } Driver Code Ends
```

[One's Complement](https://practice.geeksforgeeks.org/problems/ones-complement5928/1/?category[]=Mathematical&category[]=Mathematical&problemStatus=unsolved&difficulty[]=-1&page=1&query=category[]MathematicalproblemStatusunsolveddifficulty[]-1page1category[]Mathematical#)
```cpp
 Driver Code Ends
class Solution{
public:
    int onesComplement(int N){
        //code here
        
        // Find number of bits in the given integer 
        int number_of_bits = floor(log2(N))+1; 
        
        // XOR the given integer with poe(2,  
        // number_of_bits-1 and print the result  
        return ((1 << number_of_bits) - 1) ^ N;
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
        
        Solution ob;
        cout<<ob.onesComplement(n)<<"\n";
    }
}  // } Driver Code Ends
```

[Extended Euclidean Algorithm](https://practice.geeksforgeeks.org/problems/extended-euclidean-algorithm3848/1/?category[]=Mathematical&category[]=Mathematical&problemStatus=unsolved&difficulty[]=-1&page=1&query=category[]MathematicalproblemStatusunsolveddifficulty[]-1page1category[]Mathematical)
```cpp
// { Driver Code Starts



#include<bits/stdc++.h> 
using namespace std;

 // } Driver Code Ends


class Solution{
int extendedEuclideanAlgorithm(int a, int b, int &x, int &y)
    {
        if(b == 0)
        {
            x = 1;
            y = 0;
            
            return a;
        }
        
        int x1, y1;
        int g = extendedEuclideanAlgorithm(b, a % b, x1, y1);
        
        x = y1;
        y = x1 - (a / b) * y1;
        
        return g;
        
    }
    
    public:
    vector<int> gcd(int a, int b)
    {
        int x, y, g;
        
        g = extendedEuclideanAlgorithm(a, b, x, y);
        
        return {g, x, y};
    }
};

// { Driver Code Starts.
int main() 
{ 
    int t;
    cin>>t;
    while(t--)
    {
        int a,b;
        cin>>a>>b;
        Solution ob;
        vector<int> v = ob.gcd(a,b);
        if(v.size()!=3)
            return 0;
        cout<<v[0]<<" "<<v[1]<<" "<<v[2]<<"\n";
    }
    return 0; 
}  // } Driver Code Ends
```

[Middle of Three](https://practice.geeksforgeeks.org/problems/middle-of-three2926/1/?category[]=Mathematical&category[]=Mathematical&problemStatus=unsolved&difficulty[]=-1&page=1&query=category[]MathematicalproblemStatusunsolveddifficulty[]-1page1category[]Mathematical)
```cpp
 Driver Code Ends
//User function template for C++

class Solution{
  public:
    int middle(int A, int B, int C){
        //code here//Position this line where user code will be pasted
        if(A > B){
            if(B > C) return B; // A > B > C
            else if(A > C) return C; // A > C > B
            else return A; // C > A > B
        }
        else{
           if(A > C) return A; // B > A > C
           else if(B > C) return C; // B > C > A
           else return B; // C > B > A
        } 
    }
};

// { Driver Code Starts.
int main()
{
    int t;
    cin>>t;
    while(t--)
    {
        int A,B,C;
        cin>>A>>B>>C;
        Solution ob;
        cout<<ob.middle(A,B,C) <<"\n";
    }
    return 0;
}  // } Driver Code Ends
```

[Smallest divisible number](https://practice.geeksforgeeks.org/problems/smallest-divisible-number/1/?category[]=Mathematical&category[]=Mathematical&problemStatus=unsolved&difficulty[]=-1&page=1&query=category[]MathematicalproblemStatusunsolveddifficulty[]-1page1category[]Mathematical)
```cpp
// { Driver Code Starts
//Initial template for C++

#include <bits/stdc++.h>
using namespace std;

 // } Driver Code Ends
//User function template for C++

class Solution{
public:
    long long GCD(long long int a,long long int b){
        if(b == 0) return a;
        else return GCD(b,a % b);
    }
    
    long long LCM(long long int a,long long int b){
        return (a * b) / GCD(a,b);
    }
    
    long long getSmallestDivNum(long long n){
        // code here
        long result = 1;
        for(long i = 2; i <= n; i++){
            result = LCM(result,i);
        }
        return result;
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
        Solution ob;
        cout<< ob.getSmallestDivNum(n)<<endl;
    }
    return 0;
}  // } Driver Code Ends
```

[Repeated sum of digits](https://practice.geeksforgeeks.org/problems/repeated-sum-of-digits3955/1/?category[]=Mathematical&category[]=Mathematical&problemStatus=unsolved&difficulty[]=-1&page=1&query=category[]MathematicalproblemStatusunsolveddifficulty[]-1page1category[]Mathematical#)
```cpp
 Driver Code Ends
class Solution{   
public:
    
    int repeatedSumOfDigits(int N){
        // code here 
        
        if(N < 10) return N;
        
        int sum = 0;
        while(N > 0){
            sum += (N % 10);
            N /= 10;
        }
        return repeatedSumOfDigits(sum);
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
        cout << ob.repeatedSumOfDigits(N) << endl;
    }
    return 0; 
}   // } Driver Code Ends
```

[Sieve of Eratosthenes](https://practice.geeksforgeeks.org/problems/sieve-of-eratosthenes5242/1/?category[]=Mathematical&category[]=Mathematical&problemStatus=unsolved&difficulty[]=-1&page=1&query=category[]MathematicalproblemStatusunsolveddifficulty[]-1page1category[]Mathematical)
```cpp
// { Driver Code Starts
#include<bits/stdc++.h> 
using namespace std; 

 // } Driver Code Ends
//User function Template for C++
class Solution
{
public:
    vector<int> sieveOfEratosthenes(int N)
    {
        // Write Your Code here
        bool prime[N+1]={0};
        for(int i=2;i*i<=N;i++){
            if(prime[i]==0){
                for(int j=i*i;j<=N;j+=i){
                    prime[j]=1;
                }
            }
        }
        vector<int>v;
        for(int i=2;i<=N;i++){
            if(prime[i]==0)
                v.push_back(i);
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
        vector<int> primes  = ob.sieveOfEratosthenes(N);
        for(auto prime : primes) {
            cout<< prime <<" ";
        }
        cout<<endl;
    }
    return 0;
}  // } Driver Code Ends
```

[Carol Number](https://practice.geeksforgeeks.org/problems/carol-number4645/1/?category[]=Mathematical&category[]=Mathematical&problemStatus=unsolved&difficulty[]=-1&page=1&query=category[]MathematicalproblemStatusunsolveddifficulty[]-1page1category[]Mathematical#)
```cpp
// { Driver Code Starts
#include <bits/stdc++.h>
using namespace std;

 // } Driver Code Ends
class Solution {
  public:
    int nthCarol(int N) {
        // code here
        if(N == 1) return 1;
        else  return pow(4,N) - pow(2,(N + 1)) - 1;
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
        cout << ob.nthCarol(N) << endl;
    }
    return 0;
}  // } Driver Code Ends
```

[Add two fractions](https://practice.geeksforgeeks.org/problems/add-two-fractions/1/?category[]=Mathematical&category[]=Mathematical&problemStatus=unsolved&difficulty[]=-1&page=1&query=category[]MathematicalproblemStatusunsolveddifficulty[]-1page1category[]Mathematical#)
```cpp
// { Driver Code Starts
#include<bits/stdc++.h>
using namespace std;


void addFraction(int num1, int den1, int num2,
                 int den2);

int main()
{
    int T;
    cin>>T;
    while(T--)
    {
        int a,b,c,d,resultNum,resultDen;
        cin>>a>>b>>c>>d;
        addFraction(a,b,c,d);

    }
}
// } Driver Code Ends


/*You are required to complete this function*/
void addFraction(int num1, int den1, int num2,int den2)
{
//Your code here
  int gcd;
  int num = num1 * den2 + num2 * den1;
  int den = den1 * den2;
  
  for(int i = 1; i <= num && i <= den; i++){
      if(num % i == 0 && den % i == 0) gcd = i;
  }
  
  cout << num / gcd << "/" << den / gcd << endl;
 }
```

[Count numbers divisible by M](https://practice.geeksforgeeks.org/problems/count-numbers-divisible-by-m1524/1/?category[]=Mathematical&category[]=Mathematical&problemStatus=unsolved&difficulty[]=-1&page=1&query=category[]MathematicalproblemStatusunsolveddifficulty[]-1page1category[]Mathematical#)
```cpp
// { Driver Code Starts
// Initial Template for C++
#include <bits/stdc++.h>
using namespace std;

 // } Driver Code Ends
// User function Template for C++
class Solution {
  public:
    int countDivisibles(int A, int B, int M) {
        // code here
        int count = 0;
        for(int i = A; i <= B; i++){
            if(i % M == 0) count++;
        }
        return count;
    }
};

// { Driver Code Starts.
int main() {
    int t;
    cin >> t;
    while (t--) {
        int A, B, M;
        cin >> A >> B >> M;
        Solution ob;
        cout<<ob.countDivisibles(A, B, M)<<endl;
    }
    return 0;
}
  // } Driver Code Ends
```

[Distance and Displacement](https://practice.geeksforgeeks.org/problems/distance-and-displacement4145/1/?category[]=Mathematical&category[]=Mathematical&problemStatus=solved&difficulty[]=-1&page=2&query=category[]MathematicalproblemStatussolveddifficulty[]-1page2category[]Mathematical)
```cpp
// { Driver Code Starts
// Initial Template for C++

#include <bits/stdc++.h>
using namespace std;

 // } Driver Code Ends
// User function Template for C++

class Solution{
public:
    int distance(int n, int a[], char d[]){
        // code here
        int c = 0;
        int b = 0;
        int sum = 0;
        
        for(int i = 0; i < n; i++){
            if(d[i] == 'E') c += a[i];
            if(d[i] == 'W') c -= a[i];
            if(d[i] == 'N') b += a[i];
            if(d[i] == 'S') b -= a[i];
            sum += a[i];
        }
        int m = c * c + b * b;
        return ceil(sqrt(m) + sum); // sqrt(m) = displacement and sum is distance
    }
};

// { Driver Code Starts.

int main(){
    int t;
    cin>>t;
    while(t--){
        int n;
        cin>>n;
        int a[n];
        char d[n];
        for(int i = 0;i < n;i++)
            cin>>a[i];
        for(int i = 0;i < n;i++)
            cin>>d[i];
            
        Solution ob;
        cout<<ob.distance(n, a, d)<<"\n";
    }
    return 0;
}  // } Driver Code Ends
```

[LCM And GCD](https://practice.geeksforgeeks.org/problems/lcm-and-gcd4516/1/?category[]=Mathematical&category[]=Mathematical&problemStatus=unsolved&difficulty[]=-1&page=1&query=category[]MathematicalproblemStatusunsolveddifficulty[]-1page1category[]Mathematical#)
```cpp

using namespace std;

 // } Driver Code Ends
class Solution {
  public:
  
    long long gcd(long long x,long long y){return !y?x:gcd(y,x%y);}
    
    vector<long long> lcmAndGcd(long long A , long long B) {
        // code here
        long long GCD = gcd(A,B);
        vector<long long> ans;
        ans.push_back((A*B)/GCD);
        ans.push_back(GCD);
        return ans;
    }
};

// { Driver Code Starts.
int main() {
    int t;
    cin >> t;
    while (t--) {
        long long A,B;
        
        cin>>A>>B;

        Solution ob;
        vector<long long> ans = ob.lcmAndGcd(A,B);
        cout<<ans[0]<<" "<<ans[1]<<endl;
    }
    return 0;
}  // } Driver Code Ends
```

[Reading books](https://practice.geeksforgeeks.org/problems/reading-books3803/1/?category[]=Mathematical&category[]=Mathematical&problemStatus=unsolved&difficulty[]=-1&page=1&query=category[]MathematicalproblemStatusunsolveddifficulty[]-1page1category[]Mathematical#)
```cpp
// { Driver Code Starts
//Initial Template for C++

#include <bits/stdc++.h>
using namespace std;

 // } Driver Code Ends
//User function Template for C++

class Solution{
public:
    long long maxPoint(int N, int K, long long A[], long long B[])
    {
        // code here
        long long result = 0;
        for(int i = 0; i < N; i++){
            result = max(result,((K / A[i]) * B[i]));
        }
        return result;
    }
};

// { Driver Code Starts.

int main(){
    int t;
    cin>>t;
    while(t--){
        int N, K;
        cin>>N>>K;
        long long A[N], B[N];
        for(int i = 0;i < N;i++)
            cin>>A[i];
        for(int i = 0;i < N;i++)
            cin>>B[i];
        
        Solution ob;
        cout<<ob.maxPoint(N, K, A, B)<<"\n";
    }
    return 0;
}  // } Driver Code Ends
```

[Find The Sequence](https://practice.geeksforgeeks.org/problems/find-the-sequence1346/1/?category[]=Mathematical&category[]=Mathematical&problemStatus=unsolved&difficulty[]=-1&page=1&query=category[]MathematicalproblemStatusunsolveddifficulty[]-1page1category[]Mathematical#)
```cpp
// { Driver Code Starts
#include<bits/stdc++.h> 
using namespace std; 

 // } Driver Code Ends
class Solution
{
public:
    vector<long long> printSeries(int n)
    {
        // Write your code here
        vector<long long> v;
        long long a = 1;
        long long b = 2;
        long long c = 5;
        
        if(n == 1){
            v.push_back(a);
            return v;
        }
        
        else if(n == 2){
            v.push_back(a);
            v.push_back(b);
            return v;
        }
        
        else if(n == 3){
            v.push_back(a);
            v.push_back(b);
            v.push_back(c);
            return v;
        }
        
        
           v.push_back(a);
           v.push_back(b);
           v.push_back(c); 
           
           for(long long i = 4; i <= n; i++){
               long long d = a + b + c;
               v.push_back(d);
               long long temp = a;
               a = b;
               b = c;
               c = d;
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
        cin >> N;
        
        Solution ob;
        vector<long long> a = ob.printSeries(N);
        
        for(long long i=0;i<N;i++){
            cout<<a[i]<<" ";
        }
        cout<<endl;
        
    }
    return 0;
}  // } Driver Code Ends
```

[Sum of divisors](https://practice.geeksforgeeks.org/problems/sum-of-divisors3601/1/?category[]=Mathematical&category[]=Mathematical&problemStatus=unsolved&difficulty[]=-1&page=1&query=category[]MathematicalproblemStatusunsolveddifficulty[]-1page1category[]Mathematical)
```cpp
// { Driver Code Starts
// Initial Template for C++
#include <bits/stdc++.h>
using namespace std;

 // } Driver Code Ends
// User function Template for C++
typedef long long int lli;
class Solution {
  public:
    long long int divSum(long long int n){
        // code here
        lli sum = 0;
        for(lli i = 1; i < n; i++){
            if(n % i == 0){
                sum += i;
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
        long long int n;
        cin >> n;
        Solution ob;
        cout<<ob.divSum(n)<<endl;
    }
    return 0;
}
  // } Driver Code Ends
```

[GCD of Array](https://practice.geeksforgeeks.org/problems/gcd-of-array0614/1/?category[]=Mathematical&category[]=Mathematical&problemStatus=unsolved&difficulty[]=-1&page=1&query=category[]MathematicalproblemStatusunsolveddifficulty[]-1page1category[]Mathematical#)
```cpp
// { Driver Code Starts
#include <bits/stdc++.h>
using namespace std;

 // } Driver Code Ends
class Solution
{
	public:
	
	int GCD(int a, int b){
	    if(a == 0) return b;
	    else return GCD(b % a,a);
	}
	
    int gcd(int N, int arr[])
    {
    	// Your code goes here
    	if(N == 1) return arr[0];
    	
    	int ans = GCD(arr[0],arr[1]);
    	for(int i = 2; i < N; i++) ans = GCD(ans,arr[i]);
    	
    	return ans;
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

        int arr[N];
        for(int i = 0; i < N; i++)
        	cin >> arr[i];
        Solution ob;
       	cout <<  ob.gcd(N, arr) << "\n";
   
    }
    return 0;
}  // } Driver Code Ends
```

[Repetitive Addition Of Digits](https://practice.geeksforgeeks.org/problems/repetitive-addition-of-digits2221/1/?category[]=Mathematical&category[]=Mathematical&problemStatus=unsolved&difficulty[]=-1&page=1&query=category[]MathematicalproblemStatusunsolveddifficulty[]-1page1category[]Mathematical#)
```cpp
// { Driver Code Starts
#include<bits/stdc++.h> 
using namespace std; 

 // } Driver Code Ends
//User function Template for C++
typedef long long ll;
class Solution
{
public:
    int singleDigit(long long N)
    {
        // Write Your Code here
        ll sum = 0;
        
        while(N > 0 || sum > 9){
            if(N == 0){
                N = sum;
                sum = 0;
            }
            
            sum += (N % 10);
            N /= 10;
        }
        return sum;
    }
};

// { Driver Code Starts.
int main()
{
    int t;
    cin >> t;
    while (t--)
    {
        long long N;
        cin>>N;
        Solution ob;
        int ans  = ob.singleDigit(N);
        cout<<ans<<endl;
    }
    return 0;
}  // } Driver Code Ends
```

[Difference between sums of odd and even digits](https://practice.geeksforgeeks.org/problems/difference-between-sums-of-odd-and-even-digits2837/1/?category[]=Mathematical&category[]=Mathematical&problemStatus=unsolved&difficulty[]=-1&page=1&query=category[]MathematicalproblemStatusunsolveddifficulty[]-1page1category[]Mathematical#)
```cpp
// { Driver Code Starts
// Initial Template for C++

#include <bits/stdc++.h>
using namespace std;

 // } Driver Code Ends
// User function Template for C++

class Solution {
  public:
    int oddAndEven(string S) {
        // code here
        int even = 0, odd = 0;
        
        for(int i = 0; i < S.size(); i++){
            if(i % 2 == 0) even += S[i] - '0';
            else odd += S[i] - '0';
        }
        
        return (even == odd) ? 1 : 0;
    }
};

// { Driver Code Starts.
int main() {
    int t;
    cin >> t;
    while (t--) {
        string S;
        cin >> S;
        Solution ob;
        cout << ob.oddAndEven(S) << "\n";
    }
}  // } Driver Code Ends
```

[Count numbers containing 4](https://practice.geeksforgeeks.org/problems/count-numbers-containing-43022/1/?category[]=Mathematical&category[]=Mathematical&problemStatus=unsolved&difficulty[]=-1&page=1&query=category[]MathematicalproblemStatusunsolveddifficulty[]-1page1category[]Mathematical#)
```cpp
// { Driver Code Starts
#include <bits/stdc++.h>
using namespace std;

 // } Driver Code Ends
class Solution {
  public:
    int countNumberswith4(int N) {
        // code here
        int count = 0;
        for(int i = 1; i <= N; i++){
            count += has4(i) ? 1 : 0;
        }
        return count;     
    }
    
    bool has4(int x){
        while(x != 0){
            if(x % 10 == 4) return true;
            x = x / 10;
        }
        return false;
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
        cout << ob.countNumberswith4(N) << endl;
    }
    return 0;
}  // } Driver Code Ends
```

[Find the fine](https://practice.geeksforgeeks.org/problems/find-the-fine4353/1/?category[]=Mathematical&category[]=Mathematical&problemStatus=unsolved&difficulty[]=-1&page=1&query=category[]MathematicalproblemStatusunsolveddifficulty[]-1page1category[]Mathematical#)
```cpp
// { Driver Code Starts
#include <bits/stdc++.h>
using namespace std;



 // } Driver Code Ends

typedef long long int lli;
class Solution{
  public:
    long long int totalFine(int n, int date, int car[], int fine[])
    {
        lli sum1 = 0, sum2 = 0;
        
        for(lli i = 0; i < n; i++){
            
                if(car[i] % 2 != 0) sum1 += fine[i];
                else sum2 += fine[i];
        }
        
        if(date % 2 == 0) return sum1;
        else return sum2;
        
    }
};

// { Driver Code Starts.
int main() {
    int t;
    cin >> t;
    while (t--) {
        int n, i, date;
        cin >> n >> date;
        int car[n], fine[n];
        
        for (i = 0; i < n; i++){
            cin >> car[i];
        }
        for (int i = 0; i < n; i++) {
            cin >> fine[i];
        }
        Solution obj;
        cout << obj.totalFine(n, date, car, fine) << endl;
    }
    return 0;
}
  // } Driver Code Ends
```

[Check if divisible by 11](https://practice.geeksforgeeks.org/problems/check-if-divisible-by-114724/1/?category[]=Mathematical&category[]=Mathematical&problemStatus=unsolved&difficulty[]=-1&page=1&query=category[]MathematicalproblemStatusunsolveddifficulty[]-1page1category[]Mathematical#)
```cpp
// { Driver Code Starts
#include<bits/stdc++.h>
using namespace std;


 // } Driver Code Ends
//User function template for C++
class Solution{
public:	
	
	int divisibleBy11 (string S)
	{
	    // Your Code Here
	    int even = 0, odd = 0;
        
        for(int i = 0; i < S.size(); i++){
            if(i % 2 == 0) odd += S[i] - '0';
            else even += S[i] - '0';
        }
        
        return abs(odd - even) % 11 == 0 ? 1 : 0;
	}
};

// { Driver Code Starts.

int main()
{
	int t; cin >> t;
	while (t--)
	{
		string s; cin >> s;
		Solution ob;
		cout << ob.divisibleBy11 (s) << endl;
	}
}

// Contributed By: Pranay Bansal
  // } Driver Code Ends
```

[Point lies or not](https://practice.geeksforgeeks.org/problems/point-lies-or-not0417/1/?category[]=Mathematical&category[]=Mathematical&problemStatus=unsolved&difficulty[]=-1&page=1&query=category[]MathematicalproblemStatusunsolveddifficulty[]-1page1category[]Mathematical)
```cpp
// { Driver Code Starts

#include <bits/stdc++.h>
using namespace std;

 // } Driver Code Ends

class Solution {
  public:
    float area(int x1, int y1, int x2, int y2, int x3, int y3)
    {
        return abs((x1*(y2-y3)+x2*(y3-y1)+x3*(y1-y2))/2.0);
    }
    
    string isInsideTri(int x1, int y1, int x2, int y2, int x3, int y3, int x, int y) {
        // code here
        float A=area(x1,y1,x2,y2,x3,y3);
        float A1=area(x,y,x2,y2,x3,y3);
        float A2=area(x1,y1,x,y,x3,y3);
        float A3=area(x1,y1,x2,y2,x,y);
        if(A==A1+A2+A3)
           return "Yes";
        return "No";
    }
};

// { Driver Code Starts.
int main() {
    int t;
    cin >> t;
    while (t--) {
        int x1,y1,x2,y2,x3,y3,x,y;
        
        cin>>x1>>y1>>x2>>y2>>x3>>y3;
        cin>>x>>y;

        Solution ob;
        cout << ob.isInsideTri(x1,y1,x2,y2,x3,y3,x,y) << endl;
    }
    return 0;
}  // } Driver Code Ends
```

[Square Divisors](https://practice.geeksforgeeks.org/problems/square-divisors4319/1/?category[]=Mathematical&category[]=Mathematical&problemStatus=unsolved&difficulty[]=-1&page=7&query=category[]MathematicalproblemStatusunsolveddifficulty[]-1page7category[]Mathematical)
```cpp
// { Driver Code Starts
// Initial Template for C++

#include <bits/stdc++.h>
using namespace std;

 // } Driver Code Ends
// User function Template for C++

class Solution{
public:
    int squareFactor(long long N){
        // code here
        int count=0;
        
        for(int i=1;i <= sqrt(N);i++) {
            if(N%(i*i) == 0)
            count++;
        }
        return count;
    }
};

// { Driver Code Starts.

int main(){
    int t;
    cin>>t;
    while(t--){
        long long N;
        cin>>N;
        
        Solution ob;
        cout<<ob.squareFactor(N)<<"\n";
    }
    return 0;
}  // } Driver Code Ends
```

[Product is even or odd?](https://practice.geeksforgeeks.org/problems/product-is-even-or-odd3020/1/?category[]=Mathematical&category[]=Mathematical&problemStatus=unsolved&difficulty[]=-1&page=6&query=category[]MathematicalproblemStatusunsolveddifficulty[]-1page6category[]Mathematical#)
```cpp
// { Driver Code Starts
#include <iostream>
using namespace std;

int EvenOdd(string n1 , string n2);

// driver code
int main()
{
   int t;
   cin>>t;
   for(int i=0;i<t;i++)
   {
       string n1;
       cin>>n1;
       string n2;
       cin>>n2;
       cout<<EvenOdd(n1 , n2)<<endl;
   }
    return 0;
}
// } Driver Code Ends


int EvenOdd(string n1 , string n2)
{
    //code here.
    return (n1[n1.length() - 1] * n2[n2.length() - 1]) % 2 == 0 ? 1 : 0;
}
```

[Product of factors of number](https://practice.geeksforgeeks.org/problems/product-of-factors-of-number4757/1/?category[]=Mathematical&category[]=Mathematical&problemStatus=unsolved&difficulty[]=-1&page=5&query=category[]MathematicalproblemStatusunsolveddifficulty[]-1page5category[]Mathematical#)
```cpp
// { Driver Code Starts
// Initial Template for C++

#include <bits/stdc++.h>
using namespace std;

 // } Driver Code Ends
// User function template for C++
#define M 1000000007
typedef long long ll;
class Solution {
  public:
    int factorProduct(int n) {
        // code here
        ll prod = 1;
        for (int i = 1; i * i <= n; i++)
        {
        if (n % i == 0)
        {
            // If factors are equal,
            // multiply only once
            if (n / i == i)
                prod = (prod * i) % M;
 
            // Otherwise multiply both
            else {
                prod = (prod * i) % M;
                prod = (prod * n / i) % M;
            }
        }
    }
    return prod;
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
        cout << ob.factorProduct(N) << "\n";
    }
}  // } Driver Code Ends
```

[Sum of fifth powers of the first n natural numbers](https://practice.geeksforgeeks.org/problems/sum-of-fifth-powers-of-the-first-n-natural-numbers3415/1/?category[]=Mathematical&category[]=Mathematical&problemStatus=unsolved&difficulty[]=-1&page=5&query=category[]MathematicalproblemStatusunsolveddifficulty[]-1page5category[]Mathematical#)
```cpp
// { Driver Code Starts
// Initial template for C++

#include <bits/stdc++.h>
using namespace std;

 // } Driver Code Ends
// User function template for C++

class Solution {
  public:
    long long sumOfFifthPowers(long long n) {
        // code here
        return ((2 * n * n * n * n * n * n) +
           (6 * n * n * n * n * n) +
           (5 * n * n * n * n) -
           (n * n)) / 12;
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
        cout << ob.sumOfFifthPowers(N) << "\n";
    }
}  // } Driver Code Ends
```

[]()
```cpp

```

[]()
```cpp

```

[]()
```cpp

```

[]()
```cpp

```

[]()
```cpp

```

[]()
```cpp

```

[]()
```cpp

```

[]()
```cpp

```

[]()
```cpp

```

[]()
```cpp

```

[]()
```cpp

```

[]()
```cpp

```

[]()
```cpp

```

[]()
```cpp

```



