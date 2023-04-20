# **Operations in different lenguages**

## **Java**

### Insert

```Java
public static void addLast(int value) {
    Node n = new Node(value);
    if (head == null) {
        head = n;
        tail = n;
    } else {
        tail.next = n;
        tail = n;
    }
}

public static void addFirst(int value) {
    Node n = new Node(value);
    n.next = head;
    head = n;
    if (tail == null) {
        tail = n;
    }
}
```

### Search

```Java
public static boolean contains(Node head, int value) {
    Node n = head;
    while (n != null && n.value != value) {
        n = n.next;
    }
    if (n == null) {
        return false;
    }
    return true;
}
```

### Delete

```Java
public static boolean remove(Node head, int value) {
    if (head == null) {
        return false;
    }
    Node n = head;
    if (n.value == value) {
        if (head == tail) {
            head = null;
            tail = null;
        } else {
            head = head.next;
        }
        return true;
    }
    while (n.next != null && n.next != value) {
        n = n.next;
    }
    if (n.next != null) {
        if (n.next == tail) {
            tail = n;
            tail.next = null;
        } else {
            n.next = n.next.next;
        }
        return true;
    }
    return false;
}
```

### Iterate

```Java
public static void iterate(Node head) {
    Node n = head;
    while (n != null) {
        System.out.println(n.value);
        n = n.next;
    }
}

public static void reverseIterate(Node head, Node tail) {
    if (tail != null) {
        Node n = tail;
        while (n != head) {
            Node prev = head;
            while (prev.next != n) {
                prev = prev.next;
            }
            System.out.println(n.value);
            n = prev;
        }
        System.out.println(n.value);
    }
}
```