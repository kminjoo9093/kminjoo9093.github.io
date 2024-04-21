---
layout: single
title: "[자바스크립트_개념정리] 옵셔널 체이닝 문법 '?'"
typora-root-url: ../
---



중첩된 객체에서 값을 불러올 때 중간 속성이 없는 경우 옵셔널 체이닝 문법을 통해 에러없이 접근할 수 있다



<img src="/images/2024-04-18-optional_chaining/image-20240418183132227.png" alt="image-20240418183132227" style="zoom:50%;" />

=> 객체의 값을 불러오는데 중간에 unkown이라는 이름의 속성은 없기 때문에 에러가 떴다

<br>

이러한 에러를 막기 위한 방법으로 옵셔널 체이닝 문법을 쓴다

<img src="/images/2024-04-18-optional_chaining/image-20240418184927246.png" alt="image-20240418184927246" style="zoom:50%;" />

=> unkown뒤에 ' ? ' 를 쓰면 unkown이라는 객체가 있으면 그 안의 first를 반환하고,

unkown이라는 객체가 없으면 undefined를 반환한다

=> 물음표'?'를 써서 오류를 막을 수 있다

<br>

이 문법은 메서드, 배열 앞에서도 쓸 수 있다.

배열 앞에 쓸 때에는 '?'와 함께 '.'을 같이 찍어준다

<img src="/images/2024-04-18-optional_chaining/image-20240418185540119.png" alt="image-20240418185540119" style="zoom:50%;" />