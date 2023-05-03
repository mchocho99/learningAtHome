# **Operations in different lenguages**

## **Javascript**

### Insert

```js
const addLast = (value) => {

    const n = new Node(value);

    if (this.head === null) {
        head = n;
        tail = n;
    } else {
        this.tail.next = n;
        this.tail = n;
    }
}

const addFirst = (value, head) => {
    
    const n = new Node(value)

    n.next = head;

    head = n;

    if (tail === null) {
        tail = n;
    }
}
```

### Search

```js
const contains = (value) => {

    const n = this.head;

    while (n !== null && n.value !== value) {
        n = n.next;
    }

    if (n === value) {
        return true;
    }

    return false;
}
```

### Delete

```js
const remove = (value) => {

    const head = this.head;

    if (head === null) {
        return false;
    }

    const tail = this.tail;
    const n = head;

    if (head.value === value) {
        if (tail === head) {
            tail = null;
            head = null;
        } else {
            head = n.next;
        }
        return true;
    }

    while (n.next !== null && n.next.value !== value) {
        n = n.next;
    }

    if (n.next.value === value) {
        if (n.next === tail) {
            n.next = null;
            tail = n;
        } else {
            n.next = n.next.next;
        }
        return true;
    }

    return false;
}
```

### Iterate

```js
const iterate = () => {

    const n = head;

    while (n !== null) {
        console.log(n.value);
        n = n.next;
    }
}

const reverseIterate = () => {
    const tail = this.tail;
    const head = this.head;

    if (tail !== null) {

        Node n = tail;

        while (n !==head) {
            Node prev = head;

            while (prev.next !== n) {
                prev = prev.next;
            }

            console.log(n.value);

            n = prev;
        }

        console.log(n.value);
    }
}
```