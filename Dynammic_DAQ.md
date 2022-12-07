### Dynammic Programming

***
피보나치 수열을 예를 들면 값을 구하는 데에 여러 중복된 계산이 많을 것이다.
그럴때 중복된 부분을 메모이제이션 (TOP-DOWN) 을 사용해 저장을 해두어 불필요한 계산은 하지 않게 한다.

* Memoization(메모이제이션) : 프로그램 실행 시 이전에 계산한 값을 저장하고, 이를 이용해 중복 계산을 하지 않고 전체 실행 속도를 빠르게 하는 기술.

* 상향식 접근법 : 가장 최하위의 해답을 구한 후, 이를 저장해 해당 결과값으로 상위 문제를 푸는 방식
  
```
(작은것)(작은것)(큰것)(좀더큰것)
1. (작은것),(작은것) ==> 결과1
2. 결과,(큰것) ==> 결과2
3. 결과2,(좀더큰것) ==> 결과3
```

### Divide and Conquer

***
문제를 가장 작은 사례로 나누고, 각각을 푼 다음(하향식 접근법) 합병하여 문제의 답을 얻는 알고리즘입니다. 일반적으로 재귀함수로 주로 구현(재귀함수를 사용하지 않고, 스택이나 큐를 사용하기도 함)하며, 분할 정복 알고리즘에는 병합 정렬과 퀵 정렬이 있습니다.

분할정복의 단점으로는 스택에 다양한 데이터를 보관해야 하므로 스택 오버플로우가 발생하거나, 과도한 메모리를 사용하게 된다는 점이 있습니다.

* 하향식 접근법 : 상위의 답을 구하기 위해 아래로 내려가면서 하위의 해답을 구하는 방식

### Knapsack problem

https://gsmesie692.tistory.com/113

Q. How to improve the time complexity of standard dynamic programming algorithm for 0-1 Knapsack problem

The algorithm can be improved so that the worst-case number of entries
computed is in Θ(2^n). With this improvement, it never performs worse than the
brute-force algorithm and often performs much better. The improvement is
based on the fact that it is not necessary to determine the entries in the ith row
for every w between 1 and W. Rather, in the nth row we need only determine P
[n] [W]. Therefore, the only entries needed in the (n − 1)st row are the ones
needed to compute P [n] [W]  -- page 246 text book

