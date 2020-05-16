package linkedLists;

import java.util.Vector;


// Linked list Node. 
// This inner class is made static 
// so that main() can access it 

class Node { 

    public Object data; 
    public Node next; 

    // Constructor 
    public Node() { 

    }
    
    public Node(Object data) { 
        this.data = data; 
        this.next = null; 
    }
    
    public Node(Object data, Node next) { 
        this.data = data; 
        this.next = next; 
    }
    
//	@Override
//	public String toString() {
//		return "\nNode =>\n { data = " + data + " \n\t{ next = " + next + " } }";
//	}
    
	@Override
	public String toString() {
		return data + " " ;
	}
} 

class linkedList {
	
	public Node head; // head of list 

	
	// Initiating Linked List
	public linkedList() {	
		// TODO Auto-generated constructor stub
		// At first there will be nothing at head node 
		// so we create an empty node
		// which has nothing in its data and next, meaning they are null
		this.head = new Node("***Root***");	
	}
	
	// Print the Linked List
	public void printList() {
		Vector<Object> nodes = new Vector<>();
		Node currentNode = this.head.next;
		while(currentNode != null) {
			nodes.add(currentNode);
			
			currentNode = currentNode.next;
		}
		
		
		System.out.println(nodes);
		
	}
	
	// Print All Nodes
	public void print_allNodes() {
		Vector<Object> nodes = new Vector<>();
		Node currentNode = this.head;
		
		while(currentNode != null) {
			nodes.add(currentNode.toString());
			currentNode = currentNode.next;
		}
		
		int index = 0;
		for (Object item: nodes) {
			System.out.println("index : " + index + " => " + item + ", ");
			index ++;
		}
	
	}
	
	
	// **************INSERTION**************
	
    // Append a new node  
    public void append(Object data) { 
        // Create a new node with given data 
        Node new_node = new Node(data); 
  
        // If the Linked List is empty, 
        // then make the new node as head 
        if (this.head.next == null) { 
            this.head.next = new_node; 
            
            return;
        } 
        
        // Else traverse till the last node 
        // and insert the new_node there 
        Node currentNode = this.head;  // Here we will face a null pointer exception
        							   // if we set "Node currentNode = this.head.next"	
        while (currentNode.next != null) { 
        	currentNode = currentNode.next; 
        } 
  
        // Insert the new_node at last node 
        currentNode.next = new_node; 
         
    }
    
	// Prepend a new node
	public void prepend(Object data) {
		// As we are creating the first node of the linked list
		// therefore this node's next will be equal to the head's next
		Node node = new Node(data, this.head.next); 
		
		// now we put the newly created node in the head's next 
		// as this one is suppose to be the first node
		this.head.next = node;
	}
	
	// Insert A Node
	public void insert(Object data, Object new_data) {
		Node current_node = this.head;
		
		while(current_node.next != null) {
			if(data.toString().equals(current_node.data.toString())) {
				Node new_node = new Node(new_data, current_node.next);
				current_node.next = new_node;
				
				break;
			}
			
			current_node = current_node.next;
		}
		
		if(current_node.next == null) {
			prepend(new_data);
		}
		
	}
	
	
	// Remove
	public void remove(Object item) {
		Node previous_node = this.head;
		Node current_node = previous_node.next;
		
		while(current_node != null) {
			if (current_node.data.toString().equals(item.toString())) {
				break;
			}
			previous_node = current_node;
			current_node = current_node.next;
		}
		
		if(current_node == null) {
			return;
		}
		
		if(this.head.toString().equals(previous_node.toString())) {
			this.head.next = current_node.next;
		}
		else {
			previous_node.next = current_node.next;
		}
	}
	
	// Search
	public String search(Object item) {
		Node current_node = this.head.next;
		
		while(current_node != null) {
			if(item.toString().equals(current_node.data.toString())) {
//				System.out.println(current_node.toString());
				return current_node.toString();
			}

			current_node = current_node.next;
		}
		return "Not Found";
	}
	
	
	
	
}


public class LinkedList_singly {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		
		
		
		linkedList ll = new linkedList();
		
		ll.prepend(1);
		ll.append(2);
		ll.prepend(10);
		
			
		
		ll.insert(1, 3);
		
		ll.remove(2);
		
		ll.printList();
		
		
		System.out.print("Finding a specific Node\n" + ll.search(2));

		
		

	}

}
