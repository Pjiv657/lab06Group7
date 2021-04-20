# lab06Group7
Liona Sadler (lsad313)
Pratik Jivanji 
Tumanu 

Exercise 5.6.1 - Java
1. What is the type of collection used in the exercise?
Queue
2. What are the different ways of iterating through a collection?
Using the interator() 
3. How do you find out the size of a collection?
Check queue.size()
4. How do you add an item to a collection? What happens if you try to add an item to a collection that is already full?
Type in add(). If there is no space left, it returns an error (IllegalStateException)
5. How do you remove an item to a collection? What happens if you try to remove an item that does not exist in the collection?
Type in remove(). If you try to remove an item, NoSuchElement will display, meaning the queue is empty.
6. Change the implementation of a FIFO queue to a LIFO queue in 5.6.1.
# // use python queue
from queue import Queue
import queue

# Initialise a queue
miqVoucherQ = LifoQueue(maxsize = 100)

# NB: Assume we do not know about objects in python, so create functions insteand

# define a function to add to end of queue
def fifoEnqueue(queue,item):
  return queue.put(item)
  
# define a functiion to remove from front of queue
def fifoDequeue(queue):
  return queue.get();
  
# define a function to find queue length
def fifoLength(queue):
    return queue.qsize()
    
# define a function to find if queue is empty
def fifoIsEmpty(queue):
    return queue.empty()
    
print(fifoLength(miqVoucherQ))
print(fifoIsEmpty(miqVoucherQ))

# Add some travellers
fifoEnqueue(miqVoucherQ,["Jones, E","10","10-01-2021","20-01-2021"])
fifoEnqueue(miqVoucherQ,["Amed, J","1","11-02-2021,20-02-2021"])
fifoEnqueue(miqVoucherQ,["Vine, M","8","9-01-2021,21-09-2021"])

# Show queue length, isEmpty
print(miqVoucherQ);
print(fifoLength(miqVoucherQ));
print(fifoIsEmpty(miqVoucherQ));

# remove from the queue and make sure FIFO
#fifoDequeue(miqVoucherQ) 
#print(fifoLength(miqVoucherQ));
while not miqVoucherQ.empty():
    print(miqVoucherQ.get())


Exercise 5.6.2
1. What is the type of collection used in the exercise?
List
2. What are the different ways of iterating through a collection?
Can use a loop (while and/or for)
3. How do you find out the size of a collection?
Use len()
4. How do you add an item to a collection? What happens if you try to add an item to a collection that is already full?
Use append --> bedArr.append. Since there is no limit to a list, it will grow.
6. How do you remove an item to a collection? What happens if you try to remove an item that does not exist in the collection?
Use remove --> bedArr.remove or you can use pop(). If an item does not exist, a value error will be displayed. 
