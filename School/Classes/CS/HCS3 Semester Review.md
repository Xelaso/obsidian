

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

Unit 4 - Algorithmic Analysis

