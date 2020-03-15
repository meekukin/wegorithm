## 트리 구조   
- 데이터를 순차적으로 나열시킨 선형구조와 달리, 데이터가 계층적 혹은 망구조로 되어있는 비선형 구조이다. 또한, 선형구조는 자료를 저장하고 꺼내는 것에 초점이 맞춰져있다면, 비선형구조는 '표현'에 초점이 맞춰져있다.   

### 용어
- Root Node : 트리 구조에서 최상위에 존재하는 A와 같은 노드
- Node : 트리의 구성요소에 해당하는 A,B,C,D,E,F,G,H,I,J와 같은 요소
- Edge : 노드와 노드를 연결하는 연결설
- Terminal Node(Leaf Node) : 밑으로 또 다른 노드가 연결되어 있지 않은 H,I,J,F,G와 같은 노드
- Sub-Tree : 큰 트리(전체)에 속하는 작은 트리
- Level : 트리에서 각 층별로 숫자를 매김
- Height : 트리의 최고 레벨 (3)

### 이진트리
- 부모 노드 밑에 자식 노드가 최대 2개밖에 오지 않는, 트리의 가장 간단한 형태다. 두 자식 노드를 보통 왼쪽 자식과 오른쪽 자식으로 구분지으며, 하나의 값과 왼쪽, 오른쪽 자식 노드를 각각 가리킬 두 개의 포인터를 가진 구조로 구현할 수 있다.
- 일반적으로 n개의 자식을 가질 수 있는 트리 구조에서, 1개를 초과한 자식 하나마다 노드를 하나 추가해 추가된 새 노드의 왼쪽에 원래의 자식 노드, 오른쪽에 형제 노드를 배치 하는 이진 트리 구조로 변환할 수 있으며(Left-Child, Right-Sibling), 이 방법으로 모든 트리를 이진 트리 형태로 재구성할 수 있다(좌우를 바꾸어도 동일). 때문에 특별한 이유가 없는 이상 트리는 보통 이진 트리로 구현된다.

### 이진트리의 종류
- 정 이진 트리(full binary tree): 모든 트리의 자식은 0개나 2개다.
- 포화 이진 트리(perfect binary tree): 모든 리프 노드의 높이가 같다.
- 완전 이진 트리(complete binary tree): 모든 리프노드의 높이가 최대 1 차이가 나고, 모든 노드의 오른쪽 자식이 있으면 왼쪽 자식이 있는 이진트리이다. 다시 말해 트리의 원소를 왼쪽에서 오른쪽으로 하나씩 빠짐없이 채워나간 형태이다.

### 이진트리 순회방법
- 중위 순회(In-order traversal): 왼쪽 자손, 자신, 오른쪽 자손 순서로 방문하는 순회 방법. 이진 탐색 트리를 중위 순회하면 정렬된 결과를 얻을 수 있다.
- 전위 순회(Pre-order traversal): 자신, 왼쪽 자손, 오른쪽 자손 순서로 방문하는 순회 방법.
- 후위 순회(Post-order traversal): 왼쪽 자손, 오른쪽 자손, 자신 순서로 방문하는 순회 방법.
- 레벨 순서 순회(Level-order traversal): 너비 우선 순회(Breadth-First traversal)라고도 한다. 노드를 레벨 순서로 방문하는 순회 방법. 위의 세 가지 방법은 스택을 활용하여 구현할 수 있는 반면 레벨 순서 순회는 큐를 활용해 구현할 수 있다.

- 예시
![](/image/트리.png)
- In-order: 1 3 4 6 7 8 10 13 14
- Pre-order: 8 3 1 6 4 7 10 14 13
- Post-order: 1 4 7 6 3 13 14 10 8
- Level-order: 8 3 10 1 6 14 4 7 13
