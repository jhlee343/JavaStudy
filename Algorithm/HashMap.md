## HashMap
### HashpMap declare
  ```java
    HashMap<String,String> map1 = new HashMap<String,String>();//HashMap생성
    HashMap<String,String> map2 = new HashMap<>();//new에서 타입 파라미터 생략가능
    HashMap<String,String> map3 = new HashMap<>(map1);//map1의 모든 값을 가진 HashMap생성
    HashMap<String,String> map4 = new HashMap<>(10);//초기 용량(capacity)지정
    HashMap<String,String> map5 = new HashMap<>(10, 0.7f);//초기 capacity,load factor지정
    HashMap<String,String> map6 = new HashMap<String,String>(){{//초기값 지정
  ```

### add value
  ```java
  map.put(1,"apple");
  ```

### remove value
```java
  map.remove(1);
  map.clear();
```

### getOrDefault(Object key, V DefaultValue)
- this method allow two parameter
- originally, if u add the same key value in hashmap, the value is overwritten, so if you hope to contain the value, use getOrDefault method
  ```java
		String [] alphabet = { "A", "B", "C" ,"A"};
		HashMap<String, Integer> hm = new HashMap<>();
		for(String key : alphabet){
     hm.put(key, hm.getOrDefault(key, 0) + 1);
    }
		System.out.println("결과 : " + hm);
        	// {A=2, B=1, C=1}
	}
}
  ```
