# **Info-Science**

## **Day - 1**
### 기초 설명
#####   &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;연산자, 자료형, 변수 등 Python의 기초 지식 설명
##### &nbsp;
### CodeUp 문제 풀이
#####   &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Q6001 - Q6075 Clear
#####   &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Q6046 - Q6047, Q6059 - Q6062 의 비트시프트, 비트단위논리연산이 인상깊었다.
#####   &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;컴퓨터가 수를 저장하는 체계인 2진수를 통해 10진수에서는 보이지 않는 성질을 알 수 있었다.
#####   &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;또한 컴퓨터가 직접 이해하는 수를 이용해 계산을 하니 연산 시간이 더욱 짧아진 것을 알 수 있었다.

## &nbsp;

## **Day - 2**
### 기초 설명
#####   &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;비트시프트 연산, 아스키코드, 진법 등 기초 지식 설명
##### &nbsp;
### CodeUp 문제 풀이
#####   &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Q6076 - Q6098 Clear CodeUp 기초 100제 모두 해결
#####   &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Q6097, Q6098 의 설탕과자 뽑기, 성실한 개미 문제가 인상깊었다.
#####   &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;이중 리스트를 좌표 평면으로 설정한 뒤. 좌표값을 지정할 때 수학에서는 (x, y)를 지정한 것이
#####   &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;이중 리스트에서는 (y, x)로 대응되기에 약간의 오류가 있었지만 재미있게 풀었다.
#####   &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;이번 과정을 통해 이중 리스트를 더욱 더 원활히 다룰 수 있게 된 것 같다.

##

## **Day - 3**
### 백준 문제 풀이
#####   &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;15591번: MooTube (USACO - Silver) 해결
#####   &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;영상과 영상 사이의 유사도를 지정, 어떤 영상을 보고 있을 때, 그 영상과 다른 영상들 중 유사도가 어떤 기준값 K보다 크다면 그 영상을 추천한다.
#####   &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;이 과정을 반복하여 추천해줄 수 있는 영상의 수를 계산하여 추천
##### &nbsp;
#### 이 과정에서 겪은 오류들 : 얕은 복사, 깊은 복사, 메모리 초과
#####   &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;파이썬은 객체 지향 프로그래밍이기 때문에 list를 함수같은 지역 변수를 사용하는 부분에서 불러올 때, 전역 변수로 처리된다.
#####   &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;이로 인해 배열을 복사할 때 기본적으로 얕은 복사가 된다. 이로 인해 배열의 어떤 부분을 변경해도 다른 배열의 어떤 부분이 변경될 수 있다.
#####   &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;이러한 파이썬의 특징으로 인해 함수에서 list를 불러오고 이 리스트를 수정하는 과정에서 불러온 원본 list 또한 수정된다는 문제가 발생했다.
#####   &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;이를 해결하기 위해 함수에서 list를 불러올 때 깊은 복사 처리를 하여 완전히 독립된 새로운 list를 만드는 형식으로 수정해 문제를 해결할 수 있었다.
#####   &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;하지만 백준에서 걸어둔 메모리 제한으로 인해 재귀를 사용하는 나의 코드는 메모리 초과로 인한 오류를 낳았다.
#####   &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;이를 해결하기 위해 defaultdict와 deque를 사용하였다.
#####   &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;defaultdict를 통해 저장하지 않은 값은 설정하지 않아 코드의 크기를 줄이고 deque를 이용해 배열의 왼쪽부터 처리해 시간복잡도를 Q(N)을 Q(1)로 줄일 수 있었다.
#####   &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
#####   &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
