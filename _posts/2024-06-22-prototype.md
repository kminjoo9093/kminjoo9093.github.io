---
layout: single
title: "[자바스크립트_개념정리] 객체지향 프로토타입"
typora-root-url: ../
---



<br>

<br>

### 프로토타입 prototype



 <span style="font-size:85%; line-height:1.2;">자바스크립트 객체가 서로 기능을 상속하는 방식의 매커니즘</span>

<span style="font-size:85%;  line-height:1.2;">모든 자바스크립트 객체는 프로토타입 객체를 자동으로 가지게 되는데 이를 통해 다른 객체의 메소드와 속성을 상속받을 수 있다</span>

<span style="font-size:85% line-height:1.2;">`Object.prototype`은 모든 JavaScript 객체의 최상위 프로토타입 체인의 일부이다</span>

<br>

<br>

<span style="font-size:90%">**프로토타입 체인 prototype chain**을 통해 상속이 일어나는데</span>

<span style="font-size:85%; color:orangered;">프로토타입은 유전자와 같은 것으로 부모의 프로토타입에 뭔가를 추가하면 자식도 그것을 사용할 수 있다</span>

<br>

<img src="/images/2024-06-22-prototype/image-20240623231930510.png" alt="image-20240623231930510" style="zoom:50%;" />

<img src="/images/2024-06-22-prototype/image-20240623233543614.png" alt="image-20240623233543614" style="zoom:50%;" />

<span style="font-size:85%">=> `person` 객체에는 직접 `toUppercase()` 메소드가 없지만 최상위 프로토타입 'Object.prototype' 을 통해 상속받기 때문에  사용할 수 있다</span>

<br>

<br>

<span style="font-size:85%; font-weight:bold;">상속을 위해서 부모요소에 직접 추가할 수도 있고(이 경우 자식이 추가된 속성을 직접 가짐)</span>

<span style="font-size:85%; font-weight:bold;">부모의 유전자인 셈인 프로토타입에 추가할 수도 있다(이 경우 부모만 속성을 가지고 있지만 자식도 그 속성에 접근 가능)</span>

<br>

<span style="font-size:90%; font-weight:bold;">[ 프로토타입과 생성자함수]</span>

<img src="/images/2024-06-22-prototype/image-20240623224635238.png" alt="image-20240623224635238" style="zoom:50%;" />



<br>

<img src="/images/2024-06-22-prototype/image-20240623225045051.png" alt="image-20240623225045051" style="zoom:50%;" />

<span style="font-size:85%">=> drink로부터 생성되는 자식 beverage</span>

<span style="font-size:85%">=> drink의 프로토타입에 속성을 추가하니 beverage는 추가한 속성을 직접 가지진 않지만 접근이 가능하다</span>

<span style="font-size:85%; color:orangered;">=> 객체의 프로퍼티나 메소드에 접근할 때, JavaScript는 해당 객체에서 찾지 못하면 프로토타입 체인을 따라 부모 객체의 프로퍼티나 메소드를 찾는다</span>

<br>

<br>

<span style="font-size:90%; font-weight:bold;">[ 프로토타입의 장점 ]</span>

<span style="font-size:85%;">1. **상속**: 프로토타입을 사용하여 객체 간의 상속 관계를 구현할 수 있다. 이는 코드 재사용성을 높이고, 객체 지향 프로그래밍의 중요한 기능을 제공한다</span>

<span style="font-size:85%;">2. **메모리 절약**: 프로토타입 체인을 통해 메모리 사용을 최적화할 수 있다. 각 객체가 공통된 메소드나 속성을 메모리에 별도로 유지할 필요가 없기 때문이다</span>

<span style="font-size:85%;">3. **동적 프로퍼티 추가**: 객체의 프로토타입에 동적으로 메소드나 속성을 추가할 수 있어, 실행 중에 객체의 기능을 확장할 수 있다</span>
