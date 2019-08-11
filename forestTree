import random


class BinaryHeap:
    def __init__(self):
        self.items = []
        self.heapList = [0]
        self.currentSize = 0

    def size(self):
        return len(self.items)

    def parent(self, i):
        return (i - 1) // 2

    def left(self, i):
        return 2 * i + 1

    def right(self, i):
        return 2 * i + 2

    def get(self, i):
        return self.items[i]


    def insert(self, key):
        index = self.size()
        self.items.append(key)

        while (index != 0):
            p = self.parent(index)
            index = p

    def percUp(self, i):
        while i // 2 > 0:
            if self.heapList[i] < self.heapList[i // 2]:
                tmp = self.heapList[i // 2]
                self.heapList[i // 2] = self.heapList[i]
                self.heapList[i] = tmp
            i = i // 2

    def percDown(self, i):
        while (i * 2) <= self.currentSize:
            mc = self.minChild(i)
            if self.heapList[i] > self.heapList[mc]:
                tmp = self.heapList[i]
                self.heapList[i] = self.heapList[mc]
                self.heapList[mc] = tmp
            i = mc

    def minChild(self, i):
        if i * 2 + 1 > self.currentSize:
            return i * 2
        else:
            if self.heapList[i * 2] < self.heapList[i * 2 + 1]:
                return i * 2
            else:
                return i * 2 + 1

    def buildHeap(self, alist):
        i = len(alist) // 2
        self.currentSize = len(alist)
        self.heapList = [0] + alist[:]
        while (i > 0):
            self.percDown(i)
            i = i - 1

        return self.heapList




def buildTree():
    bheap = BinaryHeap()

    # Generate random number and insert to the binary heap
    for i in range(10):
        rand_num = random.randint(1,101)

        bheap.insert(rand_num)

    print("Binary Heap Tree Result: {}".format(bheap))

    # Print the List form of the Binary Heap
    print("List form of Binary Heap: {}".format(bheap.items))

    # Passing the generated list, to build the binary heap
    print("Tree form of Binary Heap: {}".format(bheap.buildHeap(bheap.items)))



if __name__ == "__main__":
    buildTree()
