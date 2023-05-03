# **Operations in different lenguages**

## **PHP**

### Insert

```PHP
function addLast($value) {

    $n = new Node();
    
    if ($this->$head === null) {
        $this->$head = $n;
        $this->$tail = $n;
    } else {
        $this->$tail->$next = $n;
        $this->$tail = $n;
    }
}

function addFirst($value) {

    $n = new Node();

    if ($this->$head === null) {
        $this->$head = n;
        $this->$tail = n;
    } else {
        $n->$next = $head;
        $this->$head = $n;
    }
}
```

### Search

```PHP
function contains($head, $value) {

    if ($head === null) {
        return false;
    }

    if ($head === $value) {
        return true;
    }

    $n = $head;

    while ($n !== null && $n !== $value) {
        $n = $n->$next;
    }

    if ($n === $value) {
        return true;
    }

    return false;
}
```

### Delete

```PHP
function remove($head, $value) {

    if ($head === null) {
        return false;
    }

    $n = $head;

    if ($head === $value) {
        if ($tail === $value) {
            $this->$head = null;
            $this->$tail = null;
        } else {
            $this->$head = $n->$next;
        }
        return true;
    }

    while ($n->$next->$value !== $value && $n->$next !== null) {
        $n = $n->$next;
    }

    if ($n->$next->$value === value) {
        if ($n->next === $this->$tail) {
            $this->$tail = $n;
            $n->$next = null;
        } else {
            $n->$next = $n->$next->$next;
        }
        return true;
    }
    
    return false;
}
```

### Iterate

```PHP
function iterate($head) {

    $n = $head;

    while ($n !== null) {
        echo $n->$value;
        $n = $n->$next;
    }
}

function reverseIterate($head, $tail) {

    if ($tail !== null) {

        $n = $tail;

        while ($n !== $head) {

            $prev = $head;

            while ($prev->$next !== $n) {
                $prev = $prev->$next;
            }

            echo $n->$value;

            $n = $prev;
        }

        echo $n->$value;
    }
}
```