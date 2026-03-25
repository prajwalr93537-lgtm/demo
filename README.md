# demo
your dacg
class Queue:
    def __init__(self):
        self.qlist = []
    def isEmpty(self):
        return len(self) == 0
    def __len__(self):
        return len(self.qlist)
    def enqueue(self, item):
        self.qlist.append(item)
    def dequeue(self):
        assert not self.isEmpty(), "Cannot dequeue from an empty queue."
        data = self.qlist.pop(0)
        return data
    def display(self):
        print(self.qlist)
if __name__ == "__main__":
    q = Queue()
    print("Contents of queue:")
    q.display()
    print("\nEnqueue operations:")
    q.enqueue(25)
    q.enqueue(50)
    q.enqueue(75)
    q.enqueue(100)
    print("Contents of queue:")
    q.display()
    print("\nDequeue operations:")
    print(q.dequeue(), "is removed from queue")
    print(q.dequeue(), "is removed from queue")
    print("Contents of queue:")
    q.display()
 
