# trees
#include <bits/stdc++.h>//inordered tress left root right
using namespace std;
struct Node{
    int data;
    Node* left;
    Node *right;
    
    Node(int x)
    {
        data=x;
        left=right=NULL;
    }
};
void ino(Node *root){
    if(root==NULL)return;
    ino(root->left);
    cout<<root->data;
    ino(root->right);
    cout<<root->data;
    
}

int main() {
    Node *root=new Node(1);
    root->left=new Node(2);
    root->right=new Node(3);
    root->left->left=new Node(4);
    root->left->right=new Node(5);
    root->right->left=new Node(6);

        
	
	return 0;
}
