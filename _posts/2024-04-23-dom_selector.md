---
layout: single
title: "[자바스크립트_개념정리] DOM_selector"
typora-root-url: ../
---







## 요소 선택을 도와주는 ' 선택 메서드 '

<br>

<br>

#### 1. document.getElementById()

<span style="font-size:85%"> : 주어진 문자열과 일치하는 id를 가진 요소를 찾아 객체로 반환한다</span>

<span style="font-size:85%">문서 내에 주어진 id가 없어 찾지 못하면 null을 반환</span>

<br>

**<span style="font-size:85%">[ syntax ]</span>**

```javascript
document.getElementById('id');
```



**<span style="font-size:85%">[ 구문 연습 - 퀴즈문제 ]</span>**

<img src="/images/2024-04-23-dom_selector/image-20240423002426954.png" alt="image-20240423002426954" style="zoom:50%;" />

<img src="/images/2024-04-23-dom_selector/image-20240423002444321.png" alt="image-20240423002444321" style="zoom:50%;" />



<span style="font-size:85%">=> id가 'unicorn'인 이미지 요소를 image라는 변수에 저장</span>

<span style="font-size:85%">=> id가 'mainheading'인 h1를 heading이라는 변수에 저장</span>

<br>

<br>



#### 2. document.getElementsByTagName()

<span style="font-size:85%">: 해당 태그를 모두 선택</span>

<span style="font-size:75%; color:green">Elements 가 복수형인 이유는 해당 태그를 한 번에 한 개 이상을 선택해야 하기 때문</span>

<br>

**<span style="font-size:85%">[ syntax ]</span>**

```javascript
document.getElementByTagName('tag');
```



<img src="/images/2024-04-23-dom_selector/image-20240423010424618.png" alt="image-20240423010424618" style="zoom:50%;" />

<img src="/images/2024-04-23-dom_selector/image-20240423004810359.png" alt="image-20240423004810359" style="zoom:50%;" />

<span style="font-size:85%">=> p태그인 세 개의 객체가 반환된다</span>

<span style="font-size:85%">이것은 인덱스와 길이가 있는 반복 가능한 집합이지만 배열은 아니다</span>

<br>

<img src="/images/2024-04-23-dom_selector/image-20240423005839579.png" alt="image-20240423005839579" style="zoom:50%;" />

<br>

<br>

#### 3. document.getElementsByClassName()

<span style="font-size:85%">: 해당 클래스를 모두 선택</span>

<br>

**<span style="font-size:85%">[ syntax ]</span>**

```javascript
document.getElementByClassName('class');
```

<br>

<img src="/images/2024-04-23-dom_selector/image-20240423010149211.png" alt="image-20240423010149211" style="zoom:50%;" />

<img src="/images/2024-04-23-dom_selector/image-20240423010212220.png" alt="image-20240423010212220" style="zoom:50%;" />

<span style="font-size:85%">=> 클래스가 'name'인 객체를 선택</span>

<br>

<br>

#### 4. document.querySelector()

 : 일치하는 첫 번째 요소를 반환

<br>

**<span style="font-size:85%">[ syntax ]</span>**

```javascript
document.quertSelector('tag');
document.querySelector('.class');
document.querySelector('#id')
```

<br>

<img src="/images/2024-04-23-dom_selector/image-20240423010713197.png" alt="image-20240423010713197" style="zoom:50%;" />

=> p태그 중 첫 번째 요소인 "안녕하세요"

<br>

<br>

#### 5. document.querySelectorAll()

 : 일치하는 모든 요소 반환

<br>

**<span style="font-size:85%">[ syntax ]</span>**

```javascript
document.quertSelectorAll('tag');
document.querySelectorAll('.class');
document.querySelectorAll('#id')
```

<br>

<img src="/images/2024-04-23-dom_selector/image-20240423010836164.png" alt="image-20240423010836164" style="zoom:50%;" />



