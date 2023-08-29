#Arrays # sort #lambda

java.util.Arrays;
===================
Arrays method provide Array sort, search, compare
all method is static method, so you can use this Arrays class

## Arrays.sort 
-> literally u can sort the array as a ascendind order

## Arrays + Collections
if u use arrays.sort method, then u can sort the array a ascendtind order
but if u wannner sort the method as a desending order, then u need more method

*this is the way to sort the array as descending order

```java
int [] arr = {10,20,30,40,23};
Integer[] arr2 = Arrays.stream(arr).boxed().toArray(Integer[]::new);
Arrays.sort(arr2, Collections.reverseOrder());

for(int desc : arr2){
system.out.println(desc+" ");
}
```
## Arrays + lambda Expressions
what is lambda?
-> its the concept in programming, it a word refers to an anonymous function
-> lambda dosent need name

#### lamba's expressions
-> lambda can be used as a function body of the parameter (->)
-> if function body were single sentence, the you can skip the []

```java
new Thread(new Runnable() {
   @Override
   public void run() { 
      System.out.println("Welcome Heejin blog"); 
   }
}).start();

public int sum(int a, int b) {
	return a + b;
}
```


```java
new Thread(()->{
      System.out.println("Welcome Heejin blog");
}).start();


(int a, int b) -> {return a + b;}
```

we can express Comparator method as a lambda express
```java
Arrays.sort(arr, new Comparator<int[]>() {		
	@Override
	public int compare(int[] e1, int[] e2) {
		if(e1[0] == e2[0]) {		// 첫번째 원소가 같다면 두 번째 원소끼리 비교
			return e1[1] - e2[1];
		}
		else {
			return e1[0] - e2[0];
		}
	}
});
```
this part can skip by this expression

```java
Arrays.sort(arr, (e1, e2) -> {
	if(e1[0] == e2[0]) {
		return e1[1] - e2[1];
	}
	else {
		return e1[0] - e2[0];
	}
});
```
java.util.Set;
===================

element couldn't be duplicated(repeated)

set might have order

set might be array


# java.util.HashSet
	```java
	set<String>set = new HashSet<String>();
	set.add("1");

	for(Iterator i = set.iterator(); i.hasNext();){
	system.out.println(i.next());
	}

# java.util.Iterator

java.util.Comparator<T>
======================

## Comparator

Comparator is interface. so you must embody method that is declare at the interface

```java
Comparator<T> c= = new Comparator<T>(){
@override
	public int compare(T o1, T o2){
	return 0;
	}
}
```
## compareTo()
returns the coressponding int value by comparing the dictionary order value of the String array

```java
public void test(){ 
 
    String str1 = "AA"; 
 
    String str2 = "AA"; 
 
    String str3 = "BB"; 
 
    System.out.println(str1.compareTo(str2));  // 결과  0 
 
    System.out.println(str2.compareTo(str3));  // 결과 -1 
 
    System.out.println(str3.compareTo(str2));  // 결과  1 
 
}
```
 
## compare()
compare two paramater and return the result as  in type

```java
Comarator<T> c = new Comparator<T>(){
@override
	public int compar(T o1, To2){
	if(o1>o2){
	return 1;
	}

	else if(o1<o2){
	return -1;
	}

	else{
	return 0;
	}
}
```

```java
Arrays.sort(arr, new Comparator<String>() {
	public int compare(String s1, String s2) {
		// 단어 길이가 같을 경우 
		if (s1.length() == s2.length()) {
			return s1.compareTo(s2);
		} 
		// 그 외의 경우 
		else {
			return s1.length() - s2.length();
		}
	}
});
