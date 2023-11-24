## How to get Divior(약수 구하기)
### usual way (worst case)

  ```java
  for(int i =0 ; i<N ; i++){
    if(N%i==0){
      count++;
    }
}
```
### better way
```java
for(int i =0 ; i*i<N; i++){
  if(i*i=N) count ++;
  else if(N%i==0) count+=2;
```

o(n) => o(Math.sqrt(n))
