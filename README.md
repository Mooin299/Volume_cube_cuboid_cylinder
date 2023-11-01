# Volume_cube_cuboid_cylinder
#include <iostream>
#include<cmath>
using namespace std;

float vol(float side)
{
    return side*side*side;
}
float vol(float l,float b,float h)
{
    return l*b*h;
}
float vol(float r,float h)
{
    return (M_PI*r*r*h);
}

int main() 
{
    
    int choice;
    float side,l,b,h,r;
    char ch;
    do
    {
        cout<<"Enter Your Choice: \n";
        cout<<"1.Cube\n";
        cout<<"2.Cuboid\n";
        cout<<"3.Cylinder\n";
        cin>>choice;
        
        if(choice==1)
        {
            cout<<"\nLength of the side is ";
            cin>>side;
            cout<<"\nVolume of the cube is:\t"<<vol(side)<<" cubic metre";
            
        }
        if(choice==2)
        {
            cout<<"\nLength,Breadth and Height of the cuboid is ";
            cin>>l>>b>>h;
            cout<<"\nVolume of the cuboid is:\t"<<vol(l,b,h)<<" cubic metre"<<endl;
            
        }
        if(choice==3)
        {
            cout<<"\nRadius and Height of the cylinder is ";
            cin>>r>>h;
            cout<<"\nVolume of the cylinder is:\t"<<vol(r,h)<<" cubic metre"<<endl;
            
        }
        cout<<"\nDo you want to continue[Y/N]:\n";
        cin>>ch;
    }
    while(ch=='Y');

    return 0;
}
