# data-structure-
#include <stdio.h>
#include <stdlib.h>
struct node
{
    int dt;
    struct node* link;
};
struct node* top=NULL;
void push()
{
    struct node* temp;
    temp=(struct node*)malloc(sizeof(struct node));
    printf("\nenter your data : ");
    scanf("\n%d",&temp.dt);
    temp->link=top;
    top=temp;
}
void pop()
{
    struct node* temp;
    if(top==NULL)
    {printf("\n stack underflow");}
    else
    {
        temp=top;
       printf("    \npoped element : %d", temp.dt);
       top=top->link;
       temp->link=NULL;
       free(temp);
    }
}
void display()
{
     struct node* temp;
    if(top==NULL)
    {printf("\n stack underflow");}
    else
    {
        temp=top;
        printf("\n Display : ");
        while(temp!= NULL)
        {
            printf(" %d ",temp.dt);
            temp=temp->link;
        }
    }
}
int main()
{
 push();push();push();push();push();display();printf("\n");pop();pop();display();
}
