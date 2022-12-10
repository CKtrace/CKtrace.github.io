---
title: '[Statistics] 수치형 자료 표현 방법 vs 범주형 자료 표현 방법'
layout: post
categories: statistics
tags: Statistics
comments: true
---

**Purpose of this Posting**
- 수치형 자료 표현 방법과 범주형 자료 표현 방법을 알아봅니다.


## **What are Numercial Data and Categorical Data?**

---

수치형 자료와 범주형 자료를 표현하는 여러 가지 방법들에 대해 알아보기 전에 수치형 자료와 범주형 자료란 무엇인지 알아야 합니다!

제가 이전에 수치형 자료와 범주형 자료에 대해 작성했던 글을 통해 알아보시면 좋을 것 같습니다!

바로 아래에 링크를 남겨두었으니 여러분들께 도움이 되었으면 좋겠습니다! 

[CKtrace의 산포의 척도 포스팅](https://cktrace.github.io/statistics/2022-02-22-Dispersion/)

이제 본격적으로 수치형 자료와 범주형 자료 표현 방법들에 대해 알아보도록 하겠습니다~!

## **<Numercial Data> - Dot Plot(점도표)**

---

<br>

<center><img src="https://user-images.githubusercontent.com/97859215/206828327-2227f995-39fa-45e5-a952-6699364649d5.png" width="500" height="500"></center>

> <center>Dot Chart 예시</center>

<br>

점도표(Dot Plot)란 각 관측값의 위치에 점을 표시하여 나타내는 것입니다.

같은 관측값이 존재하는 경우에는 그 위로 누적되는 형태를 띱니다.

## **<Numercial Data> - Histogram(히스토그램)**

---

<br>

<center><img src="https://user-images.githubusercontent.com/97859215/206828350-a9470f14-1cec-4209-8d11-8399b9df04d5.png" width="500" height="500"></center>

> <center>Histogram 예시</center>

<br>

히스토그램은 특히 수치형 자료 중에서 연속형 자료의 분포 형태를 나타내는데 활용됩니다.

해당하는 구간의 상대 도수를 직사각형의 면적으로 표시해 모든 면적의 합이 1이 되게 표현합니다.

(상대 도수란 무엇인지에 대해서는 도수분포표 파트에서 설명하도록 하겠습니다!)

그렇다면 히스토그램에서 높이는 무엇을 의미하는지 알아보도록 하겠습니다.

<br>

<center><img src="https://user-images.githubusercontent.com/97859215/206828360-3aa9b3db-63d8-4a55-8224-19da5ff17d05.png" width="500" height="200"></center>

> <center>Histogram 예시</center>

<br>


이때 밀도(Density)란 해당하는 구간에 자료들이 얼마나 모여 있는지 보여줍니다.

## **<Numercial Data> - Stem and Leaf Plot(줄기 잎 그림)**

---

<br>

<center><img src="https://user-images.githubusercontent.com/97859215/206828366-6411ad9f-53d6-4d19-a5ab-17a08d1a8164.png" width="200" height="300"></center>

> <center>Stem and Leaf 예시</center>

<br>


<br>

<center><img src="https://user-images.githubusercontent.com/97859215/206828385-ef62dd87-6894-40c3-b8ab-47bb2f4c0260.png" width="400" height="250"></center>

> <center>줄기와 잎의 의미</center>

<br>

줄기 잎 그림의 장점은 관측값의 정보는 어떠한 변형 없이 그대로 보존하는 것뿐만 아니라 자료의 분포 또한 알려준다는 것입니다.

## **<Categorical Data> - Bar Chart(막대 그래프)**

---

<br>

<center><img src="https://user-images.githubusercontent.com/97859215/206828467-b352b000-6464-44c7-bbdb-3bdb564b5632.png" width="400" height="350"></center>

> <center>Bar Chart 예시</center>

<br>

위 예시 그림을 통해 히스토그램은 막대그래프와 같은 것이 아닌가라는 궁금증을 가질 있습니다.

실제로 형태도 거의 똑같다 봐도 무방하기에 충분히 가질 수 있는 궁금증입니다.

하지만 통계에서는 히스토그램과 막대그래프를 엄격하게 구분한다는 점 유의해주세요!

막대 그래프는 각 범주의 빈도나 상대 도수를 막대 길이로 표시한 그래프입니다.

이때 상대 도수는 각 계급의 도수를 총 도수로 나눈 비율입니다.

단위는 % 입니다.

## **<Categorical Data> - Pie Chart(파이 차트)**

---

<br>

<center><img src="https://user-images.githubusercontent.com/97859215/206828524-e59b41f8-8fe6-48b6-8d1f-ccccb6a16b0d.png" width="500" height="550"></center>

> <center>Pie Chart 예시</center>

<br>

(위 그림을 원으로 봐주시면 감사하겠습니다 ㅠㅠ)

파이 차트는 원에 각 범주에 해당하는 비율만큼 각도를 분할해서 표시합니다.

이때 제가 여러분께 한 가지 질문을 던져보도록 하겠습니다!

> 파이 차트는 왜 원을 사용해서 표현하는 것일까요?  

바로 그 이유는 원에서 각 범주의 면적과 각도의 비가 항상 동일하기 때문입니다.

이러한 이유로 파이 차트를 표현하는데 원을 사용하는 것입니다!

## **<Numercial Data & Categorical Data> - Frequency Table(도수분포표)**

---

도수분포표는 대게 범주형 자료를 정리할 때 가장 많이 사용합니다.

도수분포표를 이해하기 위해서는 도수와 상대 도수란 무엇인지 알아야 합니다!

<br>

<center><img src="https://user-images.githubusercontent.com/97859215/206828584-dd680c96-3cc2-4e98-9b5f-855a7eec25af.png" width="500" height="250"></center>

> <center>도수와 상대 도수</center>

<br>

도수분포표에서는 상대 도수에 100을 곱해 퍼센트(%)로 표시하는 경우도 있습니다.

이제 도수와 상대 도수란 무엇인지 알아보았으니 도수분포표에 대한 설명을 이어나가도록 하겠습니다!

<br>

<center><img src="https://user-images.githubusercontent.com/97859215/206828843-66f1aff0-53c8-4859-8e39-cfdd9581aa64.png" width="300" height="500"></center>

> <center>Frequency Table 예시</center>

<br>

위 그림은 도수분포표 예시 그림입니다!

제시된 도수분포표에서 판매량이 도수이고, 판매비율이 상대 도수가 되는 것입니다~! 

그런데 도수분포표는 특이한 성질이 하나 있습니다...

바로 범주형 자료뿐만 아니라 수치형 자료를 도수분포표로 정리할 수 있다는 것입니다!

단, 조건을 충족하는 수치형 자료만 가능하다는 점 유의해주세요.

그 조건이란 무엇인지 알아보도록 하겠습니다~

자료의 수치형 값이 몇 개로 한정된 경우에 값을 몇 개의 구간으로 그룹화한 후에 해당 그룹에 속한 값들의 개수를 구합니다. (이때 그룹을 계급, class라고 합니다.)

그리고 구한 개수로 도수분포표를 만드는 것입니다!

즉, 수치형 자료 중 수치형 값이 몇 개로 한정되었다는 조건이 충족되었을 때는 수치형 자료임에도 불구하고 도수분포표로 표현 가능하다는 것입니다!

이번 포스팅에서는 수치형 자료와 범주형 자료의 다양한 표현 방법들에 대해 알아보았습니다!

여러분들께 많은 도움이 되었기를 바라며, 다음에도 좋은 포스팅으로 찾아뵙도록 하겠습니다.

긴 글 읽어주셔서 감사하다는 말씀드리며 글을 마치도록 하겠습니다!

감사합니다!