#include <bits/stdc++.h>

/*************************************************************

    Following is the LinkedListNode class structure

    template <typename T>   
    class LinkedListNode
    {
        public:
        T data;
        LinkedListNode<T> *next;
        LinkedListNode<T> *random;
        LinkedListNode(T data)
        {
            this->data = data;
            this->next = NULL;
        }
    };

*************************************************************/
void insertAtTail(LinkedListNode<int> *&head,LinkedListNode<int> *&tail,int d){
         LinkedListNode<int> *newNode = new LinkedListNode<int>(d);
         if(head == NULL){
             head = newNode;
             tail = newNode;
             return ;
         }else{
             tail -> next = newNode;
             tail = newNode;
         }
        
    }
LinkedListNode<int> *cloneRandomList(LinkedListNode<int> *head)
{
    // Write your code here.
          LinkedListNode<int> *cloneHead = NULL;
          LinkedListNode<int> *cloneTail = NULL;
          LinkedListNode<int> *temp = head;
          while(temp != NULL) {
                insertAtTail(cloneHead,cloneTail,temp -> data);
                temp = temp -> next;
          }
          LinkedListNode<int> *originalNode = head;
          LinkedListNode<int> *cloneNode = cloneHead;
          while(originalNode != NULL && cloneNode != NULL){
                LinkedListNode<int> *next = originalNode -> next;
                originalNode -> next = cloneNode;
                originalNode = next;
                next = cloneNode -> next;
                cloneNode -> next = originalNode;
                cloneNode = next;
          }
          temp = head;
          while(temp != NULL){
                if(temp -> next != NULL){
                   temp -> next -> random = temp -> random ? temp -> random -> next : temp -> random;
                }
                temp = temp -> next -> next;
          }
          originalNode = head;
          cloneNode = cloneHead;
          while(originalNode != NULL && cloneNode != NULL){
                originalNode -> next = cloneNode -> next;
                originalNode = originalNode -> next;
                if(originalNode != NULL){
                   cloneNode -> next = originalNode -> next;
                }
                cloneNode = cloneNode -> next;
          }
          return cloneHead;
}
