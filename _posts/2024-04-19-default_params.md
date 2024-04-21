---
layout: single
title: "[자바스크립트_개념정리] 기본 매개 변수"
typora-root-url: ../
---





>  #### default params   기본 매개변수

<br>

<span style="font-size:85%">함수를 쓸 때 매개변수가 없으면 디폴트 매개변수를 받는다</span>

<br>

**<span style="font-size:85%">기본 매개변수 값을 설정하지 않으면</span>**

![image-20240420120304436](/images/2024-04-19-default_params/image-20240420120304436.png)

<img src="/images/2024-04-19-default_params/image-20240420120317715.png" alt="image-20240420120317715" style="zoom:50%;" />

<span style="font-size:85%">=> 인수를 넣지 않았을 때 NaN이 나온다</span>



<br>

**<span style="font-size:85%">기본 매개변수 값을 설정하면</span>**

<img src="/images/2024-04-19-default_params/image-20240420120401443.png" alt="image-20240420120401443" style="zoom:50%;" />

<img src="/images/2024-04-19-default_params/image-20240420123448389.png" alt="image-20240420123448389" style="zoom:50%;" />

<img src="/images/2024-04-19-default_params/image-20240420123343217.png" alt="image-20240420123343217" style="zoom:50%;" />

<span style="font-size:85%">=> numSides가 받는 인수가 있을 경우는 그 값을 받고, 없을 경우는 기본 매개변수로 설정한 6을 받는다</span>

<br>

<span style="font-size:85%">**BUT !!** 위 방식은 옛날방식고 요즘 쓰는 **더 간단한 방식**이 있다</span>

<br>

<br>

<span style="font-size:90%; font-weight:bold">[ syntax ]</span>

```javascript
function 함수명(매개변수, 매개변수 = 디폴트 값) {
  return 실행문;
}

//위 구문은 매개변수가 두 개인 경우
```

<br>

<span style="font-size:85%; color:orangered">등호와 디폴트 값을 매개변수 목록에 넣어주는 방식이다</span>

<br>

<span style="font-size:90%; font-weight:bold">[ 구문 연습 ]</span>

<img src="/images/2024-04-19-default_params/image-20240420124845156.png" alt="image-20240420124845156" style="zoom:50%;" />

<img src="/images/2024-04-19-default_params/image-20240420124908267.png" alt="image-20240420124908267" style="zoom:50%;" />

<span style="font-size:85%">=> 인수가 없으니 기본 매개변수 값으로 설정한 6을 받아 함수가 실행된다</span>

<br>

<span style="font-size:85%; color:orangered">이때 매개변수의 순서를 조심해야 하는데</span>



<img src="/images/2024-04-19-default_params/image-20240420125453669.png" alt="image-20240420125453669" style="zoom:50%;" />

<img src="/images/2024-04-19-default_params/image-20240420143942949.png" alt="image-20240420143942949" style="zoom:50%;" />

<span style="font-size:85%">=> 첫 번째 매개변수인 msg의 디폴트 값을 "Hello"라 설정하고, 두 번째 매개변수 person의 인수로 "Minjoo"만 입력하고 함수를 실행</span>

<span style="font-size:85%">=> "Minjoo"가 person자리의 인수라는 것을 인식하지 못하고 첫 번째 매개변수인 msg의 인수로 인식해버림</span>

<br>



<span style="font-size:90%; color:orangered; font-weight:bold">디폴트 값이 있는 매개변수는 디폴트 값이 없는 매개변수 뒤에 와야 한다</span>



<img src="/images/2024-04-19-default_params/image-20240420145608222.png" alt="image-20240420145608222" style="zoom:50%;" />

<img src="/images/2024-04-19-default_params/image-20240420145621427.png" alt="image-20240420145621427" style="zoom:50%;" />

<span style="font-size:85%">=> 디폴트 값이 없는 person을 먼저 쓰고 "Hello"가 디폴트 값인 msg는 뒤에 씀</span>

<span style="font-size:85%">=> "Minjoo"를 person의 인수로 잘 인식함</span>