---
layout: single
title: "[자바스크립트_개념정리] 화살표 함수 arrow functions"
typora-root-url: ../
---





> #### 화살표 함수 arrow functions



<span style="font-size:85%">function 키워드 없이 함수 입력이 가능함으로 기존의 함수나 함수 표현식보다 간결</span>

<span style="font-size:85%">화살표 함수 하나만 단독으로 만들 수는 없기에 변수에 저장한다</span>

<span style="font-size:85%">화살표 함수는 배열 메서드랑 항상 함께 쓰인다</span>

<br>

**<span style="font-size:90%">[ syntax ]</span>**

```javascript
const 변수명 = (매개변수) => {
  실행문;
}
```

<br>

<span style="font-size:90%; font-weight:bold">[ 화살표 함수 구문 연습 ]</span>

<img src="/images/2024-05-09-arrow functions/image-20240409123525143.png" alt="image-20240409123525143" style="zoom:50%;" />

<img src="/images/2024-05-09-arrow functions/image-20240409123555092.png" alt="image-20240409123555092" style="zoom:50%;" />

<br>

<span style="font-size:90%; font-weight:bold">[인수가 하나일 때]</span>



<img src="/images/2024-05-09-arrow functions/image-20240409140635315.png" alt="image-20240409140635315" style="zoom:50%;" />

<img src="/images/2024-05-09-arrow functions/image-20240409125723160.png" alt="image-20240409125723160" style="zoom:50%;" />

<span style="font-size:85%">=> 괄호 생략 가능</span>

<br>



<span style="font-size:90%; font-weight:bold">[ 인수가 없는 화살표 함수 ]</span>

<img src="/images/2024-05-09-arrow functions/image-20240409135828012.png" alt="image-20240409135828012" style="zoom:50%;" />

<img src="/images/2024-05-09-arrow functions/image-20240409135838871.png" alt="image-20240409135838871" style="zoom:50%;" />

<span style="font-size:85%">=> 괄호 안은 비워놔야 함. ( 결정할 매개변수, 인수가 없어도 그 자리는 필요하다 )</span>

<br>

<span style="font-size:80%; color:green; font-weight:bold">[ 깨알 개념 정리 ]</span>

<span style="font-size:75%; color:green">**매개변수(parameter)**는 함수를 정의할 때 사용되는 변수이고 </span>

<span style="font-size:75%; color:green">**인수(argument)**는 실제로 함수가 호출될 때 넘기는 변수값이다</span>

<br>



<span style="font-size:90%; font-weight:bold">[ 화살표 함수의 축약형 ( 암시적 반환 ) ]</span>

<span style="font-size:85%"> 1. return 생략 </span>

<span style="font-size:85%">이때 중괄호를 괄호로 바꿔야 하며 괄호 안에는 단 한개의 표현식만 있어야 함</span>

<img src="/images/2024-05-09-arrow functions/image-20240409145602902.png" alt="image-20240409145602902" style="zoom:50%;" />

<br>

<span style="font-size:85%"> 2. 한줄로 작성 </span>

<img src="/images/2024-05-09-arrow functions/image-20240409145708868.png" alt="image-20240409145708868" style="zoom:50%;" />



<br>

<br>



<span style="font-size:90%; font-weight:bold">[ 화살표 함수 활용한 forEach() 와 map() ]</span>



<span style="font-size:85%"> - map()와 화살표 함수</span>

<img src="/images/2024-05-09-arrow functions/image-20240409222041521.png" alt="image-20240409222041521" style="zoom:50%;" />

<img src="/images/2024-05-09-arrow functions/image-20240409222058590.png" alt="image-20240409222058590" style="zoom:50%;" />

<span style="font-size:85%">=> map()메서드에 function키워드의 함수를 넣는 대신 화살표 함수를 넣어 movieRates 에 저장</span>



<span style="font-size:85%">- 암시적 반환</span>

<img src="/images/2024-05-09-arrow functions/image-20240409222241277.png" alt="image-20240409222241277" style="zoom:50%;" />

<br><br>



<span style="font-size:85%">- forEach()와 화살표 함수</span>



<img src="/images/2024-05-09-arrow functions/image-20240409224617719.png" alt="image-20240409224617719" style="zoom:50%;" />

<img src="/images/2024-05-09-arrow functions/image-20240409224642283.png" alt="image-20240409224642283" style="zoom:50%;" />

<span style="font-size:85%; color:orangered">=> map메서드와 다르게 forEach메서드는 항상 undefined 를 반환한다. 때문에 console.log 를 사용해야 원하는 값을 출력한다</span>

<br>

<img src="/images/2024-05-09-arrow functions/image-20240409224324108.png" alt="image-20240409224324108" style="zoom:50%;" />

<img src="/images/2024-05-09-arrow functions/image-20240409224349112.png" alt="image-20240409224349112" style="zoom:50%;" />

<br>



<img src="/images/2024-05-09-arrow functions/image-20240409224411538.png" alt="image-20240409224411538" style="zoom:50%;" />

<img src="/images/2024-05-09-arrow functions/image-20240409224440947.png" alt="image-20240409224440947" style="zoom:50%;" />

<span style="font-size:85%">=> return 키워드와 다르게 console.log는 생략할 수 없다. </span>

   <span style="font-size:85%">  암시적 반환은 return을 생략했을 때 가능한 것으로</span>

​    <span style="font-size:85%">위 예시는 return 키워드가 생략된 것과 같은 의미임으로 undefined가 반환됨</span>

