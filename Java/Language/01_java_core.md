# Java

- **JDK** is (JRE+devTools) - For developer contains javac,debugging tools,archieve tool(jar), javadoc  
- **JRE** is (JVM+lib) - For layman users to run java program  
- **JVM** is Interpreter execute byte code to machine code, contins JustInTime compiler  
- **ClassLoader**: part of JRE, loads class file to JVM  

Java is not fully oops language, due usage of primitive datatypes.

``` 
import java.Io.*;	//this package used while code in notepad  
import java.util.Scanner ;
class Hello{
  public static void main(String[]args){
    Scanner input = new Scanner(Sytem.in);
    a=input.nextInt();
    System.out.println(); //print only one line and move to next line
    System.out.print(); //print line and remain in same line we have to give \n
    System.out.printf(“%d”,$i); //print string stream
  } 
}
```
---
- **Comments**: 1. Singleline: (//) 2. Multiline: (/*.. */) 3. Documentation: (/**…\*/)  
- **Keywords**: Predefined meaning (53) words.  
- **Packages**: Collection of similar classes, interfaces and sub packages.  
```import pkg1 [.pkg2].(classname | *); //import java.io.*;```  

**Commands**  
how to compile: ```javac -d directory javafilename.java```       	
how to run: ```java myppack.javafilename```     
how to define a package in that program: ```package packagename;```    
how to import package: ```import packagename.\*;```     
how to import using fully qualified name without import keyword: ```package classname```;   

- **Constant**: Immutable. Declare as final static.  eg: static final double PI=3.14   
Note: if it is declared as private inside a class, it can be redeclare in another class  

- **Enum**:  group of constant( final,static)
```
enum Level { LOW, MEDIUM, HIGH }
Level myVar = Level.MEDIUM;
```
- **Null**: case sensitive, not falls under any type, null==null is true


## Variable:  
Basic unit of storage   
1. **Local variable**: inside method 
2. **Instant variable**: inside clas 
3. **Static variable**: Declared as static  

## Datatype:  
Predefined memory storage  
1. **b**yte = -+128 size of 1 byte   
2. **s**hort = -+32,768 size of 2 byte   
3. **i**nt = -+2,14,74,83,648 size of 4 byte   
4. **l**ong = -+9,22,33,72,03,68,54,775 size of 8 byte  
5. **f**loat = . after 6 digit, size of 4 byte   
6. **d**ouble = . after 15 digit, size of 8 byte   
7. **c**har = A-Z a-z 0-9 0-127ASCII, size of 2 byte   
8. **b**oolean = 0 1, size of depends on jvm   

Binary can be represent as adding "0b"   ex: int a = 0b011;  
Hexadecimel can be represnt as adding "0x" ex: int a = 0x2A;  

## Operators:  

|  Operators| Symbols  |  
|--|--|  
|Arithmetic Operator  |**+ - * / %**  |  
|Relational Operator  |**<, <=, >, >=, ==, !=**  |  
|Logical Operator  |**&&(AND), \|\| (OR), !(NOT)**  |  
|Assignment Operator  |**a += 4**  |  
|Inc and Dec Operator  |**a++,a--,++a,--a**  |  
|Conditional Operator  |**exp1? exp2: exp3;**  |  
|Bitwise Operator  |** &, <<, >>, >>>**  |  
|Special Operator  |**instanceof, (.)**  |  
|Unary Operator  |**~, !**  |    

```
int a=10; int b=-9;  
System.out.println(~a);//-11 (minus of total positive value which starts from 0)    
System.out.println(~b);//9 (positive of total minus, positive starts from 0)   
```  
Arithmetic operator order: System.out.println(10*10/5+3-1*4/2);  is 21  
Left shift operator: 10<<2 is 10\*2^2= 40   
Right shift operator: 10>>2 is 10/2^2= 2    , when negative number it will -2
Bitwise operator & : (a>1&b<3) second condition also been check, where && wont go to second condition   

### Static :  
create only one time, called without reference
1. static variable -     ```className.variableName;```
2. static method -    ```className.functionName();``` 
3. static import-       
4. static object -      ``` import static java.lang.System.out;```
5. static class - only nested class can be static
6. static block - ```static {}``` //execute while class get loaded
7. Instance block { } inside class, runs after static block & before constructor
-```class.forName(" ");``` executes static block & load class

### Final :  
assigned only once, mostly in constructor directly. cannot modify once it assigned  
1. final variable - cannot changed  ```final int maxSpeed =100;```
2. final method - cannot overriden 
3. final class - cannot extend, immutable   
Note: finalize() - called just before an object is garbage collected. overrides to dispose system resources, perform clean-up, minimize memory leaks.

### Typecasting:  
Convert one datatype to another
1. Implicit casting    
2. Explicit casting ```int a = (int) 3.14;	//3```   
Byte -> short -> int -> long -> float -> double  

### Array:    
Group of similar datatype ```int rajesh[]=new int[3];```   
int a[];  
int[] a;    
int[] a = new int[4];    
int[] a = new int[]{1,2,3,4};    
**Arrays Important methods**:   
Arrays.asList(arr);      
Arrays.sort(arr);   //use mergeosrt for object, and quick sort fro primitive datatype   
Arrays.sort(arr, new Comparator());    
Arrays.binarySearch(arr, searchValue);    
Arrays.binarySearch(arr, fromIndex, toIndex, searchValue);  
Arrays.compare(intArr, intArr1);    
Arrays.copyOf(arr, 10); //create new clone array, also with initial size   
Arrays.copyOfRange(intArr, 1, 3);   
Arrays.hashCode(arr);  //return hashcode  
Arrays.equals(arr1, arr2);    
Arrays.toString(arr);  //print array   
List<?> a = Lists.newArrayList(a);   


### String:  
- class represents sequence of char  
- implements Serializable, Comparable and CharSequence interfaces  

**String creation**:  
- String - by string literal 
- new String() - create new space from string pool  
- new String().intern() - used to return value from string pool     
- StringBuffer - mutable, thread safe  
- StringBuilder - mutable, no thread safe, efficient  

**String comparision**:  
- ```s1.equals(s2);```  check for each char are same or not   
- ```s1==s2;```  check address is same or not  
- ```s1.compareTo(s2);``` compare string lexicographically. ie <0,>0  

**String tokenizer**: break a string into tokens    
```
StringTokenizer st = new StringTokenizer("my name is raj");
while(st.hasMoreTokens()){st.nextToken(); } //prints //my //name //is //raj  
```

## Decisions making:
1. if(con){ exp1; }
2. if(con){ exp1; } else{ exp2; }
3. if(con){ exp1; }else if(condition2){ exp2; }else{ exp3; }
4. Tenary operator-condition ? expersion 1: expersion 2;

## Looping:
1. while(con){ body; }
2. do{ body }while(condition);
3. for(intialize counter;test condition;inc or dec counter){ body; }
4. switch(varible){case constant: operation; break;default: operation;break;}
5. break; 	//get out of loop
6. continue;	//back to continue next loop
7. continue loop_label;		loop_label;{exp}
8. goto label_name; 		label_name:{exp}
9. break label_name;		label_name:{exp}
10. For each loop(Datatype var: iterable)

## Wrapper class:  
 wrap around primitive datatype & give object appearence  
 **Advantages:**   
 - call by reference supports only in object
 - serialization supports object
 - collection framework
 - java util package
 - can use null value  

**Autoboxing:** primitive into wrapper- it uses cache value
``` 
int j=1;
Integer i = Integer.valueof(j);  or Integer i =j;
```

**Unboxing** : wrapper into primitive
 ```
 Integer i = new Integer(7);
 int = i.intValue();  or  int j=i;
 ```

## Generics:   
parameterized types  
Adv: 1.Type safety, 2.Typecast not needed, 3.Compilertime checking  
```
class MyGen<T>{  
	T obj;  
	void add(T obj){this.obj=obj;}  
	T get(){return obj;}  
}  
```

## Serialization : 
mechanism of writing obj into byte stream, implement serializable marker interface
```
FileOuputStream file = new FileOutputStream(filename);
ObjectOuputStream out = new ObjectOuputStream(file);
out.writeObject(object); out.close(); file.close();

FileInputStream file = new FileInputStream(filename);
ObjectInputStream in = new ObjectInputStream(file);
in.readObject();  //new object create 
```


---

## Exception handling:  
Unexpected event that terminate program
1. checked expception - ioexception, sqlexception  
2. unchecked exception - nullpointerexception  
3. error - OutOfMemory, StackOverFlow.  
```
try{
	throw new exception_name(“”);        
}
catch(exception e){ }
catch(arithmeticException|Exception e){} //this is multicatch
finally{}// occur for sure even though exception handled or not.
```
**Throws** :  indicates caller functions of that method  to handling that exception.  void methodName throws Exception{ }

**Custom Exception class**
```
class InvalidAgeException extends Exception{  
 InvalidAgeException(String s){  
  super(s);  
 }  
}  
```
**Try with resources:**   resource is as an object that must be closed after finishing the program  
```
try(FileOutputStream fileOutputStream=new FileOutputStream("/home/irfan/scala-workspace/java7-new-features/src/abc.txt")){  
    // -----------------------------Code to write data into file--------------------------------------------//  
        String msg = "Welcome to javaTpoint!";      
        byte byteArray[] = msg.getBytes();  // Converting string into byte array      
        fileOutputStream.write(byteArray);  // Writing  data into file  
        System.out.println("Data written successfully!");  
}catch(Exception exception){  
       System.out.println(exception);  
}  
finally{  
       System.out.println("Finally executes after closing of declared resources.");  
}  
```  
NoClassDefFoundError: runtime, classfile missing at run time. 
ClassNotFoundException: runtime, try to load the class while Class.forName() or loadClass()     

---

## Annotations:
1. Built-In Java Annotations used in Java code
 - @Override
 - @SuppressWarnings
 - @Deprecated
2. Built-In Java Annotations used in other annotations
 - @Target
 - @Retention
 - @Inherited
 - @Documented - ensure class is available in javadoc

## Regex:    
**^[a-zA-Z][a-zA-Z0-9]{8,19}**  
Where  
^ represents the start of the regex   
[a-zA-Z] represents that the first character must be an alphabet  
[a-zA-Z0-9] represents the alphanumeric character  
{8,19} represents that the length of the password must be in between 8 and 20.
```
import java.util.regex.*;  
System.out.println(Pattern.matches(".s", "as")); //line 4  
```
