## 문제

Q1. 1억건의 데이터를 현재는 한 번에 불러오고 있습니다. 어떻게 개선하면 좋을까요?

<details><summary>Q1. 답</summary>
<pre>
저는 서버 사양에 맞게 N건 씩 끊어서 불러올 것 같습니다.
offset, limit 활용.
</pre>
</details>
