# Info-Science 클래스 기록

## Day 1

### 🔹 기초 개념 학습
- 연산자, 자료형, 변수 등 Python의 기초 개념 학습

### 🔹 CodeUp 문제 풀이
- **Q6001 ~ Q6075** 완료  
- 특히 **Q6046 ~ Q6047**, **Q6059 ~ Q6062**의 비트 시프트 및 비트 논리 연산이 인상 깊었음
- 컴퓨터가 수를 저장하는 방식인 2진수를 통해, 10진수에서는 보이지 않던 성질을 이해할 수 있었음
- 컴퓨터가 직접 이해하는 수 체계(2진수)를 이용한 계산을 통해 연산 속도가 빨라짐을 체감

---

## Day 2

### 🔹 기초 개념 학습
- 비트 시프트 연산, 아스키코드, 진법 등 심화 기초 학습

### 🔹 CodeUp 문제 풀이
- **Q6076 ~ Q6098** 완료 → CodeUp 기초 100제 전부 해결!
- **Q6097, Q6098**: 설탕과자 뽑기, 성실한 개미 문제 인상 깊음  
- 이중 리스트를 좌표 평면처럼 활용하며 좌표 처리
  - 수학에서의 (x, y)와는 다르게, 리스트에서는 (y, x) 순서로 사용
- 이로 인한 좌표 혼동도 있었지만, 문제를 통해 이중 리스트 활용 능력이 크게 향상됨

---

## Day 3

### 🔹 백준 문제 풀이
- **15591번 MooTube (USACO - Silver)** 문제 해결  
  - 영상 간 유사도를 기준으로 추천 영상을 계산하는 문제
  - 유사도가 기준값 **K** 이상인 영상을 탐색하고 추천 수를 계산

### 🔹 문제 해결 과정에서의 시행착오 및 배움

#### ✅ 얕은 복사 vs 깊은 복사
- 파이썬은 객체 지향 언어이므로 리스트를 함수에서 사용할 때 기본적으로 얕은 복사가 이루어짐
- 이로 인해 원본 리스트가 의도치 않게 수정되는 문제가 발생
- 해결 방법: `copy.deepcopy()`를 통해 깊은 복사 사용 → 독립된 리스트 생성

#### ✅ 메모리 초과 문제
- 재귀 구조로 인해 메모리 초과 발생  
- 해결 방법:
  - `defaultdict`로 초기화가 필요 없는 구조 설계 → 코드 크기 감소
  - `deque` 사용으로 시간 복잡도를 O(N) → O(1)로 최적화
  - BFS(너비 우선 탐색)를 deque로 구현하여 FIFO(선입선출) 처리 → 효율적인 탐색 구현

#### ✅ 최적화 알고리즘에 대한 인사이트
- 예전에 진행했던 **체스봇 강화학습 프로젝트**에서 활용한 **Alpha-Beta Pruning** 기법과 유사한 개념을 BFS와 FIFO에서도 발견
- 복잡한 알고리즘일수록 연산량을 줄이는 **최적화 설계**가 필수적이라는 점을 실감
- 단순히 문제를 해결하는 것뿐 아니라, 성능을 고려한 설계가 중요해졌음을 느낄 수 있었음

---

## 느낀 점
- 고등학교 1학년 때까지만 해도 단순히 정답 도출만이 목적이었지만, 이제는 **시간복잡도와 메모리 효율성까지 고려하는 사고**가 자연스러워짐
- 실력의 향상과 함께 **프로그래밍적 사고력**도 함께 발전 중임을 체감
