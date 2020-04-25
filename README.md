# Stack_and_Queues_Data_Structure



> ## Node class creation: :wink:

``` js
class Node {
    constructor(value){
        this.value = value;
        this.next = null;
    }
}
```

> ## class method creation for Stack class, LIFO (Last In First Out Data Structure): :laughing:

``` js
class Stack {
    constructor(){
        this.first = null;
        this.last = null;
        this.size = 0;
    }
    push(val){
        var newNode = new Node(val);
        if(!this.first){
            this.first = newNode;
            this.last = newNode;
        } else {
            var temp = this.first;
            this.first = newNode;
            this.first.next = temp;
        }
        return ++this.size;
    }
    pop(){
        if(!this.first) return null;
        var temp = this.first;
        if(this.first === this.last){
            this.last = null;
        }
        this.first = this.first.next;
        this.size--;
        return temp.value;
    }
}
```

![stack](https://github.com/NoriKaneshige/Stack_and_Queues_Data_Structure/blob/master/stack.png)
![stack_push](https://github.com/NoriKaneshige/Stack_and_Queues_Data_Structure/blob/master/stack_push.png)
![stack_pop](https://github.com/NoriKaneshige/Stack_and_Queues_Data_Structure/blob/master/stack_pop.png)
![stack_bigO](https://github.com/NoriKaneshige/Stack_and_Queues_Data_Structure/blob/master/stack_bigO.png)
![stack](https://github.com/NoriKaneshige/Stack_and_Queues_Data_Structure/blob/master/stack.png)



> ## class method creation for Queue class, FIFO (First In First Out Data Structure): :laughing:

``` js
class Queue {
    constructor(){
        this.first = null;
        this.last = null;
        this.size = 0;
    }

    // add something in
    // add to the end
    enqueue(val){
        var newNode = new Node(val);
        if(!this.first){
            this.first = newNode;
            this.last = newNode;
        } else {
            this.last.next = newNode;
            this.last = newNode;
        }
        return ++this.size;
    }

    // return and remove the first thing that was added in
    // remove from the beginning
    dequeue(){
        if(!this.first) return null;

        var temp = this.first;
        if(this.first === this.last) {
            this.last = null;
        }
        this.first = this.first.next;
        this.size--;
        return temp.value;
    }
}

```
![queues](https://github.com/NoriKaneshige/Stack_and_Queues_Data_Structure/blob/master/queues.png)
![enqueues](https://github.com/NoriKaneshige/Stack_and_Queues_Data_Structure/blob/master/engueue.png)
![dequeues](https://github.com/NoriKaneshige/Stack_and_Queues_Data_Structure/blob/master/degueue.png)
![queues_bigO](https://github.com/NoriKaneshige/Stack_and_Queues_Data_Structure/blob/master/queues_bogO.png)
