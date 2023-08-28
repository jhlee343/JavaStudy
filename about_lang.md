# String

### Declaration String
  String a = "Jhlee 343"
  String b = "Java"
  String c = "Study"
  
### Declar String Array
  String [] st= new String[n]
  String [] st = { , , , , ,}

### charAt()
  ##Declar of String
 ```java
 String str = new String90
  str = "hello"
  char c = ' '
  c = str.charAt(0)
  System.out.println(c)
```  
  >> h
    if you want to add sequential number to 1-5 using String
    total += Str.charAt(i) -'0'
    
###  ASKII code
  alpabet -> number
  
  scanner sc = new scanner(System.in)
  int ch = sc.next().charAt(0)
  or
  char ch =sc.nect().charAt(0)
  int num = (int)ch
  
### indexOf()
    
 if you find specific string or char, return that char value.
if you couldnt find it then return value -1
    
indexOf(String s)
indexOOf(int i)

    ```java
    String s= "hell"
    for(char ch='a'; ch<='z'; a++){
     system.out.print(s.indexOf(c)"" ");
  
  > -1 -1 -1 -1 1 -1 -1 0 -1 -1 -1 2 -1 -1 4 -1 -1 -1 -1 -1 -1 -1 -1 -1 -1 -1 
  
  ### how to fins string's length ?
    ```java
    String s = "hello"
    int s_len = s.length();
    
    if you use for sentence with String , 
    
    Scanner sc = new Scammer(System.in)
    int num = sc.nextint()
    String str = sc.next()
    
    for(int i=0; i<num ; i++){
      system.out.print(str)
    }
    ```
    is not correct
    
    for(int j =0 ; j<str.length() ; j++) {
					System.out.print(str);
			}
      
     is correct
    
    why?

### how to split String using java method
   1) String str = sc.nextline();
      String[] arr = st.split(" ");
   2) String tokens = new StringTokenizer(str, " ");
    
### tokens.countTokens() -> you can count blank in string sentence

### what is different between next() nextLine()
   next() => accept one world based on the blank space
   nextLine() => accept the entire sentence before typing a letter or enter button
   		you can bring whole sentence in buffer like ( /n /t )

### how to comvert String
use Stringbuffer
```java
    String str = "ABCED"
    StringBuffer sb = new StringBuffer(str);

    String reverse = sb.reverse().toString();
```

### String to int / int to String
    ```java
    String a = "123";
    int A = Integer.ParseInt(a);

    int b = "123";
    String B = Integer.toString(b);


# StringBuilder

## StringBuilder is much lighter than StringBuffer, so nomarlly we use StringBuilder
### append
u can append the char at the char array 

``` java
StringBuilder a = new StringBuilder("hello");
a.append("world");
```

### capacity()
 return the size about the array
 
 length() method is length of the string itself containing the acutal data  capacity() is the size of the current array
 
 if you resize the array like append() method , then array's size is automatically changed
