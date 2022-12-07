 미로 찾기를 한다고 해보자. 복잡한 미로속에서 어느길이 진짜인지 찾으려면 출구가 나올 때까지 모든 길을 다 가보는 수 밖에는 없다. 만약 각 분기점 별로 이 길이 막혀있는 길인지 알 수만 있다면 상당히 편할 것이다. Backtracking이 하는 일이 바로 이것이다.

​
 0-1 Knapsack problem에서 최악의 경우는 지수승의 시간이 든다. 오랜 세월 동안 최악의 시간을 피하는 방법을 알아보았으나 구하지 못했다. 반대로 최악의 경우를 피할 수 없음도 증명하지 못했기 때문에 희망은 있다. Backtracking의 경우 이런 문제를 계산하는데 도움을 주어서 쓸모없는 작업을 하지 않도록 해주는 것이다. 물론 모든 경우에 해당되는 것이 아니라, 어느 정도 많은 경우에만 Backtracking 기술은 유효하다.

 ### Backtracking

 ***
 DFS 또는 그와 유사한 스타일의 탐색을 총칭
 가능한 지점까지 탐색하다가 막히면 다시 전단계로 되돌아온다.

 ### DFS 슈도
 ```
 // DFS - pseudo code
    // 1. 시작할 노드를 스택에 push 한다.
    // 2. 스택에서 노드를 하나 pop한다.
    // 3. If pop한 노드와 인접한 노드가 있는 지 확인한다.
        // 3-1. pop한 노드와 인접한 노드를 스택에 push한다. (이미 push/pop 했던 노드는 push하지 않는다.)
    // 4. else pop한 노드를 출력한다.
    // 5. 2번부터 Queue가 비워질 때 까지 반복한다.
```

 1. 상태공간트리 (State Space Tree Search)는 문제 해결 과정의 중간 상태들을 모두 Node로 구현해놓은 트리이다.
 2. 상태 공간 트리의 Leaf Node는 해당 문제의 해(Solution)에 해당된다.
 3. Optimum(최적해)는 Leaf Node 어딘가에 위치해 있고, 이를 효율적으로 찾아내는 것이 이 포스트의 주요 이슈이다.

### 백트래킹과 DFS의 차이
백트래킹이랑 DFS(Depth First Search) 모두 탐색하는 알고리즘이라 혼동하기 쉽다. 탐색이란 많은 양의 데이터 중에서 원하는 데이터를 찾는 과정을 의미한다. 백트래킹이랑 DFS 모두 원하는 값을 찾기 위해서 다양한 방법을 사용하는데 여기에서 차이가 발생한다. 


우선 백트래킹은 불필요한 탐색을 하지 않는다. 여기 a라는 배열이 있다. a는 132, 234, 123, 총 3개의 요소를 가지고 있는데, 123이라는 값을 찾고 있다고 하자. 순서대로 132라는 값에 접근했을 때, 백의 자리 수가 동일하나, 십의 자리 수가 다르기 때문에 더 이상 탐색을 진행하지 않고 다음 수로 넘어간다. 


그러나 DFS는 모든 경우의 수를 탐색한다. 다시 위의 예를 빌려, 132이라는 수를 탐색할 때, 십의 자리 수에 접근했을 때 원하는 수가 아님에도 불구하고 일의 자리 수까지, 즉 트리의 바닥에 도달할 때까지 탐색을 계속한다. 

```
 A preorder
tree traversal is a depth-first search of the tree. This means that the root is
visited first, and a visit to a node is followed immediately by visits to all
descendants of the node. Although a depth-first search does not require that the
children be visited in any particular order, we will visit the children of a node
from left to right in the applications
```
Solution
https://itdexter.tistory.com/86

즉, 백트래킹은 트리 구조를 기반으로 DFS 방식을 진행하면서 각 루트에 대해 조건에 부합했는지 체크(Promising).
만약 해당 트리에서 조건에 맞지 않는 노드를 발견한다면, 더 이상 탐색을 멈추고, 다른 노드로 가지를 침(Pruning).

### 백트래킹을 이용한 n-queen
https://jayce-with.tistory.com/17

### 백트래킹을 이용한 Sum of Subsets
https://scshim.tistory.com/entry/%EC%95%8C%EA%B3%A0%EB%A6%AC%EC%A6%98-%EB%B0%B1%ED%8A%B8%EB%9E%98%ED%82%B9-%EB%AC%B8%EC%A0%9C-Sum-of-Subsets

### 백트래킹을 이용한 Knapsack 0-1



### BRANCH AND BOUND 링크

https://hcr3066.tistory.com/29




