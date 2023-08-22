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

```
int [] arr = {10,20,30,40,23};
Integer[] arr2 = Arrays.stream(arr).boxed().toArray(Integer[]::new);
Arrays.sort(arr2, Collections.reverseOrder());

for(int desc : arr2){
system.out.println(desc+" ");
}
```
