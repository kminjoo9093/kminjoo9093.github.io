---
layout: single
title: "[자바스크립트_개념정리] 조건부 연산자"
typora-root-url: ../
---





조건부 연산자 (삼항 연산자)

코드를 더 간결하게 작성할 수 있음



[ syntax ]

```javascript
조건식 ? 참일 때 실행되는 식 : 거짓일 때 실행되는 식

// ? 와 : 을 기준으로 세 덩어리로 나뉨
```







<img src="/images/2024-04-16-conditional_operator/image-20240416225508582.png" alt="image-20240416225508582" style="zoom:50%;" />

=> 3은 0보다 크기 때문에 조건식이 거짓임으로 위와 같은 값이 나옴



[if문과의 비교]

<img src="/images/2024-04-16-conditional_operator/image-20240416230223647.png" alt="image-20240416230223647" style="zoom:50%;" />

=> 변수 선언과 조건식들을 한 줄에 작성하는 조건부 연사자와 달리\

If문은 변수를 따로 선언하고, 조건문도 여러 줄에 걸쳐 작성해야 함