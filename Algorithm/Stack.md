# Stack

## [stack java code](https://github.com/jhlee343/BaekjoonStudy/tree/main/%EB%B0%B1%EC%A4%80/Silver/10828.%E2%80%85%EC%8A%A4%ED%83%9D#silver-iv-%EC%8A%A4%ED%83%9D---10828)

It is a data structrue that stacking up data

Last in data , First out
for DFS

Stack use case :
  web broswer visit record
  undo
  make reverse char array
  prefix calculate

## Declare stack
 ```java
import java.util.Stack;

Stack<Integer> stackInt = new Stack<>();
```

## push(), pop() , clear()
```java
stackInt.push(1);
stackInt.push(2);

stackInt.pop();

stackInt.clear(); // delete all 
```
## empty()
check the stack's condition 
if it is empty , return true, else return false

## search()
```java
system.out.println(stackInt.search(2)
```
it search the element in stack and return that element's posisiton
if there were no element in stack, it return -1

## peak()
```java
stackInt.peek()
```
 return the last element int stack
 if stack is empty, a NoSuchElementException occurs when calling the peek() method
