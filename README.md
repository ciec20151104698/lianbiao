# lianbiao
#include<iostream>
struct Node
{
  char name[50];
  int age;
  struct Node *next;
 }
 
int main()
{
  struct Node *head,*p,*q;
  head=new Node;
  scanf("%s",head->name);
  scanf("%d",&head->age);
  int i;
  head->next=0;
  q=head;
  for(i=0;i<4;i++)
  {
    p=new Node;
    scanf("%s",p->name);
    scanf("%d",&p->age);
    p->next=0;
    q->next=p;
    q=p;
   }
   p=head;
   while(p)
   {
    printf("%s %d\n",p->name,p->age);
    p=p->next;
   }
    return 0;
  }
