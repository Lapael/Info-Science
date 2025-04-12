# Info-Science

---

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
- **Q6076 ~ Q6098** 완료 → CodeUp 기초 100제 전부 해결
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

### 🔹 느낀 점
- 고등학교 1학년 때까지만 해도 단순히 정답 도출만이 목적이었지만,ㅇ 이제는 **시간복잡도와 메모리 효율성까지 고려하는 사고**가 자연스러워짐
- 실력의 향상과 함께 **프로그래밍적 사고력**도 함께 발전 중임을 체감

---

## Day 4

### 🔹 백준 문제 풀이
- **10021 Watering the Fields (USACO - Silver)** 문제 풀이
  - 유클리드 거리의 제곱값이 **C** 이상인 경우의 선분만 채택
  - 유효한 선분들이 모든 점을 이을 때, 유클리드 거리의 제곱값의 합이 최소인 경우 탐색

### 🔹 문제 해결 과정에서의 실패 요인

#### ❌ 외부 라이브러리 불허
- 연산 속도, 구조의 단순화를 위해 **numpy**를 사용했으나
- 백준은 외부 라이브러리를 허용하지 않아 컴파일 에러 발생
- **추후 해결 필요**

### 🔹 선형 자료
- 선형 자료란 자료를 구성하는 **원소들을 하나씩 순차적으로 나열시킨 형태**
- `array, list, stack, queue, deque`등이 이에 해당됨
- 기존에 알고 있던 선형/비선형에 대한 지식이 보완됨

### 🔹 객체
- **Class & Object**
- **Class**란 객체를 만드는 설계도 같은 것
- **Object**는 실제 인스턴스
- **체스봇 강화학습 프로젝트**에서도 **Class**를 사용함
- 체스는 흑과 백이 동일한 기능을 가지는 대칭적 구조의 **제로섬 게임**이기에 **Class**가 필수적
- 각 기물에 따른 `Move Class`, 게임 전체 상태 종합하는 `GameState Class` 등을 흑/백에 할당하여 설정
- 즉 여기서 흑/백은 **Class**로 찍어낸 **Object**가 됨

### 🔹 Computer Vision
- Computer가 image 혹은 video를 처리하는 방법
- **Object Detection**, **Image Classification** 등이 이에 해당됨
- 2024년에 **싱가포르 해외연수**를 떠나 Computer Vision 계열 **AI**들을 만들어 본 기억 덕분에 쉬웠음
- 수업시간에 활용한 **얼굴 인식 예제**는 사전학습된 모델을 사용하여 얼굴을 인식함

---
