### Structure of Stack and it's definition

- Stack is a data structure that is only accessible from the **Top**. The most popular functions it provide are: 
	- [[#Push Function]] - Puts the element on **Top**.
	- Pop - Removes the element at **Top**.
	- IsEmpty - Check if the Stack is empty, return boolean.
	- Top - Returns  the value at **Top**.


![[Stack.excalidraw|100%]]

### Implementation for Linked List Stack

#### Declaration of the Stack for Linked List

- The structure for the Linked List. It have: 
	- Declaration of the integer value.
	- Declaration of a pointer to the next Node.
	- Constructors:
		- `ListNode()` - Assign Node with value 0 and a pointer to NULL.
		- `ListNode(int value)` - Assign Node with value declared in the parentheses and a pointer to NULL.
		- `ListNode(int value, ListNode *next)` - Assign the value declared in the parentheses and a pointer to the next pointer. 

```
struct ListNode{
    int val;
    ListNode* next;
    ListNode() : val(0), next(nullptr) {}
    ListNode(int value) : val(value), next(nullptr) {}     
    ListNode(int value, ListNode *next) : val(value), next(next) {}
};
```

- Adding head to the class (Pointer to the First Node in the Linked List)

```
class Stack{
	private:
		ListNode* head;
	public:
		Stack(){
			head = nullptr;
		}
};
```
##### Push Function

- This function put new value at the **Top**. Firstly it creates new Node with value and it's pointing into the first Node. After that it set the head pointer to the newly created Node. 

```
class Stack{
	private:
		...
	public:
		...
		void push(int value){
			ListNode* newNode = new ListNode(value, head);
			head = newNode;
		}
	
};
```

##### Pop Function

- This function removes the value at the **Top**. Firstly it checks if the Stack have any Node's. If yes 

```
class Stack{
	private:
		...
	public:
		...
		void pop(){
			if(head == nullptr){
				std::cout << "Error: No Node's in the list!\n";
				return;
			}else{
				ListNode* temp = head;
				head = head->next;
				delete temp;
			}
		}
};
```

