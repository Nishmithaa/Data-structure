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
	
** C++ program to implememt single linked list. **
	
#include<iostream> <br>
#include<cstdlib> <br>
using namespace std; <br>
struct node <br>
{<br> 
 int info; <br>
 struct node *next; <br>
}*start; <br>
class single_llist<br> 
{ <br>
 public: <br>
 node* create_node(int);<br> 
 void insert_begin(); <br>
 void insert_last(); <br>
 void insert_pos(); <br>
 void delete_begin(); <br>
 void delete_last(); <br>
 void delete_pos(); <br>
 void update_begin(); <br>
 void update_last(); <br>
 void update_pos(); <br>
 void sort(); <br>
 void reverse(); <br>
 void search(); <br>
 void display(); <br>
 single_llist() <br>
 { <br>
 start = NULL; <br>
 } <br>
}; <br>
int main() <br>
{ <br>
 int choice; <br>
 single_llist sl,s2; <br>
 start = NULL;  <br>

 do  <br>
 {  <br> 
 cout<<"---------------------------------"<<endl;  <br>
 cout<<"Operations on singly linked list"<<endl;  <br>
 cout<<"---------------------------------"<<endl;  <br>
 cout<<"1.Insert at first"<<endl;  <br>
 cout<<"2.Insert at last"<<endl;  <br>
 cout<<"3.Insert at position"<<endl;  <br>
 cout<<"4.Delete at first"<<endl;  <br>
 cout<<"5.Delete at Last"<<endl;  <br>
 cout<<"6.Delete at position"<<endl;  <br>
 cout<<"7.Update at first"<<endl;  <br>
 cout<<"8.Update at last"<<endl;  <br>
 cout<<"9.Update at position"<<endl;  <br>
 cout<<"10.Ascending order"<<endl;  <br>
 cout<<"11.Descending order"<<endl;  <br>
 cout<<"12.Search"<<endl; <br> 
 cout<<"13.Display"<<endl;  <br> 
 cout<<"14.Exit "<<endl;  <br>
 cout<<"Enter your choice :";  <br>
 cin>>choice;  <br>
 switch(choice) <br> 
 {  <br>
 case 1: sl.insert_begin();  <br>
 sl.display();  <br>
 break;  <br>
 case 2: sl.insert_last();  <br>
 sl.display();  <br>
 break;  <br>
 case 3: sl.insert_pos();  <br>
 sl.display();  <br>
 break;  <br>
 case 4: s2.delete_begin();  <br>
 sl.display();  <br>
 break;  <br>
 case 5: s2.delete_last();  <br>
 sl.display();  <br>
 break;  <br>
 case 6: sl.delete_pos();  <br>
 sl.display();  <br>
 break;  <br>
 case 7: sl.update_begin();  <br>
 sl.display();  <br>
 break;  <br>
 case 8: sl.update_last(); 
 sl.display(); 
 break; 
 case 9: sl.update_pos(); 
 sl.display(); 
 break; 
 case 10:sl.sort(); 
 sl.display();  <br>
 break;  <br>
 case 11:sl.reverse();  <br>
 sl.display();  <br>
 break;  <br>
 case 12:sl.search();  <br>
 sl.display();  <br>
 break;  <br>
 case 13:sl.display();  <br>
 break;  <br>
 case 14:exit(0);  <br>
 break;  <br>
 default:cout<<"Wrong choice...???"<<endl;  <br>
 break;  <br>
 }  <br>
 }  <br>
 while(choice != 14);  <br>
}  <br>
node *single_llist::create_node(int value)  <br>
{  <br>
 struct node *temp, *s;  <br>
 temp = new(struct node);  <br>
 if (temp == NULL)  <br>
 {  <br>
 cout<<"Memory not allocated"<<endl;  <br>
 return 0;  <br>
 }  <br>
 else  <br>
 {  <br>
 temp->info = value;  <br>
 temp->next = NULL;  <br>
 return temp;  <br>
 }  <br>
}  <br>
void single_llist::insert_begin()  <br>
{  <br>
 int value;  <br>
 cout<<"Enter the value to be inserted : ";  <br>
 cin>>value;  <br>
 struct node *temp, *s;  <br>
 temp = create_node(value);  <br>
 if (start == NULL)  <br>
 {  <br>
 start = temp;  <br>
 start->next = NULL;  <br>
 cout<<temp->info<<" is inserted at first in the empty list"<<endl;  <br>
 }  <br>
 else  <br> 
 {  <br>
 s = start; <br> 
 start = temp;  <br>
 start->next = s;  <br>
 cout<<temp->info<<" is inserted at first"<<endl;  <br>
 } <br> 
}  <br>
void single_llist::insert_last()  <br>
{  <br>
 int value;  <br>
 cout<<"Enter the value to be inserted : ";  <br>
 cin>>value;  <br>
 struct node *temp, *s;  <br>
 temp = create_node(value);  <br>
 if (start == NULL)  <br>
 {  <br>
 start = temp;  <br>
 start->next = NULL;  <br>
 cout<<temp->info<<" is inserted at last in the empty list"<<endl;  <br>
 }  <br>
 else  <br>
 {  <br>
 s = start;  <br>
 while (s->next != NULL)  <br>
 {  <br>
 s = s->next;  <br>
 }  <br>
 temp->next = NULL;  <br>
 s->next = temp;  <br>
 cout<<temp->info<<" is inserted at last"<<endl;  <br>
 }  <br>
}  <br>
void single_llist::insert_pos()  <br>
{  <br>
 int value, pos, counter = 0, loc = 1; <br> 
 struct node *temp, *s, *ptr;  <br>
 s = start;  <br>
 while (s != NULL)  <br>
 {  <br>
 s = s->next;  <br>
 counter++;  <br> 
 }  <br>
 if (counter == 0) <br>{ <br>
	}  <br>
 else <br> 
 {  <br>
 cout<<"Enter the postion from "<<loc<<" to "<<counter+1<<" : "; <br> 
 cin>>pos;  <br>
 s = start;  <br>
 if(pos == 1)  <br>
 {  <br>
 cout<<"Enter the value to be inserted : ";  <br> <br>
 cin>>value;  <br>
 temp = create_node(value);  <br>
 start = temp;  <br>
 start->next = s;  <br>
 cout<<temp->info<<" is inserted at first"<<endl;  <br>
 }  <br>
 else if (pos > 1 && pos <= counter)  <br>
 {  <br>
 cout<<"Enter the value to be inserted : ";  <br>
 cin>>value;  <br>
 temp = create_node(value);  <br>
 for (int i = 1; i < pos; i++)  <br>
 {  <br>
 ptr = s;  <br>
 s = s->next;  <br>
 }  <br>
 ptr->next = temp;  <br>
 temp->next = s;  <br>
 cout<<temp->info<<" is inserted at position "<<pos<<endl;  <br>
 }  <br>
 else if (pos == counter+1)  <br>
 {  <br>
 cout<<"Enter the value to be inserted : ";  <br>
 cin>>value;  <br>
 temp = create_node(value);  <br>
 while (s->next != NULL)  <br>
 {  <br>
 s = s->next;  <br>
 }  <br>
 temp->next = NULL;  <br>
 s->next = temp;  <br>
 cout<<temp->info<<" is inserted at last"<<endl;  <br>
 }  <br>
 else  <br>
 {  <br>
 cout<<"Positon out of range...!!!"<<endl;  <br>
 }  <br>
 }  <br>
}  <br>
void single_llist::delete_begin()  <br>
{  <br>
 if (start == NULL) <br>
	{ <br>
	}  <br>
 else  <br>
 {  <br>
 struct node *s, *ptr;  <br>
 s = start;  <br>
 start = s->next;  <br>
 cout<<s->info<<" deleted from first"<<endl;  <br>
 free(s);  <br>
 }  <br>
}  <br>
void single_llist::delete_last()  <br>
{  <br>
 int i, counter = 0;  <br>
 struct node *s, *ptr;  <br>
 if (start == NULL){}  <br>
 else  <br>
 {  <br>
 s = start;  <br>
 while (s != NULL) <br> 
 {  <br>
 s = s->next;  <br>
 counter++;  <br>
 }  <br>
 s = start;  <br>
 if (counter == 1)  <br>
 {  <br>
 start = s->next; <br> 
 cout<<s->info<<" deleted from last"<<endl;  <br>
 free(s);  <br>
 }  <br>
 else  <br>
 {  <br>
 for (i = 1;i < counter;i++)  <br>
 {  <br>
 ptr = s;  <br>
 s = s->next;  <br>
 }  <br>
 ptr->next = s->next;  <br>
 cout<<s->info<<" deleted from last"<<endl;  <br>
 free(s); <br> 
 }  <br>
 }  <br>
}  <br>
void single_llist::delete_pos()  <br>
{  <br>
 int pos, i, counter = 0, loc = 1;  <br>
 struct node *s, *ptr;  <br>
 s = start;  <br>
 while (s != NULL)  <br>
 {  <br>
 s = s->next; <br> 
 counter++;  <br>
 }  <br>
 if (counter == 0){}  <br>
 else  <br>
 {  <br>
 if (counter == 1)  <br>
 { <br> 
 cout<<"Enter the postion [ SAY "<<loc<<" ] : ";  <br>
 cin>>pos;  <br>
 s = start;  <br>
 if (pos == 1)  <br>
 {  <br>
 start = s->next;  <br>
 cout<<s->info<<" deleted from first"<<endl; <br> 
 free(s);  <br>
 }  <br>
 else  <br>
 cout<<"Position out of range...!!!"<<endl;  <br>
 }  <br>
 else  <br>
 {  <br>
 cout<<"Enter the postion from "<<loc<<" to "<<counter<<" : ";  <br>
 cin>>pos;  <br>
 s = start;  <br> <br>
 if (pos == 1)  <br>
 {  <br>
 start = s->next;  <br>
 cout<<s->info<<" deleted from first"<<endl;  <br>
 free(s);  <br>
 }  <br>
 else if (pos > 1 && pos <= counter)  <br>
 { <br> 
 for (i = 1;i < pos;i++)  <br>
 {  <br>
 ptr = s;  <br>
 s = s->next;  <br>
 }  <br>
 ptr->next = s->next;  <br>
 if(pos == counter)  <br>
 {cout<<s->info<<" deleted from last"<<endl; <br> 
 free(s);}  <br>
 else  <br>
 {cout<<s->info<<" deleted from postion "<<pos<<endl; <br> 
 free(s);}  <br>
 }  <br>
 else  <br>
 cout<<"Position out of range...!!!"<<endl;  <br>
 }  <br>
 }  <br>
}  <br>
void single_llist::update_begin()  <br>
{  <br>
 int value, pos=1, i,counter = 0;  <br>
 struct node *s, *ptr;  <br>
 s = start;  <br>
 while (s != NULL)  <br>
 {  <br>
 s = s->next;  <br>
 counter++;  <br>
 }  <br>
 if (counter == 0){}  <br>
 else if (pos == 1) <br> 
 {  <br>
 cout<<"Enter the new node : ";  <br>
 cin>>value;  <br>
 start->info = value;  <br>
 cout<<"Node updated at first position : "<<pos<<" = "<<start->info<<endl;  <br>
 }  <br>
}  <br>
void single_llist::update_last()  <br>
{  <br>
 int value, pos, i,counter = 0;  <br>
 struct node *s, *ptr; <br> 
 s = start;  <br>
 while (s != NULL)  <br>
 {  <br>
 s = s->next;  <br>
 counter++;  <br>
 }  <br>
 s=start;  <br>
 if (counter == 0){}  <br>
 else  <br>
 {  <br>
 cout<<"Enter the new node : ";  <br>
 cin>>value;  <br>
 for (i = 1; i < counter ; i++)  <br>
 {  <br>
 s = s->next;  <br>
 }  <br>
 s->info = value;  <br>
 cout<<"Node updated at last position : "<<counter<<" = "<<s->info<<endl;  <br>
 }  <br>
}  <br>
void single_llist::update_pos()  <br>
{  <br>
 int value, pos, i,counter = 0, loc = 1;  <br>
 struct node *s, *ptr;  <br>
 s = start;  <br>
 while (s != NULL)  <br>
  {  <br>
 s = s->next;  <br>
 counter++;  <br>
 }  <br>
 if (counter == 0){}  <br>
 else  <br>
 {  <br>
 if (counter == 1)  <br>
 {  <br>
 cout<<"Enter the postion [ SAY "<<loc<<" ] : ";  <br>
 cin>>pos;  <br>
 s = start;  <br>
 if (pos == 1)  <br>
 {  <br>
 cout<<"Enter the new node : ";  <br>
 cin>>value;  <br>
 start->info = value;  <br>
 cout<<"Node updated at position : "<<pos<<" = "<<start->info<<endl;  <br>
 }  <br>
 else  <br>
 cout<<"Position out of range...!!!"<<endl;  <br>
 }  <br>
 else  <br>
 {  <br> 
 cout<<"Enter the postion from "<<loc<<" to "<<counter<<" : ";  <br> 
 cin>>pos;  <br>
 s = start;  <br>
 if (pos == 1)  <br>
 {  <br>
 cout<<"Enter the new node : ";  <br>
 cin>>value;  <br>
 start->info = value;  <br>
 cout<<"Node updated at position : "<<pos<<" = "<<start->info<<endl;  <br>
 }  <br>
 else if (pos > 1 && pos <= counter)  <br>
 {  <br>
 cout<<"Enter the new node : ";  <br>
 cin>>value;  <br>
 for (i = 1; i < pos ; i++)  <br>
 {  <br>
 s = s->next;  <br>
 }  <br>
 s->info = value;  <br>
 cout<<"Node updated at position : "<<pos<<" = "<<s->info<<endl;  <br>
 }  <br> 
 else <br>
 cout<<"Position out of range...!!!"<<endl;  <br>
 }  <br>
 }  <br>
}  <br>
void single_llist::sort()  <br>
{  <br> 
 struct node *ptr, *s;  <br>
 int value;  <br>
 if (start == NULL){}  <br>
 else  <br>
 {  <br>
 ptr = start;  <br> 
 while (ptr != NULL)  <br>
 {  <br>
 for (s =  ptr->next;s !=NULL;s = s->next)  <br>
 {  <br>
 if (ptr->info > s->info)  <br>
 {  <br>
 value = ptr->info;  <br>
 ptr->info = s->info;  <br>
 s->info = value;  <br>
 }  <br>
 }  <br>
 ptr = ptr->next;  <br>
 }  <br>
 }  <br>
}  <br>
void single_llist::reverse()  <br>
{  <br>
 struct node *ptr, *s;  <br>
 int value;  <br>
 if (start == NULL){}  <br>
 else  <br>
 {  <br>
 ptr = start;  <br>
 while (ptr != NULL)  <br>
 {  <br>
 for (s = ptr->next;s !=NULL;s = s->next)  <br>
 {  <br>
 if (ptr->info < s->info)  <br>
 {  <br>
 value = ptr->info;  <br>
 ptr->info = s->info;  <br>
 s->info = value;  <br>
 }  <br>
 }  <br>
 ptr = ptr->next;  <br>
 }  <br> 
} <br>
}  <br>
void single_llist::search()  <br>
{  <br>
 int value, loc = 0, pos = 0, counter = 0;  <br>
 struct node *s;  <br>
 s = start;  <br>
 while (s != NULL)  <br>
 {  <br>
 s = s->next;  <br>
 counter++;  <br>
 }  <br>
 if (start == NULL){}  <br>
 else  <br>
 {  <br>
 cout<<"Enter the value to be searched : ";  <br>
 struct node *s;  <br>
 s = start;  <br>
 while (s != NULL)  <br>
 { <br> 
 pos++;  <br>
 if (s->info == value)  <br>
 {  <br>
 loc++;  <br>
 if(loc == 1) <br> <br> 
 cout<<"Element "<<value<<" is found at position "<<pos;  <br>
 else if(loc <= counter)  <br>
 cout<<" , "<<pos;  <br>
 }  <br>
 s = s->next;  <br>
 }  <br>
 cout<<endl;  <br>
 if (loc == 0)  <br>
 cout<<"Element "<<value<<" not found in the list"<<endl;  <br>
 }  <br>
}  <br>
void single_llist::display()  <br>
{  <br>
 struct node *temp;  <br>
 if (start == NULL)  <br>
 cout<<"Linked list is empty...!!!"<<endl;  <br>
 else  <br>
 {  <br>
 cout<<"Linked list contains : ";  <br>
 temp = start;  <br>
 while (temp != NULL)  <br>
 {  <br> 
 cout<<temp->info<<" ";  <br>
 temp = temp->next;  <br>
 }  <br>
 cout<<endl;  <br>
 }  <br>
} <br>
	**Output** <br>
![image](https://user-images.githubusercontent.com/98141713/152734170-ebb17dbb-28e2-4bb6-a7ab-b328cd1d49b8.png) <br>
![image](https://user-images.githubusercontent.com/98141713/152734247-156bdac7-f97b-439a-99bc-4c3904f5ebab.png) <br>
![image](https://user-images.githubusercontent.com/98141713/152734278-13d436f6-805a-4ba8-b6b9-18705374d335.png) <br>
![image](https://user-images.githubusercontent.com/98141713/152734301-1dbf6628-5c8b-447e-89d2-2aea1d7c4c39.png) <br>
![image](https://user-images.githubusercontent.com/98141713/152734349-8d5a7c40-b778-406f-b025-cb2ef9a011de.png) <br>
![image](https://user-images.githubusercontent.com/98141713/152734370-f180ad06-c41e-484e-a529-0cdcf5052365.png) <br>
![image](https://user-images.githubusercontent.com/98141713/152734400-c6a97444-5c1c-4aeb-b4c4-3185da46ab42.png) <br>
![image](https://user-images.githubusercontent.com/98141713/152734440-2b215f62-ad47-4b1c-9714-67d528b5f7d1.png) <br>
	
	
	
	
	
#include<iostream>
#include<cstdlib>
using namespace std;
struct node
{
int info;
struct node *next;
}*start;

class single_llist
{
public:
node* create_node(int);
void insert_begin();
void delete_begin();
void display();
single_llist()
{
start=NULL;
}
};
int main()
{
int choice;
single_llist sl,s2;
start = NULL;

do
{
cout<<"___________"<<endl;
cout<<"Operations on singly linked list"<<endl;
cout<<"___________"<<endl;
cout<<"1.Insert at first"<<endl;
cout<<"2.Delete at first"<<endl;
cout<<"3.Display"<<endl;
cout<<"4.Exit "<<endl;

cout<<"Enter your choice :";
cin>>choice;
switch(choice)
{
case 1: sl.insert_begin();
sl.display();
break;

case 2: s2.delete_begin();
sl.display();
break;
case 3:sl.display();
break;
case 4:exit(0);
break;
default:cout<<"Wrong choice...???"<<endl;
break;
}
}


while(choice != 4);
}
node *single_llist::create_node(int value)
{
struct node *temp, *s;
temp = new(struct node);
if (temp == NULL)
{
cout<<"Memory not allocated"<<endl;
return 0;
}
else
{
temp->info = value;
temp->next = NULL;
return temp;
}
}
void single_llist::insert_begin()
{
int value;
cout<<"Enter the value to be inserted : ";
cin>>value;
struct node *temp, *s;
temp = create_node(value);
if (start == NULL)
{
start = temp;
start->next = NULL;
cout<<temp->info<<" is inserted at first in the empty list"<<endl;
}
else
{
s = start;
start = temp;
start->next = s;
cout<<temp->info<<" is inserted at first"<<endl;
}
}
void single_llist::delete_begin()
{
if (start == NULL)
{
}
else
{
struct node *s, *ptr;
s = start;
start = s->next;
cout<<s->info<<" deleted from first"<<endl;
free(s);
}
}

void single_llist::display()
{
struct node *temp;
if (start == NULL)
cout<<"Linked list is empty...!!!"<<endl;
else
{
cout<<"Linked list contains : ";
temp = start;
while (temp != NULL)
{
cout<<temp->info<<" ";
temp = temp->next;
}
cout<<endl;
}
}

	
#include<iostream><br>
using namespace std;<br>
struct Node <br>
{<br>
	int value;<br>
	struct Node *next;<br>
};<br>
struct Node* head=NULL;<br>
struct Node* sHead=NULL;<br>
struct Node* temp=NULL;<br>
void insert(int new_data)<br>
{<br>
	struct Node* new_node = new Node();<br>
	new_node->value = new_data;<br>
	new_node->next = head;<br>
	head = new_node;<br>
}
int n;<br>
int ele;<br>
int splitlndex;<br>
int main()<br>
{<br>
	int i;
	cout<<"Enter number of elements you want in the list\t";<br>
	cin>>n;<br>
	cout<<"Enter elements:"<<endl;<br>
	for(i=0;i<n;i++)<br>
	{<br>
		cin>>ele;<br>
		insert(ele);<br>
	}<br>
	cout<<"\nList of elements:"<<endl;<br>
	Node *t;<br>
	t=head;<br>
	while(t!=NULL)<br>
	{<br>
		cout<<t->value<<"\t";<br>
		t=t->next;<br>
	}<br>
	cout<<"\n\nEnter the element you want the list to split";<br>
	cin>>splitlndex;<br>
	while(splitlndex<0||splitlndex>n-1)<br>
	{<br>
		cout<<"Invalid position.Try again."<<endl;<br>
		cin>>splitlndex;<br>
	}<br>
	temp = head;<br>
	for(i=0;i<splitlndex;i++)<br>
	{<br>
		if(i==splitlndex-1)<br>
		{<br>
			Node *tN;<br>
			tN=temp->next;<br>
			sHead=tN;<br>
			temp->next=NULL;<br>
			break;<br>
		}<br>
		temp=temp->next;<br>
	}<br>
	temp=head;<br>
	if(temp==NULL)<br>
	{<br>
		cout<<"\n First list is empty"<<endl;<br>
	}<br>
	else<br>
	{<br>
		cout<<"\n\nFirst list element"<<endl;<br>
		while(temp!=NULL)<br>
		{<br>
			cout<<temp->value<<"\t";<br>
			temp=temp->next;<br>
		}<br>
	}<br>
	temp=sHead;<br>
	if(temp==NULL)<br>
	{<br>
		cout<<"\nSecond list is empty"<<endl;<br>
	}<br>
	else<br>
	{<br>
		cout<<"\n\nSecond list elements"<<endl;<br>
		while(temp!=NULL)<br>
		{<br>
			cout<<temp->value<<"\t";<br>
			temp=temp->next;<br>
		}<br>
	}<br>
	return 0;<br>
}<br>
	
**Output**<br>
![image](https://user-images.githubusercontent.com/98141713/155066730-8bbf39f8-6fbe-4cfc-9d69-50b691ca0196.png)<br>
	
	
**Create a WAP to store K keys into an array or size To the location competing a hash function. For key %n where key%n where m>n to handle  collision use linear** 	
#include<iostream><br>
#include<limits.h><br>
using namespace std;<br>
void Insert(int ary[],int hFn, int Size)<br>
{<br>
int element,pos,n=0;<br>
cout<<"Enter key element to insert\n";<br>
cin>>element;<br>

pos = element%hFn; <br>

while(ary[pos]!= INT_MIN)<br>
	{  <br>
if(ary[pos]== INT_MAX)<br>
            break;<br>
pos = (pos+1)%hFn;<br>
n++;<br>

if(n==Size)<br>
            break;<br>     
}<br>

if(n==Size)<br>
        cout<<"Hash table was full of elements\nNo Place to insert this element\n\n";<br>
else<br>
        ary[pos] = element;  <br><br>  
}<br>

void display(int ary[],int Size)<br>
	{<br>
int i;<br>
 
cout<<"Index\tValue\n";<br>
for(i=0;i<Size;i++)<br>
        cout<<i<<"\t"<<ary[i]<<"\n";<br>
}<br>


int main()<br>
{<br>
int Size,hFn,i,choice;<br>
cout<<"Enter size of hash table\n";<br>
cin>>Size;<br>
 hFn=Size;<br>
int ary[Size];<br>
for(i=0;i<Size;i++)<br>
        ary[i]=INT_MIN; <br>
        
do<br>
{<br>
	
cout<<"Enter your choice\n";<br>
cout<<" 1-> Insert\n 2-> Display\n 0-> Exit\n";<br>
cin>>choice;<br>
<br>
switch(choice)<br>
{<br>
case 1:<br>
Insert(ary,hFn,Size);<br>
break;<br>

case 2:<br>
display(ary,Size);<br>
break;<br>

default:<br>
cout<<"Enter correct choice\n";<br>
break;<br>
}<br>

}<br>
while(choice);<br>
return 0;<br>
}<br>

**Output**<br>
![image](https://user-images.githubusercontent.com/98141713/155929805-358015f9-fad7-445a-953f-6b6ba143fba8.png)<br>
![image](https://user-images.githubusercontent.com/98141713/155929822-59c90b11-fd0d-46e7-b24e-ec25dbb7568e.png)<br>
	

**Doubly linked list**<br>
	#include <iostream><br>
using namespace std;<br>
struct Node<br>
	{<br>
   int data;<br>
   struct Node *prev;<br>
   struct Node *next;<br>
};<br>
struct Node* head = NULL;<br>
void insert(int newdata) <br>{<br>
   struct Node* newnode = (struct Node*) malloc(sizeof(struct Node));<br>
   newnode->data = newdata;<br>
   newnode->prev = NULL;<br>
   newnode->next = head;<br><br>
   if(head != NULL)<br>
   head->prev = newnode ;<br>
   head = newnode;<br>
}<br>
void display()<br> {<br>
   struct Node* ptr;<br>
   ptr = head;<br>
   while(ptr != NULL)<br> {<br>
      cout<< ptr->data <<" ";<br>
      ptr = ptr->next;<br>
   }<br>
}<br>
int main()<br>
	{<br>
   insert(3);<br>
   insert(1);<br>
   insert(7);<br>
   insert(2);<br>
   insert(9);<br>
   cout<<"The doubly linked list is: ";<br>
   display();<br>
   return 0;<br>
}<br>
	
**Output**<br>
![image](https://user-images.githubusercontent.com/98141713/155933730-3b9e1f96-d429-472e-b967-87f48fc37935.png)<br>
	
**Heap**<br>
#include <iostream><br>
using namespace std;<br>
void MaxHeapify<br>
 (int a[], int i, int n)<br>
{<br>
	int j, temp;<br>
	temp = a[i];<br>
	j = 2*i;<br>
	while (j <= n)<br>
	{<br>
		if (j < n && a[j+1] > a[j])<br>
		j = j+1;<br>
		if (temp > a[j])<br>
			break;<br>
		else if (temp <= a[j])<br>
		{<br>
			a[j/2] = a[j];<br>
			j = 2*j;<br>
		}<br>
	}<br>
	a[j/2] = temp;<br>
	return;<br>
}<br>
void HeapSort(int a[], int n)<br>
{<br>
	int i, temp;<br>
	for (i = n; i >= 2; i--)<br>
	{<br>
		temp = a[i];<br>
		a[i] = a[1];<br>
		a[1] = temp;<br>
		MaxHeapify(a, 1, i - 1);<br>
	}<br>
}<br>
void Build_MaxHeap(int a[], int n)<br>
{<br>
	int i;<br>
	for(i = n/2; i >= 1; i--)<br>
		MaxHeapify(a, i, n);<br>
}<br>
int main()<br>
{<br>
int n, i,arr[100];<br>
	cout<<"\nEnter the number of data element to be sorted: ";<br>
	cin>>n;<br>
	n++;<br>
	for(i=1;i<n;i++)<br>
	 {<br>
	 cout<<"Enter element"<<i<<":";<br>
	 cin>>arr[i];<br>
	 }<br>
	Build_MaxHeap(arr, n-1);<br>
	HeapSort(arr, n-1);<br>
	cout<<"\nSorted Data ";<br>
	for (i = 1; i < n; i++)<br>
		cout<<" "<<arr[i];<br>
	return 0;<br>
}<br>
				  
 **Output**<br>
![image](https://user-images.githubusercontent.com/98141713/155941394-23f9ad04-1050-4d54-9629-b56b772e7ba9.png)<br>


**Max heap and min heap**
#include <iostream>
#include <conio.h>
using namespace std;
void max_heapify(int *a, int i, int n)
{
    int j, temp;
    temp = a[i];
    j = 2 * i;
    while (j <= n)
    {
        if (j < n && a[j+1] > a[j])
            j = j + 1;
        if (temp > a[j])
            break;
        else if (temp <= a[j])
        {
            a[j / 2] = a[j];
            j = 2 * j;
        }
    }
    a[j/2] = temp;
    return;
}
void build_maxheap(int *a,int n)
{
    int i;
    for(i = n/2; i >= 1; i--)
    {
        max_heapify(a,i,n);
    }
}

void min_heapify(int *a,int i,int n)
{
    int j, temp;
    temp = a[i];
    j = 2 * i;
    while (j <= n)
    {
        if (j < n && a[j+1] < a[j])
            j = j + 1;
        if (temp < a[j])
            break;
        else if (temp >= a[j])
        {
            a[j/2] = a[j];
            j = 2 * j;
        }
    }
    a[j/2] = temp;
    return;
}
void build_minheap(int *a, int n)
{
    int i;
    for(i = n/2; i >= 1; i--)
    {
        min_heapify(a,i,n);
    }
}


int main()
{
	 int n, i, x;
    cout<<"enter no of elements of array\n";
    cin>>n;
     int a[20];
    for (i = 1; i <= n; i++)
    {
        cout<<"enter element"<<(i)<<endl;
        cin>>a[i];
    }
    
     build_maxheap(a,n);
    cout<<"Max Heap\n";
    for (i = 1; i <= n; i++)
    {
        cout<<a[i]<<endl;
    }
    
     build_minheap(a, n);
    cout<<"Min Heap\n";
    for (i = 1; i <= n; i++)
    {
        cout<<a[i]<<endl;
    }
    getch();
}


	
	
#include <iostream>

void meargeArrays(int a[],int low,int mid,int high)
{
    int i=low,j=mid+1,index=low,temp[100],k;
    
    while(i<==mid && j<==high)
    {
        if(a[i]<a[j])
        {
            temp[index]=a[j];
            j++
            
        }
        index++;
    }
    if(i>mid)
    {
        while(j<=high)
        {
            temp[index]=a[i];
            i++;
            index++;
        }
    }
    else
    while(i<=mid)
    {
        temp[index]=a[i];
        i++;
        index++;
    }
    }
    for(k=low;k<index;k++)
    {
        a[k]=temp[k];
    }
   }
   void mergesort(int a[],int low,int high)
   {
       if(low<high)
       {
           int middle = (low + high) / 2; 
           mergesort(a, low, middle);
            mergesort(a, middle + 1, high); 

          mergeofarrays(a, low, middle, high); 
       }
   }
        int main() {
  int n = 7;
  int a[100] = {54,34,23,10,98,2,3};
  mergesort(a, 0, 6);
  for (int i = 0; i < n; i++) {
    cout << a[i] << " ";
  }
}                                                                            
}
		    
**Hash table**<br><br>
#include<iostream><br>
#include<limits.h> <br>
using namespace std;<br>
void Insert(int ary[],int hFn, int Size)<br>{ <br>
 int element,pos,n=0; <br>
cout<<"Enter key element to insert\n";<br>
cin>>element;<br>
pos = element%hFn; <br>
while(ary[pos]!= INT_MIN)<br> { <br>
if(ary[pos]== INT_MAX)<br>
 break; <br>
pos = (pos+1)%hFn; <br>
n++;<br>
if(n==Size)<br>
 break; <br>
} <br>
if(n==Size)<br>
 cout<<"Hash table was full of elements\nNo Place to insert this element\n\n"; <br>
else<br>
 ary[pos] = element; <br>
} <br>
void display(int ary[],int Size)<br>{ <br>
int i;<br>
 
cout<<"Index\tValue\n";<br>
for(i=0;i<Size;i++)<br>
 cout<<i<<"\t"<<ary[i]<<"\n"; <br>
} <br>
int main()<br>{<br>
int Size,hFn,i,choice; <br>
cout<<"Enter size of hash table\n";<br>
cin>>Size;<br>
hFn=Size;<br>
int ary[Size];<br>
for(i=0;i<Size;i++)<br>
 ary[i]=INT_MIN; <br>
do<br>{ <br>
cout<<"Enter your choice\n";<br> 
cout<<" 1-> Insert\n 2-> Display\n 0-> Exit\n";<br>
cin>>choice;<br>
switch(choice)<br>{<br>
case 1:<br>
Insert(ary,hFn,Size);<br>
break; <br>
case 2:<br>
display(ary,Size);<br><br>
break; <br>
default:<br>
cout<<"Enter correct choice\n";<br>
break; <br>
} <br>
}<br>while(choice);<br>
return 0;<br>
}<br>
	**Output**<br>
![image](https://user-images.githubusercontent.com/98141713/163770173-dfefb79f-dbd3-4473-9a3a-3e73dfd86ff4.png)<br>
	
	**N queens**
	#include <bits/stdc++.h>
#define N 4
using namespace std;

void printSolution(int board[N][N])
{
	for (int i = 0; i < N; i++) {
		for (int j = 0; j < N; j++)
			cout << " " << board[i][j] << " ";
	}
}
bool isSafe(int board[N][N], int row, int col)
{
	int i, j;
	for (i = 0; i < col; i++)
		if (board[row][i])
			return false;
	for (i = row, j = col; i >= 0 && j >= 0; i--, j--)
		if (board[i][j])
			return false;
	for (i = row, j = col; j >= 0 && i < N; i++, j--)
		if (board[i][j])
			return false;

	return true;
}

bool solveNQUtil(int board[N][N], int col)
{
	if (col >= N)
		return true;

	for (int i = 0; i < N; i++) {

		if (isSafe(board, i, col)) {
			board[i][col] = 1;
			if (solveNQUtil(board, col + 1))
				return true;

			board[i][col] = 0;
		}
	}

	return false;
}

bool solveNQ()
{
	int board[N][N] = { { 0, 0, 0, 0 },
						{ 0, 0, 0, 0 },
						{ 0, 0, 0, 0 },
						{ 0, 0, 0, 0 } };

	if (solveNQUtil(board, 0) == false) {
		cout << "Solution does not exist";
		return false;
	}

	printSolution(board);
	return true;
}

int main()
{
	solveNQ();
	return 0;
}
			**Output**
			![image](https://user-images.githubusercontent.com/98141713/163773240-e8b31945-dc7c-4cc2-baa0-e729eecc49bc.png)

