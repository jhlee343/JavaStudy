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
