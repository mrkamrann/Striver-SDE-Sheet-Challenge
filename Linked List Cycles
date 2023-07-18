#include<bits/stdc++.h>

Node *firstNode(Node *head)

{

    //    Write your code here.

    if(head == NULL || head->next == NULL){

        return NULL;

    }

    unordered_map<Node*,int> mp;

    Node* curr=head;

    while(curr->next != NULL){

        if(mp.count(curr) == 0){

            mp[curr]=1;

            curr=curr->next;

        }else{

            return curr;

        }

    }

    return NULL;

}
