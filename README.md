# C---Chocolate-Bunny
#include <bits/stdc++.h>
using namespace std;
#define ull unsigned long long
#define ll long long
#define ld long double


int main() {

    int n;
    cin>>n;
    vector<int> A(n+1,0);
    A[0]=0;
    int k1,k2;
    int x=1,y=2;
    for(int i=1;i<=n-1;i++){
        cout<<"?"<<" "<<x<<" "<<y<<endl;
        cin>>k1;
        cout<<"?"<<" "<<y<<" "<<x<<endl;
        cin>>k2;
        if(k1>k2){
            A[x]=k1;
            x=y;
            y++;
        }else{
            A[y]=k2;
            y++;
        }
    }
    cout<<"!"<<" ";
    for(int i=1;i<A.size();i++){

        if(A[i]==0){
            cout<<n<<" ";
        }else{
            cout<<A[i]<<" ";
        }

    }
    int verdict;
    cin>>verdict;
    return 0;
}





