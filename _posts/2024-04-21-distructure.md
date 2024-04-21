---
layout: single
title: "[자바스크립트_개념정리] 구조 분해 "
typora-root-url: ../
---





### 구조 분해  distructure

<span style = "font-size:85%">: 주로 배열이나 객체의 속성을 해체해서 원하는 값을 선정해 복사한 후 별도의 변수에 저장한다</span>

<br>

<br>

#### - 배열 리터럴의 구조 분해

<span style = "font-size:85%">배열의 구조 분해에서는 순서가 중요하다</span>

<br>

<span style = "font-size:90%; font-weight:bold">[ syntax ]</span>

```javascript
const a = [1, 2, 3, 4];
const [b, c] = a;  //=> a배열을 구조 분해

console.log(b)  //1
console.log(c)  //2
```



<br>

<span style = "font-size:90%; font-weight:bold">[ 구문 연습하기 ]</span>

<img src="/images/2024-04-21-distructure/image-20240421171345366.png" alt="image-20240421171345366" style="zoom:50%;" />

<img src="/images/2024-04-21-distructure/image-20240421171407021.png" alt="image-20240421171407021" style="zoom:50%;" />

<span style = "font-size:85%">=> 두 번째 줄에서 ' = ' 좌측의 대괄호는 raceResults 배열에서 분해한 각 요소를 어떻게 지칭할지 결정한다</span>

<span style = "font-size:85%">=> 배열 요소는 순서대로 gold, silver, bronze의 값이 되고 나머지 'sera', 'tomi'는 나머지 매개변수 everyoneElse에 모여 저장됨</span>



<br>

<br>

<br>



#### - 객체 리터럴의 구조분해

<span style = "font-size:85%">순서를 따르지 않아 배열 구조 분해보다 실용적이다</span>

<span style = "font-size:85%">객체의 값을 기반으로 새로운 변수를 만든다</span>



<br>

<span style = "font-size:90%; font-weight:bold">[ syntax ]</span>

```javascript
const 객체리터럴명 = {
  속성1: 값1,
  속성2: 값2,
  속성3: 값3
}

const {속성1, 속성2} = 객체리터럴명;   // 구조 분해로 속성1,2 를 복사

//속성1이라는 변수에 '속성1:값1'을 속성2라는 이름의 변수에 '속성2:값2'를 저장한 셈이다
```

<br>

<span style = "font-size:90%; font-weight:bold">[ 구문 연습하기 ]</span>

<img src="/images/2024-04-21-distructure/image-20240421173704869.png" alt="image-20240421173704869" style="zoom:50%;" />

<img src="/images/2024-04-21-distructure/image-20240421173744541.png" alt="image-20240421173744541" style="zoom:50%;" />

<span style = "font-size:85%">=> 구조분해로 변수에 저장한 firstName, age, email의 값은 반환이 되지만, 저장하지 않은 city, lastName의 값은 반환되지 않는다</span>

<br>

<span style = "font-size:85%">구조 분해 방법을 쓰지 않으면 아래와 같이 따로 따로 변수에 저장해야 해서 번거롭다</span>

<img src="/images/2024-04-21-distructure/image-20240421174141243.png" alt="image-20240421174141243" style="zoom:50%;" />

<img src="/images/2024-04-21-distructure/image-20240421174153986.png" alt="image-20240421174153986" style="zoom:55%;" />

<br>

<br>

<span style = "font-size:90%; font-weight:bold">- 객체 리터럴의 속성명과 다른 ' 새로운 이름 '으로 변수 저장하기</span>

<img src="/images/2024-04-21-distructure/image-20240421185847446.png" alt="image-20240421185847446" style="zoom:50%;" />

<img src="/images/2024-04-21-distructure/image-20240421185902008.png" alt="image-20240421185902008" style="zoom:55%;" />

<span style = "font-size:85%">=> 객체 리터럴에서 ' born ' 이라는 속성명의 값이 ' birthYear ' 변수에 저장됨</span>

<br>

<span style = "font-size:90%; font-weight:bold">- 디폴트 값 추가</span>

<img src="/images/2024-04-21-distructure/image-20240421191041086.png" alt="image-20240421191041086" style="zoom:50%;" />

<img src="/images/2024-04-21-distructure/image-20240421191053769.png" alt="image-20240421191053769" style="zoom:55%;" />

<span style = "font-size:85%">=> 값이 존재하는 ' birthYear '는 그 값(born : 1999)이 나오고, 새로운 속성이라 값이 존재하지 않는 gender는 디폴트 값인 'female' 이 반환됨</span>

<br>

<br>

<br>



#### - 함수 매개변수의 구조분해

함수를 정의할 때 괄호안에 매개변수 작성으로 전달되는 값의 구조를 분해할 수 있다

주로 객체에 사용되는 방법



<br>

<br>

 <span style = "font-size:85%">user라는 객체 리터럴을 가지고  ' lastName ' 과 ' firstName ' 의 값으로 함수를 실행하려 할 때</span>

<img src="/images/2024-04-21-distructure/image-20240421194005107.png" alt="image-20240421194005107" style="zoom:50%;" />

<br>

 <span style = "font-size:85%">구조 분해를 하지 않으면 </span>

<img src="/images/2024-04-21-distructure/image-20240421194308739.png" alt="image-20240421194308739" style="zoom:50%;" />

<img src="/images/2024-04-21-distructure/image-20240421194112442.png" alt="image-20240421194112442" style="zoom:60%;" />

<br>

 <span style = "font-size:85%">구조분해를 하면 아래와 같다</span>

<img src="/images/2024-04-21-distructure/image-20240421194531970.png" alt="image-20240421194531970" style="zoom:50%;" />

<img src="/images/2024-04-21-distructure/image-20240421194542539.png" alt="image-20240421194542539" style="zoom:60%;" />

<br>

 <span style = "font-size:85%; color: green">이때 더 간단히 구조 분해 하는 방법이 있는데</span>

<img src="/images/2024-04-21-distructure/image-20240421195302617.png" alt="image-20240421195302617" style="zoom:50%;" />

<img src="/images/2024-04-21-distructure/image-20240421195313477.png" alt="image-20240421195313477" style="zoom:60%;" />

 <span style = "font-size:85%">=> 함수를 정의할 때 매개변수 자리에서 구조를 분해한다 (이때 객체이름 user를 쓰지 않음)</span>

 <span style = "font-size:85%">=> 함수를 실행할 때 구조 분해한 매개변수 자리에 user를 쓰면 user객체가 구조 분해되어 firstName과 lastName 값이 뽑혀 나온다</span>



<br>

<br>

##### 배열 메서드와 구조 분해 활용



<span style = "font-size:90%; font-weight:bold">[ 활용 1 ]</span>

<img src="/images/2024-04-21-distructure/image-20240421202342768.png" alt="image-20240421202342768" style="zoom:50%;" />

<img src="/images/2024-04-21-distructure/image-20240421202353324.png" alt="image-20240421202353324" style="zoom:50%;" />

<img src="/images/2024-04-21-distructure/image-20240421202406270.png" alt="image-20240421202406270" style="zoom:50%;" />

 <span style = "font-size:85%">=> 위와 같이 객체 리터럴이 들어있는 배열이 있을 때, 구조 분해를 하지 않으면</span>

 <span style = "font-size:85%">filter메서드의 인수인 화살표 함수에서 movie라는 매개변수가 필요하다</span>

<br>

 <span style = "font-size:85%">하지만 매개변수자리를 구조 분해하면</span>

<img src="/images/2024-04-21-distructure/image-20240421203241478.png" alt="image-20240421203241478" style="zoom: 55%;" />

<img src="/images/2024-04-21-distructure/image-20240421203217889.png" alt="image-20240421203217889" style="zoom:50%;" />

 <span style = "font-size:85%">=> movie와 같은 매개변수가 없어도 같은 결과가 나온다</span>

<br>

<br>



<span style = "font-size:90%; font-weight:bold">[ 활용 2 ]</span>

<img src="/images/2024-04-21-distructure/image-20240421203806652.png" alt="image-20240421203806652" style="zoom:50%;" />

<img src="/images/2024-04-21-distructure/image-20240421203751090.png" alt="image-20240421203751090" style="zoom:50%;" />

 <span style = "font-size:85%">=> map메서드를 사용할 때도 마찬가지로 구조 분해를 하지 않은 방식을 사용하면 movie라는 매개변수가 필요하고</span>

<br>

<img src="/images/2024-04-21-distructure/image-20240421204028495.png" alt="image-20240421204028495" style="zoom:50%;" />

<img src="/images/2024-04-21-distructure/image-20240421204056958.png" alt="image-20240421204056958" style="zoom:50%;" />

 <span style = "font-size:85%">=> 구조 분해를 하면 movie라는 매개변수를 넣지 않아 더 간편하다</span>