## 문제

Q1. Hash table 이 무엇인지에 대해서 설명해주세요.

## 정답

<details><summary>Q1. 답</summary>
<pre>
Hash function 으로 나온 값
즉, Hash value 는 보통 index 로 사용됩니다.

index 로 사용되는 이유는 접근의 시간복잡도를 최소화 하기 위함입니다.
Hash value 를 생성하는데를 제외하고 충돌이 일어나지 않는 상황을 가정한다면, O(1) 에 접근이 가능합니다.

하지만 충돌이 나는 상황에서는 어떤 방법을 적용해야 효율적인지는 상황에 알맞게 적용해야 됩니다.

--- 요약 ---

1. Hash table 은 최대한 빠른 삽입, 조회, 삭제를 위해서 사용한다.
2. Hash function 에서의 나온 값(Hash value) 를 통해서 index 에 접근한다.
3. 배열을 미리 만들어서 사용하기 때문에 메모리를 많이 사용할 수 있다.
   </pre>
   </details>
