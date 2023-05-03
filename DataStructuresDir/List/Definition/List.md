# **List**

## **What** is a List?
* A **List** is a data structure that contains a linear sequence of a number of elements that have the same type.

* The items can be of any data type
    * Numbers (1, 2, 10, 8, 12).
    * Characters ('H', 'O', 'L', 'A').
    * Cities ("MVD", "BSAS", "NY").

* We need to define the order of the items.

## **Types:**

### 1. **Linked List**
 It is a data structure consisting of a group of nodes which together represent a sequence, each node is composed of data and a reference (in other words, a link) to the next node in the sequence.

 This structure allows for efficient insertion or removal of elements from any position in the sequence during iteration

 ![Linked list information](/DataStructuresDir/List/img/linked-list.jpeg)


### **Pseudocode for Basic Operations:**

***

### **Insert:**

Inserts a node at the end of the list.

```
Pre: "value" is the value to add to the list
Post: value has been placed at the tail of the list
function AddLast(value)
    n ← node(value)
    if head = ø
        head ← n
        tail ← n
    else
        tail.next ← n
        tail ← n
    end if
end AddLast
```

Inserts a node at the top of the list

```
Pre: "value" is the value to add to the list
Post: value has been placed at the head of the list
function AddFirst(value)
    n ← node(value)
    n.next ← head
    head ← n
    if tail = ø
        tail ← n
    end if
end AddFirst
```

### **Search:**

```
Pre: "head" is the head in the list
     "value" is the value to search for
Post: the item is either in the linked list, true; otherwise false
function Contains(head, value)
    n ← head
    while (n != ø and n.value != value)
        n ← n.next
    end while
    if n = ø
        return false
    end if
    return true
end Contains
```

### **Delete:**

```
Pre: "head" is the head node in the list
     "value" is the value to remove from the list
Post: value is removed from the list, true, otherwise false
function Remove(head,value)
    if head = ø
        return false
    end if
    n ← head
    if n.value = value
        if head = tail
            head ← ø
            tail ← ø
        else
            head ← head.next
        end if
        return true
    end if
    while (n.next != ø and n.next.value != value)
        n ← n.next
    end while
    if n.next != ø
        if n.next = tail
            tail ← n
            tail.next = ø
        else
            n.next ← n.next.next
        end if
        return true
    end if
    return false
end Remove
```

### **Iterate:**

```
Pre: "head is the head node in the list
Post: the items in the list have been iteretated
function Iterate(head)
    n ← head
    while n != ø
        print n.value
        n ← n.next
    end while
end Iterate
```

### **Iterate in Reverse:**

```
Pre: head and tail belong to the same list
Post: the items in the list have been traversed in reverse order
function ReverseIterate(head, tail)
    if tail != ø
        n ← tail
        while n != head
            prev ← head
            while prev.next != n
                prev ← prev.next
            end while
            print n.value
            n ← prev
        end while
        print n.value
    end if
end ReverseIterate
```

***

### **Complexities:**
**Time**:
| Access | Search | Insertion | Deletion |
|--------|--------|-----------|----------|
|  O(n)  | O(n)   | O(1)      | O(n)     |

**Space:**

O(n)

***

You can see the examples of the operations in Java
here [link to operations](../Methods/MethodsJava.md)

You can see the examples of the operations in C#
here [link to operations](../Methods/MethodsCSharp.md)

You can see the examples of the operations in Javascript
here [link to operations](../Methods/MethodsJS.md)

You can see the examples of the operations in PHP
here [link to operations](../Methods/MethodsPHP.md)


