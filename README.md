# algorithm
내가 푼 알고리즘 문제
# kim-yunsoo
[![Solved.ac Profile](http://mazassumnida.wtf/api/v2/generate_badge?boj=doradorav)](https://solved.ac/doradorav/)

<img width="728" alt="스크린샷 2022-11-27 오후 3 19 39" src="https://user-images.githubusercontent.com/68580993/204122113-389c5791-cfb3-441f-98ea-7ee3549d3b42.png">


이진검색트리-
 왼쪽 서브트리<부모노드<오른쪽 서브트리
 모든연산 erase insert find update->O(lgN)
 원소의 대소구분가능
 이진검색트리는 편향되지않으므로 좋다..->자가균형트리가 균형을 맞춰줌
 STL->set multiset map
 set map 항상 O(N) vs unordered set unorderd map O(1) 최악은 충돌때문에 O(N)

힙사용-우선순위로 원소 나열
우선순위큐(디폴트 최대힙): 원소의 추가 O(lgN) 우선순위 가장높은원소 조회O(1) /삭제O(lgN)
 최소힙 부모<자식 최대힙 부모>자식 위에서부터 순서대로 원소 나열
 루트를 제거하는경우 밑 원소와 위치를 바꾸며 내려가며 자리정돈O(lgN)
 
 이진검색트리 vs 힙
  공통점 둘다 이진트리
  차이점 힙은 최대/최소 찾기에 편헌 구조 이진검색트리는 특정 트리를 빠르게 탐색가능한 구조
  이진검색트리보다 힙이 더빠르고 공간도적게차지
 ->이진검색트리는 불균형 생길때 처리해주는 과정상 오버헤드 발생 힙은 자체가 불균형이없음

 그래프-
  정점(Vertex/Node)+간선(degree)
  무방향/방향그래프
  순환/비순환그래프
  완전/연결그래프

  인접행렬
  공간복잡도O(V^2) 
  두정점이 연결되어있는지 여부:시간복잡도O(1)
  정점 v에 연결된 모든정점 확인:O(V)
  정점이 적을때 E가 V^2에 가까울때
  -인접행렬로 정점을 행렬로 나타낼수있다 0,1로 간선이 있는지 표현

  인접리스트
  공간복잡도O(V+E)
  두정점이 연결되어있는지 여부:시간복잡도O(min(deg(u),deg(v)))
  정점 v에 연결된 모든정점 확인:O(deg(v))
  간선이 적을때 E가 V^2보다 훨씬 적을때
  -인접리스트 V개의 리트를 만들어 연결된 정점을 넣어줌

  BFS-O(V+E)
  DFS-O(V+E)

트리-
  무방향이면서 사이클이 없는 연결그래프
  정점 V 간선 V-1
  이진 트리-> 레벨순회(높이 순 순회) 전위 중위 후위  

위상정렬-
  방향 그래프서 간선으로 주어진 정점간 선후관게를 위배하지 않도록 나열하는 정렬
  ex)선수과목 (순서가 정해져있는경우)
  그래프에 사이클이있으면 안된다!-> 방향그래프지만 사이클은 x 

  구현방법: indegree가 하나도 없는게 시작점 =0 
  outdegree가 하나도 없는게 종료지점
  시작점에서 이어진 위치로 이동하며 indegree가 없는 간선을 하나씩 제거한다.
  각 정점의 indegree값을 저장했다가 1씩 간선을 지울때마다 감소 0일때 큐에 넣어 연산.
  사이클이라면? indegree가 0인게 없어서 큐에 넣을게 없다
  시간복잡도 O(V+E)


