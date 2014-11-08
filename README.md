Python
======

number 4

alist.append(item) - adds a new item to the end of a list
alist.insert(i, item) - inserts an item at the ith position in a list
alist.pop() - removes and returns the last item in a list
alist.pop(i) - removes and returns the ith item in a list
alist.sort() - modifies a list to be sorted
alist.reverse() - modifies a list to be in reverse order
alist.index(item) - returns the index of the first occurence of item
alist.count(item) - returns the number of occurences of item
alist.remove(item) - removes the first occurence of item




myList = [7, 9, 'a', 'cat', False]
>>> myList
[7, 9, 'a', 'cat', False]
>>> myList.append(3.14)
>>> myList.append(7)
>>> myList
[7, 9, 'a', 'cat', False, 3.14, 7]
>>> myList.insert(3, 'dog')
>>> myList
[7, 9, 'a', 'dog', 'cat', False, 3.14, 7]
>>> myList.index('cat')
4
>>> myList.count(7)
2
>>> myList.remove(7)
>>> myList
[9, 'a', 'dog', 'cat', False, 3.14, 7]
>>> myList.pop(myList.index('dog'))
'dog'
>>> myList
[9, 'a', 'cat', False, 3.14, 7]
>>> myString = "the quick brown fox"
>>> myString.split()
['the', 'quick', 'brown', 'fox']




mylist = [7.76, 9.96, 14.07, 8.50, 15.55, 15.85, 56.93, 21.65, 10.40, 19.64]

def range(alist):
    return max(alist)-min(alist)

def minimum(alist):
    return min(alist)

def maximum(alist):
    return max(alist)

def mean(alist):
    mean = sum(alist)/len(alist)
    return mean

def median(alist):
    copylist = alist[:]
    copylist.sort()
    if len(copylist) % 2 == 0:
        rightmid len(copylist)//2
        leftmid = rightmid - 1
        median = (copylist[leftmid] + copylist[rightmid])/2
    else:
        mid = len(copylist)//2
        median = copylist[mid]
    return median

import math
def standarddev(alist):
    themean = mean(alist)

    total = 0
    for each in alist:
        difference = each - themean
        diffsq = difference ** 2
        total = total + diffsq

    sdev = math.sqrt(total/len(alist)-1)
    return sdev
    
    
def mode(alist):
    countdict = {}

    for item in alist:
        if item in countdict:
            countdict[item] = countdict[item]+1
        else:
            countdict[item] = 1

    countlist = countdict.values()
    maxcount = max(countlist)

    modelist = [ ]
    for item in countdict:
        if countdict[item] == maxcount:
            modelist.append(item)

    return modelist
