---
layout: single
title: "[자바스크립트_개념정리] arguments 와 rest"
typora-root-url: ../
---





 #### 인수 객체   **' arguments '** 



<span style="font-size:85%">배열과 비슷한 형태로 유사 배열 객체라고 부르기도 하며 함수로 전달된 모든 인수를 참조할 수 있다</span>

<span style="font-size:85%">요소에 접근하려면 인덱스를 사용해야 하며 length 속성을 갖고 있지만</span>

<span style="font-size:85%; color:orangered">배열이 아니며 push 나 pop등과 같은 배열 메서드를 사용할 수는 없다</span>

<br>

<img src="/images/2024-04-20-arguments_object/image-20240421002004152.png" alt="image-20240421002004152" style="zoom:50%;" />

<span style="font-size:85%">=> 모든 인수를 받을 수 있도록 함수를 정의할 때 매개변수를 정하지 않고, 인수 객체 arguments를 출력하도록 함</span>

<span style="font-size:85%">=> 여러 인수를 넣어 함수를 실행하니까 배열과 비슷한 형태로 모든 인수를 모아 놓은 arguments 객체가 출력되는 걸 볼 수 있다</span>



<br>

<br>

<span style="font-size:85%; color:green">인수 객체 ' arguments' 는 배열이 될 수 없기에 배열 메서드 사용이 불가하고, 화살표 함수에서 사용할 수 없기에 인수들을 배열로 변활할 수 있는 나머지 매개변수 '...' 가 필요하다</span>

<br>

<br>



####  ' ... '  나머지 매개변수 ( rest params )



<span style="font-size:85%">매개변수 목록에 자리하며</span>

<span style="font-size:85%">계획보다 많은 인수를 받을 경우 남아있는 인수를 모두 모아 배열로 나타낸다</span>

<br>



**<span style="font-size:90%">[ 특징 확인하기 ]</span>**

<img src="/images/2024-04-20-arguments_object/image-20240421122229096.png" alt="image-20240421122229096" style="zoom:50%;" />

<span style="font-size:85%">=> 매개변수 하나를 넣었을 때 인수 여러개를 넣으면 첫번째 인수만 유효함</span>



<br>

<img src="/images/2024-04-20-arguments_object/image-20240421122321762.png" alt="image-20240421122321762" style="zoom:50%;" />

<span style="font-size:85%; color:orangered">=> 나머지 매개변수를 사용하면 여러 인수들을 모아 배열로 나타냄</span>

<br>

<br>

**<span style="font-size:90%">[ 실제 배열에 reduce메서드 사용 ]</span>**

<img src="/images/2024-04-20-arguments_object/image-20240421130500829.png" alt="image-20240421130500829" style="zoom:50%;" />



<br>

**<span style="font-size:85%">[ 나머지 매개변수와 reduce메서드 사용 ]</span>**

<img src="/images/2024-04-20-arguments_object/image-20240421130215031.png" alt="image-20240421130215031" style="zoom:50%;" />

<span style="font-size:85%">=> '...' 를 넣으면 함수에 **배열이 아닌 여러 인수를 넣어도 배열 메서드 reduce를 실행할 수 있다**</span>

<span style="font-size:85%">=> 함수에 실제 배열을 넣어 reduce메서드를 실행한 것과 결과가 동일</span>



**<span style="font-size:85%; color:orangered">[ 주의 ]</span>**

<img src="/images/2024-04-20-arguments_object/image-20240421134620700.png" alt="image-20240421134620700" style="zoom:50%;" />

<span style="font-size:85%">=> 모든 인수를 받는 인수객체 arguments는 배열메서드 reduce 사용 불가</span>

<br>

<br>

**<span style="font-size:90%">[ 나머지 매개변수 활용하기 ]</span>**

<img src="/images/2024-04-20-arguments_object/image-20240421132646200.png" alt="image-20240421132646200" style="zoom:50%;" />

<img src="/images/2024-04-20-arguments_object/image-20240421132629186.png" alt="image-20240421132629186" style="zoom:50%;" />

<span style="font-size:85%">=> 'minjoo', 'suhyun'은 각각 첫 번째, 두 번째 매개변수에 들어가고</span>

<span style="font-size:85%">=> 나머지  'mina', 'joe', 'mike' 인수들는 ...everyoneElse로 인해 한데 모아짐</span>

<br>

<br>

**<span style="font-size:85%; color:orangered">[ 주의 ]</span>**

<span style="font-size:85%; color:orangered">스프레드 '...' 와 구분해야한다</span>

<span style="font-size:85%; color:orangered">스프레드 '...' 는 인수들을 펼치고, 나머지 매개변수 '...' 는 인수들을 한데 모으는 역할이다</span>