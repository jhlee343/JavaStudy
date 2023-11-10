# 1. Floyd-Warshall Algorithm

## what is Floyd-Wahrshall Algorithm?
- the algorithm that find the shortest route at a whole
- it is slightly different from dijstra
- this algorithm run only one time and can find the shorest route

## the process
- configuration the dimenstion arry[2차원 행렬의 구성]
- every round at each route select the availabe second node
- select the short
- repeat
- INF means there's no route from node to specific node
- if u have 5 node thens 5 round, 3node? 3round

### round 1  
- set #1 node as a intermid node
- there no route between 2 and 4
- but set #1 node then can move 2-1-4
- update the distance

### round 2
- set #2 node as a intermid node

### source
```java
//reset the dist array using adj arr
for(int i =0 ; i<=n ; i++){
  for(int j =0 ; j<=n ; j++{
    if(i==j){dist[i][j]=0)
    else if(adf[i][j]){
        dist[i][j] = adj[i][j];
        }
    else dist[i][j] = INF;
    }
}
//k is the mid node's num
for(int k =0 ; k<=n  k++){
  for(int i =1 ; i<=n ; i++){
      for(int j =1 ; j<=n ; j++){
          dist[i][j]= min(dist[i][j], dist[i][k]+dist[k][j]);
      }
    }
  }
```
[excersice problem : programmers 합승택시 요금](https://school.programmers.co.kr/learn/courses/30/lessons/72413)
```java
//fares[][] => 2차원 배열 [n][3]짜리 배열이였음
 for(int[] edge : fares){
            dist[edge[0]][edge[1]] = edge[2];
            /*=> dist[fares[i][0]][[fares[i][1]] = fares[i][2]
                  fares 배열의 노드들 위치 복사해 온거네..*/
            dist[edge[1]][edge[0]] = edge[2];
        }
```

