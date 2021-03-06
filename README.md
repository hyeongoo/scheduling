# 202001604 강현구 scheduling 과제

## 출력결과

![스케쥴링 4결과](C:\Users\82104\Desktop\스케쥴링 4결과.PNG)

![스케쥴링 8결과](C:\Users\82104\Desktop\스케쥴링 8결과.PNG)

![스케쥴링 16결과](C:\Users\82104\Desktop\스케쥴링 16결과.PNG)

## 시간복잡도

n개의 작업을 배정하고, 배열 L을 탐색해야하므로 n x O(m) + O(m) = O(nm)이다.

따라서 작업이 4, 8, 16일 때 각각의 시간복잡도는 O(8), O(16), O(32)이다.

반면에, 무작위 대입(bruteforce)방법을 사용하면 기계에 작업을 배정하는 모든 경우의 수를 살펴봐야 하기 때문에 시간복잡도는 O(n^m)이다.

따라서 작업이 4, 8, 16일 때 각각의 시간복잡도는 O(16), O(64), O(256)이다.

## 근사비율

알고리즘의 근사해를 OPT-라 하고 최적해를 OPT라고 할 때, OPT/OPT-는 각각 2, 0.25, 0.125이다.

따라서 OPT-<=2xOPT가 성립한다.

