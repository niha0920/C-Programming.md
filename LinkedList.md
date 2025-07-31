## Program that delete the middle node of a singly linked list
```C
#include<stdio.h>
#include<stdlib.h>
struct Node {
    int data;
    struct Node *next;
};
struct Node *createNode(int data)
{
    struct Node *newNode = (struct Node*)malloc(sizeof(struct Node));
    newNode->data = data;
    newNode->next = NULL;
    return newNode;
}
void deleteMiddle(struct Node **head)
{
    if(*head == NULL || (*head)->next == NULL)
    {
        free(*head);
        *head == NULL;
        return;
    }
    struct Node *trav = *head, *ftrav = *head, *prevtrav = NULL;
    while(ftrav != NULL && ftrav->next != NULL)
    {
        ftrav = ftrav->next->next;
        prevtrav = trav;
        trav = trav->next;
    }
    prevtrav->next = trav->next;
    free(trav);
}
void printList(struct Node *head)
{
    while(head != NULL)
    {
        printf("%d->", head->data);
        head = head->next;
    }
    printf("NULL\n");
}
int main()
{
    struct Node *head = createNode(1);
    head->next = createNode(2);
    head->next->next = createNode(3);
    head->next->next->next = createNode(4);
    head->next->next->next->next = createNode(5);
    //head->next->next->next->next->next = createNode(6);   //Output : After deleting middle node : 1->2->3->5->6->NULL 
    printf("Original list : ");
    printList(head);
    deleteMiddle(&head);
    printf("After deleting middle node : ");
    printList(head);
}
```
