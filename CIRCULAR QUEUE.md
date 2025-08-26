# Exp No: 36  
## Circular Queue 
---

### AIM  
To write a Python program with a function to insert integer values into a Circular Queue.

---

### ALGORITHM

1. Start  
2. Check if the Circular Queue is full  
   - If `size == max_size`, print `"Queue is full"` and exit the function  
3. If the queue is not full:  
   - Read the element to be inserted   
   - Insert the element at the `tail` position  
   - Update tail using: `tail = (tail + 1) % max_size` (circular increment)  
   - Increment `size` by 1  
4. End

---

### PROGRAM

```
# 212223060073
# Gowri Sankari R
class Queue:
    def __init__(self,size):
        self.items=[0]*size
        self.max=size
        self.head,self.tail,self.size=0,0,0
    def enqueue(self,item):
        if self.is_list_full():
            print("Queue is full")
            return
        self.items[self.tail]=item
        self.tail=(self.tail+1)%self.max
        self.size+=1
    def dequeue(self):
        item=self.items[self.head]
        self.head=(self.head+1)%self.max
        self.size-=1
        return item
    def is_list_full(self):
        if self.size==self.max:
            return True
        return False
    def is_empty(self):
        if self.size==0:
            return True
        return False
size=int(input())
queue=Queue(size)
str=int(input())
str1=int(input())
str2=int(input())
queue.enqueue(str)
queue.enqueue(str1)
queue.enqueue(str2)
print(queue.items)
```

### OUTPUT
<img width="1185" height="484" alt="14B" src="https://github.com/user-attachments/assets/2fbea3aa-09ed-4be5-9c07-f95832850a27" />

### RESULT
Thus the Python program with a function to insert integer values into a Circular Queue is implemented and executed successfully
