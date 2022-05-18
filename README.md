#include <iostream>
using namespace std;
struct node
{
    int data;
    node *left;
    node *right;
    node(int x)
    {
        data=x;
        left=right=NULL;
        
    }
};
void preorder(node *root)
{
    if(root!=NULL)
    {
       // cout<<(root->data)<<" ";//preorder
        preorder(root->left);
     //   cout<<(root->data)<<" ";//inoder
        
        preorder(root->right);
       // cout<<(root->data)<<" ";//postorder
        
    }
    
}


int main() {
	// your code goes here
	node *root=new node(10);
	root->left=new node(20);
	root->right=new node(30);
	root->left->left=new node(40);
	preorder(root);
	return 0;
}
