---
title: '[Statistics] 결합분포와 주변분포'
layout: post
categories: statistics
tags: Statistics
comments: true
---

**Purpose of this Posting**
- 결합분포와 주변분포에 대해 알아봅니다.

## **Joint Distribution(결합분포)**

---

결합분포란 두 개 혹은 그 이상의 변수들을 고려한 확률 분포입니다.

결합분포를 구성하는 변수들이 이산확률변수일 때는 이산확률변수에 대해 결합확률질량함수를 갖습니다.

예를 들어, 결합분포를 구성한 변수 두 개가 이산확률변수라면 결합확률질량함수는 아래와 같습니다.

<br>

<center><img src="https://user-images.githubusercontent.com/97859215/206823634-df914c42-1d4f-40c4-9bf6-9f683b276885.png" width="300" height="150"></center>

<br>

변수들이 이산확률변수인 경우가 존재하는 것처럼, 연속확률변수인 경우도 존재합니다.

결합분포를 구성하는 변수들이 연속확률변수일 때는 연속확률변수에 대해 결합확률밀도함수를 갖습니다.

예를 들어, 결합분포를 구성한 변수 두 개가 연속확률변수라면 결합확률밀도함수는 아래와 같습니다.

<br>

<center><img src="https://user-images.githubusercontent.com/97859215/206823648-f4c5587c-68b7-450d-bdea-10df9cc0213e.png" width="300" height="250"></center>

<br>

위 필기 본에서 알 수 있다시피 결합확률밀도함수는 두 가지 특징을 갖기 때문에 이 부분 알아가시면 좋을 것 같습니다!

즉, 정리해보면 결합분포는 2개 혹은 그 이상의 변수들을 고려한 확률분포이고 변수들이 연속확률변수인지 이산확률변수인지에 따라 차이가 존재한다는 것입니다!

## **Marginal Distribution(주변분포)**

---

주변분포는 결합분포와 밀접하게 연관된 분포입니다.

주변분포는 두 변수의 결합분포가 있을 때 한 변수의 분포를 무시했을 때 다른 한 변수의 분포를 주변분포라고 합니다.

조금 더 이해하기 쉽게 설명하자면, 표본 공간이 사건 Y1, Y2, Y3,... , Yn로 분할될 때 사건 X의 확률을 그림으로 그려보면

<br>

<center><img src="https://user-images.githubusercontent.com/97859215/206823659-19155dd4-141a-4379-9655-e003216af18d.png" width="400" height="250"></center>

<br>

위 그림과 같은 구조를 갖게 되고 식으로 나타내게 되면 아래와 같습니다.

<br>

<center><img src="https://user-images.githubusercontent.com/97859215/206823683-e0f957be-d880-461a-90c2-758e74430bfa.png" width="300" height="150"></center>

<br>

이제 결합분포와 주변분포를 표를 통해 결합확률과 주변확률이 어떻게 구성되어 있는지 확인해보도록 하겠습니다.

## **Joint Probability & Marginal Probability**

---

표를 통해 결합확률과 주변확률에 대해 알아보도록 하겠습니다.

<br>

<center><img src="https://user-images.githubusercontent.com/97859215/206823723-8ea2d18b-f652-4f29-8e7b-b7029ed1f180.png" width="500" height="300"></center>

<br>

위 표를 통해서도 위에서 결합분포와 주변분포에 대해 설명드린 것처럼 결합확률은 두 변수를 고려한 값이고, 주변확률은 하나의 변수를 고정하고 하나의 변수 값만을 고려한 값임을 알 수 있습니다.

이렇게 해서 결합분포, 주변분포 그리고 결합확률과 주변확률에 대해 알아보았습니다.

긴 글 읽어주셔서 감사하다는 말씀드리며 글을 마치도록 하겠습니다.

감사합니다.