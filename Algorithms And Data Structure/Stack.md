### Structure of Stack and it's definition

- Stack is a data structure that is only accessible from the **Top**. The most popular functions it provide are: 
	- [[#Push Function]] - Puts the element on **Top**.
	- [[#Pop Function]] - Removes the element at **Top**.
	- [[#IsEmpty function]] - Check if the Stack is empty, return boolean.
	- [[#Top function]] - Returns  the value at **Top**.


![[Stack.excalidraw|100%]]

### Implementation for Linked List Stack

#### Using a STL library Stack

- The best way of creating a Stack class is just by using a in build library Stack.

```
#include <stack>

int main(){
	stack<data type> name_of_stack;
}
```

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


##### IsEmpty function

- This function checks if the stack is empty. Returns a boolean.

```
class Stack{
	private:
		...
	public:
		...
		bool isEmpty(){
			if(head == nullptr){
				return true;
			}else{
				return false;
			}
		}
};
```

##### Top function

```
class Stack{
	private:
		...
	public:
		...
		<datatype> Top(){
			ListNode* temp = head;
			return temp->val;
		}
};
```
### Methods and use of a Stack

#### Reversing a string in a O(n) time and O(n) space complexity
[[344. Reverse String]]

- We firstly declare a stack class containing characters. Then we iterate through the Array to put all of the characters into the stack. Then we replace every character in the string in a reverse order thanks to LIFO (Last In First Out). We swap the character and then pop the element from the stack.

```
#include <stack>
#include <vector>
class Solution {
public:
    void reverseString(std::vector<char>& s) {
        std::stack<char> stack;
        for(int i = 0; i < s.size(); i++){
            stack.push(s[i]);
        }

        for(int i = 0; i < s.size(); i++){
            s[i] = stack.top();
            stack.pop();
        }
    }
};
```