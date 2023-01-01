---
layout: single
title:  '[Statistics] 변동 계수'
categories: Statistics
tag: [Statistics]
toc: true
author_profile: true
sidebar:
    nav: "docs"
sitemap :
    changefreq : weekly
    priority : 1.0
---


**Purpose of this Posting**
- 변동 계수에 대해 알아봅니다.

## **Before entering...**

---

변동 계수에 대해 알아보기 전에 표준 편차란 무엇인지에 대해 알아야 합니다.

혹시 표준 편차에 대한 개념이 조금 분명하지 않거나 무엇인지 모르시는 분들께 도움이 되고자 제가 작성했던 포스팅의 링크를 첨부하도록 하겠습니다.


[CKtrace의 산포의 척도 포스팅](https://cktrace.github.io/statistics/2022-02-22-Dispersion/)

위 포스팅을 통해 표준 편차에 대해 알아보시고 이 포스팅을 읽으시면 더 잘 이해가 되실 거라 믿습니다!

그러면 이제 변동 계수에 대해 알아보도록 하겠습니다!

## **Why do we use Coefficient of Variance(변동 계수)?**

---

표준 편차를 이용해 두 그룹을 비교할 때, 두 그룹의 평균값의 차이가 크면 문제가 발생합니다.

왜냐하면, 평균값이 커질수록 산포도가 커지는 경향이 있기 때문입니다.

이러한 이유 때문에 표준 편차만을 이용해서 산포를 비교하는 것은 적절하지 않을 수 있기 때문에 이를 보완해주는 변동 계수(Coefficient of Variance)를 사용해야 합니다.

그렇다면 변동 계수란 무엇인지 자세히 알아보도록 하겠습니다.

## **What is Coefficient of Variance?**

---

변동 계수(Coefficient of Variance)는 평균값을 이용해 표준 편차를 보정해줍니다.

변동 계수를 구하는 식은 아래와 같습니다.

<br>

<center><img src="https://user-images.githubusercontent.com/97859215/206828124-ad3701c7-58dc-47b4-9168-e98e69d70284.png" width="500" height="250"></center>

> <center>변동 계수 구하는 공식</center>

<br>

위에서 말씀드렸다시피 변동 계수는 평균값을 이용해 표준 편차 값을 보정해주는 것을 알 수 있습니다.

조금 더 이해하기 쉽도록 하나의 질문에 대해 답해나가는 형태로 설명해드리도록 하겠습니다.

<br>

> 비교하는 두 그룹 A, B 중 B가 표준 편차가 더 큰 경우,  
> 반드시 B가 A보다 더 많이 분산되었다고 할 수 있나요?

<br>

우선, 답은 "아니요"입니다.

왜냐하면 평균값이 크면 표준 편차도 크기 때문입니다.

그래서 우리는 두 그룹을 표준 편차로 정확하게 비교하기 위해서는 변동 계수를 사용해야 합니다!

이번 포스팅을 통해 변동 계수란 무엇인지 알아보았습니다.

다음에도 좋은 내용을 담은 포스팅을 가져올 수 있도록 더욱더 노력하겠습니다!

긴 글 읽어주셔서 감사하다는 말씀드리며 글을 마치도록 하겠습니다.

감사합니다!