# Deque(double-ended queue)

- you can insert, remove element in both side
- faster than list, safe in thread enviroment
- ex) list's pop method => o(N) / deuqeu's pop method => o(1)
- use push, pop often then deque is better than list

### declare
```java
Deque<Integer> deque = new Deque<>();
deque.addFirst();
deque.addLast();

deque.pollFirst();
deque.pollLast();

deque.peekFirst();
deque.peekLast();
```
