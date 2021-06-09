
# Collections
framework/container to access prepackaged data structure.

## List
1. **ArrayList**: dynamic array, default size-10, new size = (current_size x 3/2+1), null allowed  
2. **LinkedList**: dynamic array with insertion efficient  
3. **Vector**: thread safe, same like arraylist  

## Queue FIFO
1. **Priority queue**: special type of queue wherein all elements ordered as per comparator, not thread safe   
2. **ArrayDeque**   
3. **ArrayBlocking queue**  

## Set: does not allow duplicate
1. **Hashset** does not allow duplicates    
2. **LinkedHasedSet**: ArrayList without duplicate  
3. **TreeSet** : ordered ascending 
4. **EnumSet**: set implementation which contain only enum values,     	

## Map: has string as key  
1. **HashMap**: Null key allowed, implements hashtable underlying, unordered, not thread safe, can make synchronized Collections.synchronizedMap(hashMap);      
2. **HashTable**: Null key/value not allowed, slow, thread safe  
3. **TreeMap**: implements red black tree, wherein all elements ordered as per compareTo() method    
4. **NavigableMap**:  
5. **LinkedHashMap**: ordered HashMap  
6. **ConcurrentHashMap**: same like hashtable, but not have locks like hashtable  

1.Object put(Object key, Object value)  
2.void putAll(Map map)  
3.Object remove(Object key)  
4.Object get(Object key)  
5.boolean containsKey(Object key)  
6.Set keySet()  
7.Set entrySet()  
8.Object getKey(), Object getValue()  

## Queue  
1. peek(): return object at top of current queue  
2. poll(): return object and remove queue value, or return null if queue empty     
3. remove(): same as poll(), but throw NoSuchElementException if queue empty  


**Concurrent collection classes**:  alternative to java collections classes with providing concurrency  
**Iterator**  Iterator itr = list.iterator(); while (itr.hasNext()) {System.out.print(itr.next() + " "); }   
**List Iterator**: traverse front and back,  ListIterator i = list.listIterator();while (i.hasPrevious()) {System.out.print(i.previous() + " "); }
**Synchronized Collection**: 
  1. Collections.synchronizedCollection(Collection c)
` 2. Collections.synchronizedList(List list)
  3. Collections.synchronizedMap(Map<K,V> m)
  4. Collections.synchronizedSet(Set s)
  5. Collections.synchronizedSortedMap(SortedMap<K,V> m)
  6. Collections.synchronizedSortedSet(SortedSet s)

**Default size**:  
|Collections | Capacity |
|:------------|:----------|
|ArrayList   | 10       |
|Vector      | 10       |
|HashSet     | 16       |
|HashMap     | 16       |
|HashTable   | 11       |
|HashSet     | 16, LoadFactor:0.75       |

**Collections vs Collection** 
Collections are utility class in java.util package. It consists of only static methods which are used to operate on objects of type Collection.  
|Collections Methods                  | Description  |
|:-------------------------------------|:-------------------------------------------------------------|
|Collections.max()	                  |This method returns maximum element in the specified collection.|
|Collections.min()	                  |This method returns minimum element in the given collection.|
|Collections.sort()	                  |This method sorts the specified collection.|
|Collections.shuffle()	              |This method randomly shuffles the elements in the specified collection.|
|Collections.synchronizedCollection() |This method returns synchronized collection backed by the specified collection.|
|Collections.binarySearch()	          |This method searches the specified collection for the specified object using binary search algorithm.|
|Collections.disjoint()	              |This method returns true if two specified collections have no elements in c|ommon.|
|Collections.copy()	                  |This method copies all elements from one collection to another collectio|n.|
|Collections.reverse()	              |This method reverses the order of elements in the specified collection.|
|Collections.unmodifiableList()	              |This method make List as Final|

**CopyOnWriteArrayList**: Modifications implemented in fresh copy  
**HashMap handles collision**: it uses balanced tree instead of List  

**Comparable**
**Comparator*