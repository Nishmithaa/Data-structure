# Data-structure
# List of Programmes
 **1.adding 10 array elements using for ,while,do while**
#include <iostream><br>
 
using namespace std;<br>
 
int main()<br>
{<br>
    int i,arr[10],sum1=0,sum2=0,sum3=0,n; <br>
     char ch;<br>
    do<br>
	{<br>
 	 cout<<"ENTER CHOICE\n"<<"1.For\n"<<"2.While\n"<<"3.Do While\n";<br>
    cout<<"Make a choice: ";<br>
    cin>>n;<br>
     
    switch(n)<br>
    {<br>
        case 1:<br>
        	cout<<"Enter 10 elements:\n";<br> 
    for(i=0;i<10;++i)<br>
      cin>>arr[i];<br> 
	  for(i=0;i<10;++i)<br> 
        sum1=sum1+arr[i];<br> 
    
    cout<<"Sum of numbers is:"<<sum1;<br> 
     break;<br>
         
        case 2 : <br>
        	cout<<"Enter 10 elements:\n"; <br>
        i=0;<br>
        while(i<10)<br>
        {<br>
        	cin>>arr[i];<br>
        	i++;<br>
		}<br>
		i=0;<br>
		while(i<10)<br> 
		{<br>
			sum2=sum2+arr[i];<br>
			i++; <br>
		}<br>
        cout<<"Sum of numbers is:"<<sum2; <br>
            
            break;<br>
         
        case 3 : <br>
        cout<<"Enter 10 elements:\n";<br> 
        i=0;<br>
        do<br>
	{<br>
        		cin>>arr[i];<br>
        		i++;<br>
		}<br>
	while(i<10);<br>
        
         i=0;<br>
        do<br>
	{<br>
        		sum3=sum3+arr[i];<br>
        		i++;<br>
		}<br>
	
	while(i<10);<br>
		 cout<<"Sum of numbers is:"<<sum3; <br>
            break;<br>
             
        default : <br>
            cout<<"Invalid Choice\n";<br>
    }<br>
     
    cout<<"\nDo you want to continue ? : ";<br>
    cin>>ch;<br>
 
    }<br>
	while(ch=='Y'||ch=='y');v
     
    return 0;<br>
}<br>
<br>**output**<br>
![image](https://user-images.githubusercontent.com/98141713/150930917-2be1cf36-9f49-4bf7-9b9a-5c738e38e452.png)

	
**2.Array using stack**
	
	#include <iostream><br>
using namespace std;<br>
int stack[100], n=100, top=-1;<br>
void push(int val)<br>
	{<br>
   if(top>=n-1)<br>
   cout<<"Stack Overflow"<<endl;<br>
   else <br>
	{<br>
      top++;v
      stack[top]=val;<br>
   }<br>
}v
void pop()<br>
	{<br>
   if(top<=-1)<br>
   cout<<"Stack Underflow"<<endl;<br>
   else <br>
	{<br>
      cout<<"The popped element is "<< stack[top] <<endl;<br>
      top--;<br>
   }<br>
}<br>
void display()<br>
	{<br>
   if(top>=0) <br>
	{<br>
      cout<<"Stack elements are:";<br>
      for(int i=top; i>=0; i--)<br>
      cout<<stack[i]<<" ";<br>
      cout<<endl;<br>
   }<br>
	else<br>
   cout<<"Stack is empty";<br>
}<br>
int main()<br>
	{<br>
   int ch, val;<br>
   cout<<"1) Push in stack"<<endl;<br>
   cout<<"2) Pop from stack"<<endl;<br>
   cout<<"3) Display stack"<<endl;<br>
   cout<<"4) Exit"<<endl;<br>
   do <br>
	{<br>
      cout<<"Enter choice: "<<endl;<br>
      cin>>ch;<br>
      switch(ch)<br>
	{<br>
         case 1: <br>
	{<br>
            cout<<"Enter value to be pushed:"<<endl;<br>
            cin>>val;<br>
            push(val);<br>
            break;<br>
         }<br>
         case 2:<br>
	{<br>
            pop();<br>
            break;<br>
         }<br>
         case 3:<br>
	{<br>
            display();<br>
            break;<br>
         }<br>
         case 4:<br>
	{<br>
            cout<<"Exit"<<endl;<br>
            break;<br>
         }<br>
         default:<br>
	{<br>
            cout<<"Invalid Choice"<<endl;<br>
         }<br>
      }<br>
   }<br>
	while(ch!=4);<br>
   return 0;<br>
}<br>
<br>**output**<br>
![image](https://user-images.githubusercontent.com/98141713/150932229-97edb7b6-b4f8-4b40-ace3-65cde6f8e287.png)
	
