How to determine the lower bounds of all algorithms that search a given key k in an array A[1..n] using only key comparison and key copy operation ?

키 비교 및 키 복사 작업만 사용하여 배열 A[1..n]에서 주어진 키 k를 검색하는 모든 알고리즘의 하한을 결정하는 방법은 무엇입니까?

답 : binary search tree
정렬된 배열에서의 이진탐색 시간복잡도는 logN
Its worst-case time complexity is 𝒍𝒐𝒈𝒏.

• Question: if we limit ourselves to algorithms that
search only by comparisons of keys, can we develop a
better algorithm than 𝒍𝒐𝒈𝒏(binary Search) )?

• Answer : NO, because the lower bound of the search
problem is 𝛀(𝒍𝒐𝒈𝒏) as we study in the next slides.

이진트리 시간복잡도 증명
https://velog.io/@xdfc1745/%EC%9D%B4%EC%A7%84%ED%8A%B8%EB%A6%AC-%EC%8B%9C%EA%B0%84%EB%B3%B5%EC%9E%A1%EB%8F%84

이진트리 삽입, 선택
https://velog.io/@haero_kim/%EC%9D%B4%EC%A7%84-%ED%83%90%EC%83%89-%ED%8A%B8%EB%A6%AC-Binary-Search-Tree

https://ha-young.github.io/2020/data-structrue/2020-09-22-%EC%9E%90%EB%A3%8C%EA%B5%AC%EC%A1%B0-Tree%EC%97%90-%EB%8C%80%ED%95%B4-%EC%95%8C%EC%95%84%EB%B3%B4%EC%9E%90---1-%ED%8A%B8%EB%A6%AC,%EC%9D%B4%EC%A7%84%ED%83%90%EC%83%89%ED%8A%B8%EB%A6%AC/



