## Dijkstra Algorithms

***
다익스트라 알고리즘은 하나의 정점에서 다른 모든 정점으로 가는 최단 거리를 구하는 알고리즘 입니다. A,B,C,D,E,F 노드가 있을 때 하나의 정점A를 기준으로 A-B, A-C, A-E ...까지의 최단거리를 구할 수 있습니다. 이전에 구한 값을 재사용한다는 의미에서 다이나믹프로그래밍, 항상 가장 짧은 거리의 노드를 선택한다는 점에서 그리디 알고리즘으로 분류하기도 합니다.

1. 출발 노드를 설정

2. 출발 노드를 기준으로 각 노드의 거리를 저장

3. 방문하지 않은 노드 중에서 가장 거리가 짧은 노드를 선택

4. 해당 노드를 거쳐가는 경우와 거쳐가지 않은 경우를 비교하여 최단거리 갱신

5. 3,4 과정을 반복

-- 선형탐색으로 구한 경우이며 시간복잡도는 O(N^2)
-- '힙'을 사용하게 되는데 이경우 시간복잡도는 O(NlogN)

출처:https://kosaf04pyh.tistory.com/316
출처:https://propercoding.tistory.com/111

## Floyd Warshall Algorithms

***
다익스트라 알고리즘의 경우 하나의 정점에서 모든 정점으로의 최단거리를 구하는 문제였다면 플로이드 와샬 문제는 '모든 정점에서 모든 정점으로의 최단거리'를 구하는 알고리즘 입니다.

-- 그림과 함께 설명이 필요해 링크를 걸어두겠다.

https://propercoding.tistory.com/109

이 그림에서 노드 1을 거치는 경우, 노드 2를 거치는 경우 쭉 해나아가면서 노란색이 칠해져있는 부분이 노드 1이 포함이 안되어있어 노드 1을 거쳐가면 새로 갱신이 될 수 있는 비용들인데, 생각해보면 저 노란 부분들이 왜 갱신될 수 있는 곳인지 알것이다. 1포함된 행 열 재외 자기자신 제외.

이 알고리즘의 시간 복잡도는 O(n^3)이다. n은 노드 개수를 뜻한다. 

```
public class Main {
    static int number = 4;  //노드의 개수
    static int INF = 1000000000;  //무한
    static int[][] arr = { //자료 배열 초기화
        {0, 5, INF, 8},
        {7, 0, 9, INF},
        {2, INF, 0, 4},
        {INF, INF, 3, 0},
    };

    // 플로이드 와샬 함수
    static void floydWarshall() {
        int[][] graph = new int[number][number];
        for (int i = 0; i < number; i++) {
            for (int j = 0; j < number; j++) {
                graph[i][j] = arr[i][j];
            }
        }
        
        for (int k = 0; k < number; k++) { // k = 거쳐가는 노드
            for (int i = 0; i < number; i++) { // i = 출발 노드
                for (int j = 0; j < number; j++) { // j = 도착 노드
                    if (graph[i][k] + graph[k][j] < graph[i][j]) {
                        // 노드 k를 거쳐가는 비용이 더 적으면 이 비용으로 갱신
                        graph[i][j] = graph[i][k] + graph[k][j];
                    }
                }
            }
        }
    }
}
```