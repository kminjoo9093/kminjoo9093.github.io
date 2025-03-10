---
layout: single
title: "[자바스크립트] intersectionObserver로 스크롤 애니메이션주기"
typora-root-url: ../
---





### Intersection Observer



브라우저 API 중 하나로, 요소와 뷰포트의 교차 영역을 감시하고 이벤트를 처리하는 기능을 제공한다. 스크롤 이벤트를 사용하지 않고도 **요소가 화면에 나타나는 시점을 감지하거나, 사라지는 시점을 쉽게 관찰**할 수 있게 해준다.

<br>

[intersectionObserver 사용 패턴]

```javascript
const observer = new intersectionObserver(콜백함수, 옵션); //관찰자 생성

const 관찰대상 = document.queryselector('html요소'); //관찰할 html요소 선택
observer.observe(관찰대상); //관찰자와 관찰대상 연결

//콜백함수는 관찰대상이 감지되면 실행할 코드
```



그러나 이렇게만 작성하면 정확한 코드가 아니며 오류가 날 수 있다

관찰대상 자체를 감시하는데 화면에 들어오고 나갈 때를 감지하기 때문에 관찰대상이 등장, 퇴장할때 모두 실행되기 때문이다

<br>

콜백함수는 IntersectionObserverEntry 객체와 관찰자 목록을 받는데

엔트리 목록에 포함되어 있는 각 엔트리(실제 관찰대상)가 화면에 등장하는지 확인하기 위해서 isIntersecting 속성 값을 확인한다

> isIntersecting : IntersectionObserverEntry 객체에서 사용할 수 있는 속성으로 관찰된 요소가 현재 뷰포트와 교차하는지(화면에 등장하는지) 여부를 true/false로 나타낸다

```javascript
//intersectionObserve의 콜백함수

function 콜백함수(entries, observer){
  entries.forEach((entry)=>{
    if(entry.isIntersecting){
    	//관찰대상이 화면에 등장 시 실행할 코드
    } else {
      //관찰대상이 화면에서 사라질 때 실행할 코드
    }
  })
}

//매개변수
//entries : 관찰된 각 요소(`IntersectionObserverEntry`)에 대한 정보를 담고 있는 배열
//observer: `IntersectionObserver` 객체 자체. 메서드 호출하여 관찰 요소들을 관리하고 추가 설정할 수 있다(unobserve()-관찰을 중지, disconnect()-관찰 해제)
```

=> 'isIntersecting' 사용으로 요소가 등장하는 순간을 조건으로 지정하면 등장/퇴장을 나눠 기능을 부여할 수 있다

<br>

=> 콜백 함수에서 entries 배열의 각 요소 entry는 관찰 중인 요소에 대한 정보를 포함하는IntersectionObserverEntry객체이다. 이 객체가 감시하는 실제 DOM 요소에 접근하기 위해서는 **' target '** 속성을 통해 실제 관찰 대상 요소를 가리켜야 한다. 

```javascript
//예시
entry.target.style.opacity = 1;
```

<br>

[ 참고 ]

entries 배열에서 특정 요소를 직접 접근하고 싶을 때 ' [0] ' 과 같이 인덱스를 사용할 수도 있다. 

하지만 일반적으로 forEach를 사용하여 모든 요소를 처리하는 것이 더 유연하고 권장되는 방법이다.

<br>

<br>

[ 옵션 ]

**Root**

가시성을 체크하기 위해 관찰하는 뷰포트의 기준이 되는 요소를 설정한다. 루트는 반드시 타겟의 상위 요소여야 한다.  기본적으로는 브라우저의 뷰포트를 기준으로 하지만, 특정 요소 안에서만 교차 영역을 계산하려면 해당 요소를 지정할 수 있다.

**타입**: Element 또는 null

**기본값**: null

<br>

**rootMargin**

뷰포트와 루트 요소 사이의 여백을 설정한다. 이 값의 집합은 교차 지점을 계산하기 전에 루트 요소 경계 박스의 각 사이드 값을 늘리거나 줄일 수 있다.

**타입**: 문자열

**기본값**: "0px" (css style의 margin 설정 방법과 동일)

<br>

**threshold (임계값)**

관찰 대상 요소와 뷰포트가 교차하는 비율을 설정하는 것으로 이 범위에 들면 콜백이 실행된다. 예를 들어, [0.5] 로 설정하면 요소의 절반 이상이 화면에 나타날 때 콜백이 호출됩니다. 

여러 값을 배열로 설정할 수 있어 여러 교차 비율에 대해 다르게 반응할 수 있다. 만약 가시성이 25%만큼 넘어갈 때마다 콜백을 실행하고 싶다면, [0, 0.25, 0.5, 0.75, 1]을 지정하면 된다.

1.0의 값은 모든 픽셀이 가시 상태가 될 때까지 임계값이 통과되지 않는다는 것을 의미합니다.

**타입**: 숫자 또는 숫자 배열

**기본값**: [0]



<br>

<br>

[관련 개념]

**intersectionRatio** (교차 비율)

:  IntersectionObserverEntry 객체의 속성으로, 관찰된 요소와 뷰포트가 교차하는 영역의 '정확한 실제 비율' 을 나타낸다. 콜백 함수 내에서 이 값을 통해 요소의 가시성 여부를 판단하거나 필요한 작업을 수행할 수 있다.

*threshold는 관찰 요소와 뷰포트의 교차 영역 비율을 **설정**하는 옵션 배열이고, intersectionRatio는 **실제 교차한 영역의 비율**을 나타내는 속성

**타입**: 값은 0에서 1 사이의 실수로 나타낸다. 0은 요소가 화면에 전혀 보이지 않음을 의미하고, 1은 요소의 전체 영역이 화면에 보이는 것을 의미합니다.

<br>

<br>

