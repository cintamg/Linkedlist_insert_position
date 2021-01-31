# Linkedlist_insert_position
To insert elements at a specified position.
SinglyLinkedListNode* insertNodeAtPosition(SinglyLinkedListNode* head, int data, int position) {
SinglyLinkedListNode* newnode=new SinglyLinkedListNode(data);
if(head==NULL)
return newnode;;
int i=1;
newnode->next=0;
SinglyLinkedListNode* temp=head;
if(position==0)
{
    newnode->next=head;
    head=newnode;
}
else {
while(position-1>0)
{
    temp=temp->next;
    position--;;
}
newnode->next=temp->next;
temp->next=newnode;
}
return head;
}
