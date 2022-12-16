Sorting time complexity
```
O(n²)

bubble sort

selection sort

insertion sort

quick sort(최악의 경우. 평균은 O(nlogn))
```

```
O(nlogn)

merge sort

heap sort
```
Decision tree를 가장 잘 이해시켜준다.
https://ict-nroo.tistory.com/57

Decision tree를 이용하여 Comparison sort의 시간복잡도를 증명한다.
https://youtu.be/5ep010tcJn4



O(nlogn)보다 시간복잡도가 더 낮은 comparison 정렬 알고리즘은 존재할 수 없다는 것이 이번 학습에서 얻을 수 있는 결론이다.

Why we study the theoretical lower bound of the time
complexity of all algorithms of a given problem?

어쨋든 우리는 더 나은 효율적인 알고리즘을 항상 원하지만 sorting computational problem 에서 only key comparsion 연산을 통해 더이상 발전할 수 없다는 것을 증명했다. 하한 보다 더 나은 시간복잡도를 가질 수 없다.

Any algorithm refers to all known algorithms
which are developed in the past or all unknown
algorithms that can be developed in the future to
solve the same computational problem.

What type of model is used to determine the lower bounds of
all algorithms that sort a given array A[1..n] using only key
comparison and key copy operations ? Why the model is
appropriate to do this task?

binary decision tree
Binary decision tree can model a sorting problem
and the execution of the sorting algorithm corresponds to a
path from the root to leaf nodes.




Group 1: Sorting algorithms that uses only key comparison
and key copy operations.
 They cannot do other operations.
 Examples: selection sort, bubble sort, insertion sort,
quicksort , heap sort, merge sort

Group 2: Sorting algorithms that uses other operations in
addition to key comparison and key copy operations.
 These algorithms can do arithmetic operation on keys,
 They can use key as index of arrays
 Examples: Bucket Sorting, Counting sort, Radix sort.


Counting sort , radix sort, bucket sort

https://youtu.be/Urmb0FpW6Hk

https://youtu.be/7heKwjqkY60

버킷 정렬 : 값을 비교하여 정렬하는 기법인 comparison sort의 계산복잡성은 최소 O(nlogn)입니다. 버킷 정렬은 분석 대상 데이터의 분포 특성을 활용해 계산복잡성을 O(n) 수준으로 개선시키려는 것을 목적으로 하고 있습니다. 버킷 정렬은 데이터가 특정 범위 내에 확률적으로 균등하게 분포한다고 가정할 수 있을 때 적용할 만한 기법입니다. 



***
문제
Question: Can we develop a new sorting
algorithm whose time complexity is better
than ϴ(nlogn) using only key comparison?
 Answer : No, because the lower bound of the
sorting problem is Ω(nlogn) which is equal to
the time complexity of merge sort algorithm
ϴ(nlogn).

Question: Suppose we designed a new algorithm that
takes T(n) to solve a given problem. Can we say that the
algorithm is the best possible algorithm?
 Case 1: Yes, if the worst-case time complexity of the
algorithm θ(T(n)) and the lower bound of the problem
Ω(T(n)) are the same.
 Case 2: No, if the two bounds are not the same.
