# **Operations in different lenguages**

## **C#**

### Insert

```C#
public static void AddLast (int value) {

    Node n = new Node(value);

    if (head == null) {
        head = n;
        tail = n;
    } else {
        tail.next = n;
        tail = n;
    }
}

public static void AddFirst (int value, Node head) {
    
    Node n = new Node(value);

    n.next = head;

    head = n;

    if (tail == null) {
        tail = n;
    }
}
```

### Search

```C#
public static bool Contains (int value) {

    Node n = head;

    while (n != null && n.value != value) {
        n = n.next;
    }

    if (n == value) {
        return true;
    }

    return false;
}
```

### Delete

```C#
public static bool Remove (int value) {

    if (head == null) {
        return false;
    }

    Node n = head;

    if (n.value == value) {
        if (head == tail) {
            tail = null;
            head = null;
        } else {
            head = n.next;
        }
        return true;
    }

    while (n.next != null && n.next.value != value) {
        n = n.next;
    }

    if (n.next.value == value) {
        if (n.next == tail) {
            tail = n;
            n.next = null;
        } else {
            n.next = n.next.next;
        }
        return true;
    }

    return false;
}
```

### Iterate

```C#
public static void Iterate () {

    Node n = head;

    while (n != null) {
        Console.WriteLine(n.value);
        n = n.next;
    }
}

public static void ReverseIterate () {
    if (tail != null) {
        Node n = tail;
        while (n != head) {
            Node prev = head;
            while (prev.next != n) {
                prev = prev.next;
            }
            Console.WriteLine(n.value);
            n = prev;
        }
        Console.WriteLine(n.value);
    }
}
```