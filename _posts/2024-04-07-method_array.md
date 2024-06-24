---
layout: single
title: "[자바스크립트_개념정리] 배열 메서드 forEach(), map(), fill()"
typora-root-url: ../
---





## 배열 메서드

<br>



#### 배열 메서드 종류

**"  forEach()  &nbsp;/  map()  &nbsp; /   fill()  &nbsp; /  filter()  &nbsp; /  reduce()  &nbsp;/  some()  &nbsp;/  every()  &nbsp;/  find()   "**

<br>

<span style="font-size:85%">위 배열 메서드들은 **함수를 인수**로 받는다</span>

<span style="font-size:70%; color:orangered; font-weight:bold">* 콜백함수: 다른 함수의 매개변수로 전달되는 함수</span>



<br>

<br>

> #### forEach( )



<span style="font-size:85%">어떤 함수를 넣든 상관없이 배열의 각 요소가 차례로 함수로 자동으로 전달되어 함수를 한 번씩 실행한다.</span>

<span style="font-size:85%">배열의 요소에 대해 반복문 역할을 한다고 볼 수 있다.</span>

<span style="font-size:85%">For of 루프가 등장하고 forEach()를 많이 쓰진 않지만 </span>

<span style="font-size:85%; color: orangered">그럼에도 forEach()나 map()을 쓰는 이유는 배열 메서드를 쓰면 성능은 떨어질 수 있지만 연달아 쓰는게 가능하기 때문에 편리하다.</span>

<br>

**<span style="font-size:90%">[ syntax ]</span>**

```javascript
배열이름.forEach(function(element, index){
  실행문;
})

//함수를 인수로 받는 forEach메서드
```

<br>

<span style="font-size:90%; font-weight:bold">[ forEach() 구문 연습]</span>

<img src="/images/2024-04-07-method_array/image-20240408000340162.png" alt="image-20240408000340162" style="zoom:50%;" />

<img src="/images/2024-04-07-method_array/image-20240408000411309.png" alt="image-20240408000411309" style="zoom:50%;" />

<span style="font-size:85%">=> forEach메서드를 사용하는 일반적인 방식으로 <span style="color:orangered">forEach 메서드와 같은 줄에서 이 목적만을 위한 이름없는 함수를 정의</span></span>

  <span style="font-size:85%">  numbers 배열의 요소를 차례로 출력</span>

<br>

<span style="font-size:90%; font-weight:bold">[ For of 루프와 forEach 메서드 비교 ]</span>

<img src="/images/2024-04-07-method_array/image-20240408000551571.png" alt="image-20240408000551571" style="zoom:50%;" />

<span style="font-size:85%">=> 이후 for of 루프 사용으로 함수를 넣을 필요가 없어지고 더 간결해짐</span>

<br>



<span style="font-size:90%; font-weight:bold">[ forEach() 구문 연습 - 짝수 출력]</span>

<img src="/images/2024-04-07-method_array/image-20240408000901084.png" alt="image-20240408000901084" style="zoom:50%;" />

<img src="/images/2024-04-07-method_array/image-20240408000914318.png" alt="image-20240408000914318" style="zoom:50%;" />

<span style="font-size:85%">=> numbers 배열의 요소들 중 2로 나눴을때의 나머지가 0인 것을 조건으로 참인 요소만 출력</span>

   <span style="font-size:85%; color:orangered"> 함수의 매개변수 자리 (el)에 numbers 배열의 각 요소가 차례로 인수로 전달되어 함수가 실행됨</span>

<br>

<span style="font-size:90%; font-weight:bold">[ forEach() 활용 - 영화제목과 평점 출력]</span>

<img src="/images/2024-04-07-method_array/image-20240408001938153.png" alt="image-20240408001938153" style="zoom:50%;" />

<img src="/images/2024-04-07-method_array/image-20240408002019582.png" alt="image-20240408002019582" style="zoom:50%;" />

<span style="font-size:85%">=> 매개변수 movie 자리에 배열의 각 요소(여기서는 객체 리터럴)가 인수로 들어와 차례로 함수에 전달</span>



<br>

<span style="font-size:90%; font-weight:bold">[forEach메서드 밖에서 함수 정의하는 방법]</span>

<img src="/images/2024-04-07-method_array/image-20240407235435493.png" alt="image-20240407235435493" style="zoom:50%;" />

<img src="/images/2024-04-07-method_array/image-20240407235400877.png" alt="image-20240407235400877" style="zoom:50%;" />

=> <span style="font-size:85%">이미 정의한 함수를 전달하는 이 방식은 잘 쓰지 않는다</span>



<br>

<br>

<br>



> #### map()



<span style="font-size:85%">foreach()와 같이 배열의 요소에 대해 반복을 하는데 <span style="color: orangered">map()은 요소를 바꿀 수 있음</span></span>

<span style="font-size:85%">이때 기존의 배열이 바뀌는 것이 아니라 요소를 바꾼 새로운 배열을 생성함(return사용)</span>

<br>

**<span style="font-size:90%">[ syntax ]</span>**

```javascript
배열이름.map(function(element, index){
  실행문;
})

```

<br>

<span style="font-size:90%; font-weight:bold">[ map() 구문 연습 ]</span>

<img src="/images/2024-04-07-method_array/image-20240408225954385.png" alt="image-20240408225954385" style="zoom:50%;" />

<img src="/images/2024-04-07-method_array/image-20240408230008575.png" alt="image-20240408230008575" style="zoom:50%;" />

<span style="font-size:85%">=> 기존 배열의 요소에 각각 2를 곱한 값들로 새로운 배열이 만들어 지고, doubles라는 변수에 저장</span>



<br>

<span style="font-size:90%; font-weight:bold">[ map() 연습 - 영화제목만 추출한 배열만들기 ]</span>

<img src="/images/2024-04-07-method_array/image-20240408230757916.png" alt="image-20240408230757916" style="zoom:50%;" />

<img src="/images/2024-04-07-method_array/image-20240408230845563.png" alt="image-20240408230845563" style="zoom:50%;" />

<span style="font-size:85%">=> movies라는 배열의 각 요소를 함수의 매개변수 movie 자리로 받은 후, title을 반환받아서 새로운 배열을 만든다. 새로운 배열을 titles라는 변수에 저장한다.</span>

<br>

<br>

<br>

> #### fill()

<span style="font-size:85%">배열을 괄호안의 내용으로 채워준다</span>





<img src="/images/2024-04-07-method_array/image-20240509132617206.png" alt="image-20240509132617206" style="zoom:50%;" />

<span style="font-size:85%">=> 길이가 7인 빈 배열 만들기</span>

<br>

<img src="/images/2024-04-07-method_array/image-20240509133102417.png" alt="image-20240509133102417" style="zoom:50%;" />

<span style="font-size:85%">=> fill()메서드를 사용해 배열의 요소를 채운다</span>

<span style="font-size:85%">=> 괄호 속에 아무것도 없으면 undefined가 채워짐</span>

<br>

<img src="/images/2024-04-07-method_array/image-20240509134904803.png" alt="image-20240509134904803" style="zoom:50%;" />

<span style="font-size:85%">=> 0으로 채워있던 배열에서 map()을 사용해 기존 요소들의 '인덱스'가 요소가 되는 '새 배열'을 만들었다</span>



<br>

<br>

<br>







