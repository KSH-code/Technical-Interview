## 문제

Q1. 초당 30 개의 Insert/Update/Delete 의 제한이 있는 DB 가 존재한다. 이 DB 는 로그 작성할때만 사용한다.

서비스 운영중 갑자기 초당 300 건의 요청이 오게되면 어떤 현상이 일어나고 해결 방법은 무엇인가?

<details><summary>Q1. 답</summary>
<pre>
Message queue 와 같은 곳에 데이터를 담아두고 초당 30 개씩 처리하는 로직을 작성한다. (로그는 즉시 작성되지 않아도 되기 때문이다.)
</pre>
</details>
