
Alexander So
6th Period HCS3
[2, 5]
# Unit 1 - Java Review

1.
```
Iterator<Double> iter = list.iterator();
while(iter.hasNext()){
	double num = iter.next();
	if(num < 2.5){
		iter.remove();
	}
}

```
  
2.
```
int count = 0;
for(double num : list){
	if(num >= 3.6){
		count++;
	}
}
```
3.
```
int [][] birthdays = new int[12][13];
```

4.
```
int month = 1;
for(int[] row : birthdays){
	int count = 0;
	for(int num : row){
		count += num;
	}
	
	System.out.println("There are " + count + " birthdays in month " + month);
	month++;
}
```


5.
```
int most, month, grade;
most = month = grade = 0;
int m = 0;
for(int[] row : birthdays){
	int g = 0;
	for(int num : row){
		if(most < num){
			most = num;
			month = count;
			grade = g;
		}
		g++;
	}
	m++;
}
System.out.println("Grade " + grade + ", month " + month + " has the most birthdays.");
```

# Unit 2 - OOP Review

6.
```
The difference between an abstract class and an interface is an abstract class is allowed to have method bodies. 
```

7.
```
Make the subclass abstract
```

8.
```
public interface Lockable{
	int key;
	public void setKey(int key);
	public void lock(int key);
	public void unlock(int key);
	public boolean isLocked();
}
```

9.
```
public class Pegasus extends MythicalCreatures implements SuperPower, Flying
```

10.
```
protected void paintComponent(Graphics g) {
	int width = 100;
	int height = 200;
	int x = (getWidth() - width)/2;
	int y = (getHeight() - height)/2;
	g2.setColor(Color.GREEN);
	g2.fillRect(x,y,width,height);
	g2.setColor(Color.RED);
	g2.drawLine(x,y+height,x+width,y); 
}
```

11.
```
other members of the enclosing class
```

12.
```
actionEvent
```

13.
```
actionListener
```

14.
```
actionPerformed
```

15.
```
redraw()
```


# Unit 3 - File Input/Output

16.
```
System.out.printf("18s +8d  +.3f", stuname, id, gpa);
```

17.
```
Text stores readable and easily modifiable formats, while binary is in binary form
Text files can be transfered between computer systems, binary files cannot
```

18.
```
Sequential access is in order, while random access randomly accesses data in no set order
```

19.
```
Data caching is storing data temporarily in a location for faster and easier access. This is important in I/O because it is temporary, and if it is not saved it is lost.
```

20.
```
Serializable
```

21.
```
PrintWriter write = new PrintWriter("final.dat");
write.println("Up\nOppenheimer\nInception");
write.close();

```

22.
```
Scanner scan = new Scanner(new File("final.dat"));
while(scan.hasNextLine()){
	System.out.println(scan.nextLine());
}

```

# Unit 4 - Algorithmic Analysis

23.
```
Big O notation is a way of notating the efficiency of code, ie O(n) and O(n^2)
```

24.
```
b: instant, print
c: linear, single loop
d: quadratic, nested loop
e: logorithmic, binary search
f: loglinear, binary tree sorting
g: exponential: recursion fibonachi 
```

25.
```
B: O(n^2)
C: O(n^5)
D: O(n^4)
E: O(n^2)
```

26.
```
A: O(N)
B: O(N^2)
C: O(log N)
```

27.
```
O(n^2)
```
28.
```
Still O(n^2)
```
29.
```
Still O(n^2)
```
30.
```
35 17 19 14 28 92
28 17 19 14 35 92
14 17 19 28 35 92
14 17 19 28 35 92
14 17 19 28 35 92
```

31.
```
O(n^2)
```
32.
```
O(n)
```
33.
```
O(n^2)
```
34.
```
17 35 92 14 28 19
17 35 92 14 28 19
14 17 35 92 28 19
14 17 28 35 92 19
14 17 19 28 35 92
```

35.
```
O(nlogn)
```
36.
```
O(nlogn)
```
37.
```
O(nlogn)
```
38.
```
[35, 17, 92, 14, 28, 19]
[35, 17, 92] [14, 28, 19]
[35, 17] [92] [14, 28] [19]
[35] [17] [92] [14] [28] [19]
[17, 35] [92] [14, 28] [19]
[17, 35, 92] [14, 19, 28]
[14, 17, 19, 28, 35, 92]
```

39.
```
O(nlogn)
```
40.
```
O(nlogn)
```
41.
```
O(n^2)
```
42.
```
[81, 64, 50, 29, 36, 47] pivot = 50
------------------------
[50, 64, 81, 29, 36, 47] 
[47, 36, 29, 50] | [81, 64] (| is partition); 36 and 81 are the pivots
-------------------------
[36, 47, 29, 50] | [81, 64]
[29, 36] | [47, 50] | [64, 81] 29 and 47 are the pivots
--------------------------
[29, 36] | [47, 50] | [64, 81]
--------------------------
[29, 36, 47, 50, 64, 81]
```


# Unit 5 - Sets, and Maps

45.
```
A set is a collection of data that is similar to an array but cannot contain duplicates
```

46.
```
A TreeSet is sorted, while a HashSet is unsorted. 
A HashSet has a add of O(1), while TreeSet has O(logn)
HashSet contains method is O(1) while TreeSet is O(logn) 
```

47.
```
TreeSet<String> temp = new TreeSet<>();
for(int i = 0; i < mySet.size(); i++){
	if(mySet.get(i).equals("West")){
		break;
	}
	temp.add(mySet.get(i));
}
for(int i = 0; i < temp.size(); i++){
	System.out.println(temp.get(i));
}
```

48.
```
A map is a collection of data that is stored via a key and value. There cannot be two of the same key, but different keys can point to the same value
```

49.
```
HashMap has a get of O(1), ContainsKey of O(1)
TreeMap has a get of O(logn) and a ContainsKey of O(logn)
```

50.
```
Iterator<String> iter = myMap.keySet().iterator();
while(iter.hasNext()){
	String str = iter.next();
	if(myMap.get(str) >= 3.6){
		System.out.println(str);
	}
}
```

# Unit 6 - Linked Lists and Generic Programming

51.
```
A data type with no set type, it can accept any thing within the given constraints
```

52.
```
IllegalStateException is when you try and do something while the iterator isnt holding a value, such as doing remove twice. NoSuchElementException is when you do something that causes you to go out of bounds and try to keep going 
```

53.
```
[Martin, Harvey, Juliet, Marlene, Tom]
```

54.
```
Iterator<String> iter = staff.listIterator();
while(iter.hasNext()){
	String str = iter.next();
	if(str.contains("ar")){
		iter.remove();
	}
	System.out.println(str);
}
```

55.
```
Improves addLast but not removelast
```

56.
```
a: linked list
b: linked list
c: array
d: array
```

57.
```
public void addFirst(E obj){
	ListNode<E> node = new ListNode<E>(obj, null);
	if(front == null){
		front = back = node;
	}
	else{
		node.setNext(front);
		front = node;
	}
}
```

58.
```
public E removeFirst(){
	if(front == null){
		throw new NoSuchElementException;
	}
	E val = front.getValue();
	if(front == back){
		front = back = null;
		return val;
	}
	front = front.getNext();
	return val;
}
```

59.
```
Have a generic type (<K>) in the class heading or a method heading
```

60.
```
Raw types mean using a generic type without specifying a type parameter
```


61.
```
public class Practice <K extends AceIt, V extends Exam>
```

62.
```
public int getHeadache(List<E extends Painkiller> listObj)
```

# Unit 7 - Special Linked Lists

63.
```
removeLast()
```

64.
```
ListNode<Integer> temp = back.getNext();
double num = 0;
int count = 0;
do{
	num += temp.getValue();
	count++;
	temp = temp.getNext();
} while(temp != back);

num /= count;

```

65.
```

public void addFirst(E val){
	ListNode<E> node = new ListNode<>(val, null);
	if(back == null){
		back = node;
	}
	else{
		node.setNext(back.getNext());
		back.setNext(node);
	}
}

public E removeFirst(){
	if(back == null){
		throw new NoSuchElementException;
	}	
	E val = back.getNext().getValue();
	back.setNext(back.getNext().getNext());
	return val;
}

```


66.
```
public void addFirst(E val){
	ListNode<E> node = new ListNode<>(val, null, null);
	if(front == null){
		front = back = node;
	}
	else{
		node.setNext(front);
		front = node;
	}
}

public E removeFirst(E val){
	if(front == null){
		throw new NoSuchElementException;
	}
	E val = front.getValue();
	if(front == back){
		front = back = null;
		return val;
	}
	else{
		front = front.getNext();
		front.setPrevious(null);
	}
}

```


67.
```
Singly Linked List
```

68.
```
addFirst: O(1)
addLast: O(1)
removeFirst: O(1)
removeLast: O(n)
get: O(n)
```

69.
```
Hashing transforming any key/string into a value to be stored in a hash table for fast access. The ideal time complexity is O(1)
```

70.
```
hashCode()
```

71.
```
Collision is when two different values have the same hash code, resulting in the need to resolve it using something like chaining
```

72.
```
a) If a collision occurs, keep going linearly until a empty slot is found
b) If a collision occurs, check the i^2 slot in the ith iteration until a slot if found
c) Each spot in a hashtable holds a linked list. if a collision occurs, 'chain' the value onto the linked list (adding it to the list)
```
