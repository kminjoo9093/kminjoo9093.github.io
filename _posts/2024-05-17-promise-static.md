---
layout: single
title: "[자바스크립트_개념정리] Promise가 제공하는 static 함수"
typora-root-url: ../
---



<br>

#### Promise.all()

<br>

<span style="font-size:85%">: 여러 개의 Promise를 동시에 실행</span>

<span style="font-size:85%">인자로 배열을 넣을 수 있는데 그 배열 안에 여러 개의 promise를 넣으면 동시에 실행된다</span>

<span style="font-size:85%; color:orangered">전달 된 프로미스 중 하나라도 실패하면 모든 promise를 reject시킴</span>

<span style="font-size:85%; color:orangered">여러 프로미스가 실패하면 제일 처음 실패한 promise의 에러가 catch에 들어감</span>

<br>

<br>

<br>

#### Promise.allSettled()

<br>

<span style="font-size:85%; color:orangered">각각의 promise의 성공/실패를 자세히 알고싶을 때 사용</span>

<span style="font-size:85%">all 과 마찬가지로 배열 형태로 promise를 전달받음</span>

<span style="font-size:85%">전달된 promise의 작업이 성공이든 실패든 완료될 때까지 기다림</span>

<br>

<br>

<br>

#### Promise.any()

<br>

<span style="font-size:85%">배열 형태로 promise를 전달받음</span>

<span style="font-size:85%; color:orangered">전달된 promise중에 가장 먼저 resolve된 것의 값을 반환</span>

<span style="font-size:85%; color:orangered">promise가 모두 실패해야 에러</span>

<span style="font-size:85%">reject가 있어도 그 후 resolve인 promise가 있다면 그것의 값을 반환</span>

<br>

<br>

<br>

#### Promise.race()

<br>

<span style="font-size:85%"> 배열 형태로 promise를 전달받음</span>

<span style="font-size:85%; color:orangered">전달해준 promise끼리 경주를 시키듯 가장 빨리 완료되는 promise의 결과를 반환</span>

<br>

<br>

