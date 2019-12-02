# Diffie-Hellman-Key-Exchange
#include<iostream>

using namespace std;

#include<math.h>

#include<vector>
#include<cstring>
#include <iostream>
#include <cmath>
using namespace std;


long long int p;
long long int g;
long long int x1;
long long int x2;
long long int a;
long long int b;
long long int y11;
long long int y22;
long long int k1;

long long int k2;
long long int k3;
long long int k4;
 int main( )

{

cout<<"\n\n\t Enter value of p & g =";

cin>>p>>g;

cout<<"\n\n\t Enter value of xA & xB =";

cin>>x1>>x2;

a=pow(g,x1);
y11=(long long int)a%p;

cout<<"\n\t YA:"<<y11;


b=pow(g,x2);
y22=(long long int)b%p;

cout<<"\n\t YB:"<<y22;


if (y22=!0)
{
    k1=pow(y22,x1);
    k2=(long long int)k1%p;
    cout<<"\n\t k:"<<k2;

    if(y11!=0)
    {
         k3=pow(y11,x2);
    k4=(long long int)k3%p;
    cout<<"\n\t k:"<<k4;

    if(k2==k4)
    {
        cout<<"new key generated"<<k2;
    }

    }
    }
     ///cout<<"\n\n\t no key generated";
    return 0;

}







