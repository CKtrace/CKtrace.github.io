---
layout: single
title: '[Statistics] 이산확률변수 VS 연속확률변수'
categories: Statistics
tag: [Statistics]
toc: true
author_profile: true
sidebar:
    nav: "docs"
---


**Purpose of this Posting**
- 이산확률변수와 연속확률변수에 대해 알아봅니다.


## **Discrete Random Variable vs Continuous Random Variable**

#### **(이산확률변수 vs 연속확률변수)**

---

이산확률변수(Discrete Random Variable)는 확률 변수의 값을 셀 수 있는 경우이고, 연속확률변수(Continuous Random Variable)는 확률 변수의 값을 셀 수 없는 경우입니다.

이산확률변수는 확률 변수의 값을 셀 수 있기에 이산확률변수 X가 각 변수 x일 확률이 딱딱 정해지는 반면, 연속확률변수는 확률 변수의 값을 셀 수 없기에 연속확률변수가 X가 어떤 범위 안에 속할 확률을 구합니다. 

두 확률 변수는 확률과 변수들을 이용해 함수로 나타낼 수 있습니다!

\-> 이산확률변수는 확률질량함수!

\-> 연속확률변수는 확률밀도함수!

다음 인덱스를 통해 확률질량함수와 확률밀도함수를 차례로 알아보도록 하겠습니다.

## **Probability Mass Function(확률질량함수)**

---

이산확률변수 X가 임의의 x일 확률 -> P(X = x)

이때, P(X = x)를 x에 대한 함수로 표현한 것이 확률질량함수(Probability Mass Function)입니다.

<br>

<center><img src="https://user-images.githubusercontent.com/97859215/206822486-22a66e12-c1c8-415a-a24a-ade94ef9a89e.png" width="300" height="200"></center>

> <center>확률의 공리</center>

<br>

또한 확률질량함수는 이산확률변수 X가 가질 수 있는 모든 값에 대해 이 값을 가질 확률들이 대응되는 관계를 나타낸 함수입니다.

<br>

<center><img src="https://user-images.githubusercontent.com/97859215/206822500-34853901-5204-4a90-b4ad-b28e24a7ac9d.png" width="500" height="150"></center>


<br>

그렇다면 이제 일반적인 확률질량함수는 어떤 그래프 형태를 띠는지 알아보도록 하겠습니다.

<br>

<center><img src="https://user-images.githubusercontent.com/97859215/206822520-23b4941f-5f4e-4aa2-abd5-d594a9161bf2.png" width="400" height="400"></center>

> <center>확률질량함수 그래프</center>

<br>

확률질량함수의 그래프에서 y값은 확률이지만 다음 인덱스에서 알아볼 연속확률변수와 연관된 함수의 그래프에서는 확률이 다른 형태로 나타나기에 잘 기억해두셔야 합니다!

확률질량함수의 성질은 총 3가지로 나눌 수 있습니다.

<br>

<center><img src="https://user-images.githubusercontent.com/97859215/206822559-d7ec1ac8-b16d-44d3-8b81-aac2287b01d7.png" width="400" height="200"></center>

> <center>확률질량함수의 세 가지 성질</center>

<br>

이산확률변수에 확률질량함수가 있다면 연속확률변수와도 연관된 함수를 알아보도록 하겠습니다!

## **Probability Density Function(확률밀도함수)**

---

연속확률변수 X가 임의의 범위(a~b) 안에 속할 확률 -> P(a ≤  X ≤ b)

이때, 연속확률변수를 나타내는 함수가 바로 확률밀도함수(Probability Density Function)입니다.

<br>

<center><img src="https://user-images.githubusercontent.com/97859215/206822610-b18c6489-aade-4d50-836c-2e117fa10297.png" width="400" height="100"></center>


<br>

확률밀도함수의 그래프는 일반적으로 어떤 형태를 띄는지 알아보도록 하겠습니다.

<br>

<center><img src="https://user-images.githubusercontent.com/97859215/206822633-598f7461-8739-4dc2-b23c-936bf68e672b.png" width="400" height="350"></center>

> <center>확률밀도함수의 그래프</center>

<br>

확률밀도함수의 그래프에서 y값은 확률질량함수와 달리 밀도를 의미합니다. 

확률질량함수의 그래프에서 y값은 확률을 의미했다면 확률밀도함수의 그래프에서는 위 그래프에서 색을 채운 부분처럼, 면적의 넓이가 확률이 됩니다.

마지막으로 확률밀도함수의 성질에 대해 알아보도록 하겠습니다.

확률밀도함수의 성질 또한 총 3가지로 나눌 수 있습니다.

<br>

<center><img src="https://user-images.githubusercontent.com/97859215/206822654-80846640-0ea9-418f-a43f-052407debc2a.png" width="400" height="200"></center>

> <center>확률밀도함수의 세 가지 성질</center>

<br>

이렇게 해서 이산확률변수와 연속확률변수에 관련한 내용들을 알아보았습니다.

긴 글 읽어주셔서 감사하다는 말씀드립니다.

더 나은 글로 또다시 찾아뵙도록 노력하겠습니다!