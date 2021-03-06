
# [01] 세그먼트 트리 (Segment Tree)

[WHEN?] 여러 개의 데이터가 <b>연속적으로</b> 존재할 때 특정한 범위의 데이터 합을 구한다.
<br>
<b>[관련문제들]</b> <br>
1. [백준 P2042: 구간 합 구하기](../../Baekjoon/Gold1/구간-합-구하기)


## index
0. [개요](#-0.-개요)
1. [Brute-force로 구하기](#-1.-Brute-force로-구하기)
2. [트리 구조로 구하기](#-2.-트리-구조로-구하기)

-----------------------
## 0. 개요
   {1, 9, 3, 8, 4, 5, 5, 9, 10, 3, 4, 5}의 배열이 주어졌을 때, 인덱스 3 ~ 6까지 연속된 데이터의 합을 구해라.
  <br><br>

## 1. Brute-force로 구하기
   
   앞에서부터 하나씩 더해가므로 데이터의 개수가 N개라고 하면 시간 복잡도는 <b>O(N)</b>이 나온다. <br>
   뿐만 아니라 배열의 값이 변경되어 다시 구간 합을 구해야할 때, 탐색하며 합을 구했던 바뀌지 않은 요소들에 대해 다시 접근하므로 매우 비효율적이다.
   <br><br>

## 2. 트리 구조로 구하기
   
   세그먼트 트리는 이진 트리이다.<br>
   배열의 구간을 반씩 나누어 자식 노드가 그 나누어진 두 구간의 합을 갖는다. <br>
   따라서 시간 복잡도를 O(lgN)으로 줄일 수 있고, 트리 구조이기에 구현은 재귀적으로 하는 것이 간편하다.<br>
   공간복잡도는 배열의 길이가 N이라고 했을 때, O($2*(⌊lgN⌋^2)$)가 된다. <br>
   이유는 포화 이진 트리를 형성하고, 트리의 높이는 $⌊lgN⌋^2$ 이기 때문이다.

 

