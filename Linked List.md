#### **[[Two Pointers]]**

### Structure of the Linked List

```
struct Node{
	int val; // The value ( val ) of the Node
	Node* next; // Pointer to the next Node of a Linked List
};
```

### Useful methods in a Linked List

-  Traversing through the list ( Two examples ):

This one we can use to check how many node's are there in the Linked List, or just traverse through the list.

```
	while(temp->next != nullptr){
		temp = temp->next;
	}
```

Or

```
	while(temp != nullptr){
		temp = temp->next;
	}
```

- **Using a dummy Node to help with edge cases**. Sometimes there are cases where we need to delete head, so it that situations we create a Node behind the head. Then we later create new Node to replace the head that is pointing to dummy->next so your previous head. If the head was removed we will return nullptr and not a error. Then we delete it so we can deallocate the memory from our program.
```
	Node* dummy = new Node(0, head); // Creates a dummy node behind the head
	...

	Node* newHead = dummy->next;
	delete dummy;
	return newHead;
```
### Implementing a Linked List

##### Creating a new Node on the end of a Linked List.
- Firstly we create a new Node with the value we want It to have. Then we check if the head is empty ( NULL ) if yes we insert node as a head. If no we create a temp variable that will traverse to the end of a Linked List and connect the new Node. 

```
class ListNode{
	public:
		void CreateNode(int value){
			Node* newNode = new Node(value, nullptr) // Create a new node
 			if(head == nullptr){ // Check if Head is empty
				head = newNode; // If yes head = newNode
			}else{
				Node* temp = head; // Create temp var to cycle through the list
				while(temp->next != nullptr){
					temp = temp->next
				}
				temp->next = newNode; // Put the node on the end
			}
		}

};
```

##### Creating a new Node in the front of a  Linked List

```
class ListNode{
	public:
		void CreateNode(int value){
			Node* newNode = new Node(value, nullptr) // Create a new node
 			if(head == nullptr){ // Check if Head is empty
				head = newNode; // If yes head = newNode
			}else{
				Node* temp = head->next; // Create temp var
				head = newNode;
				newNode->next = temp;
			}
		}
};
```

##### Deleting the n  Node in a Linked List

```
class ListNode{
	public:
		void deleteNode(Node* head){
			
		}
}
```

##### Reversing the Linked List

- We traverse through the Linked List and change the Node next pointer to point to the previous Node in a Linked List. The head will become NULL after reverse so that's why the first previous var is pointed to NULL. 

```
class ListNode{
public:
    Node* reverseList(Node* head) {
        Node* prev = nullptr;

        while (head != nullptr) {
            ListNode* next = head->next;
            head->next = node;
            node = head;
            head = temp;
        }

        return node;        
    }
};
```

##### Removing every element with value n

- First we check if the temp node is not a NULL. Then we check again but now we check if the next node is not equal to NULL and if it's the value we are looking to delete. Then we just change to pointing direction to the next of next Node. And in the end we delete the Node with the val and the dummy Node. 

- In this implementation we use the dummy Node so it's easier to manage the edge cases like:

  `Input = [] , val = 1 
  `Input = [7, 7, 7, 7] , val = 7` 
  
```
class Solution {
	public:
		ListNode* removeElements(ListNode* head, int val) {
			ListNode* dummy = new ListNode(0, head);
				ListNode* temp = dummy;
				while(temp != nullptr){
					while(temp->next != nullptr && temp->next->val == val){
						Node* nodeDelete = temp->next;
						temp->next = temp->next->next;
						delete nodeDelete;
					}
					temp = temp->next;
				}
			return dummy->next;
		}
};
```

##### 