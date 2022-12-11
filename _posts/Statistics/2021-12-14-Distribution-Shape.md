---
layout: single
title: '[Statistics] 분포의 형태 (왜도 & 첨도)'
categories: Statistics
tag: [Statistics]
toc: true
author_profile: true
sidebar:
    nav: "docs"
---

**Purpose of this Posting**
- 분포의 형태에 대해 알아봅니다.


## **분포의 형태**

---

수치형 자료에 대한 통계 분석 방법

→ 대부분 모집단의 중심 위치를 기준으로 좌우 대칭 형태를 가진다고 가정!

통계 분석의 적절성

→ 분석 방법에서의 가정한 조건을 얼마나 자료가 만족을 하는지에 영향을 받습니다.

분포 형태에 대한 측도

→ 자료가 모집단의 가정을 얼마나 만족하는지 확인이 필요합니다 -> 왜도와 첨도를 통해 확인!

## **왜도 (Skewness)**

---

자료의 중심 위치를 기준으로 좌우 중 한 쪽으로 쏠렸는지 확인할 수 있게 해주는 척도입니다.

→ 이상치(중심에서 많이 떨어져 있는 값)가 있는지 점검할 수 있습니다. 즉, 정규 분포인지 아닌지 확인할 수 있게 해주는 것이죠.

→ Histogram(히스토그램) 또는 Box plot(상자 그림)을 통해서 왜도를 확인할 수 있습니다.

→ '꼬리가 길다.'라는 것은 이상치를 가지는 자료가 있다는 것입니다.

<br>

<center><img src="https://user-images.githubusercontent.com/97859215/206621415-8fcf4d61-dd10-4c71-93b1-1c2892aa6d60.png" width="700" height="170"></center>

> <center>왜도 (Skewness)</center>

## **왜도 공식**

---

<center><img src="https://user-images.githubusercontent.com/97859215/206621546-b6a57cd0-48f9-476d-a21f-2211dc757913.png" width="300" height="100"></center>

> <center>왜도 공식 (s = 표준 편차)</center>

<img src="https://user-images.githubusercontent.com/97859215/206621642-6bfcf8f6-3239-4cfe-a443-432cbc6f330c.png" width="100" height="50">

\->  이 식을 통해 나온 평균을 중심으로 왼쪽이 음수, 오른쪽이 양수입니다.

자료 평균에서 멀어지면 멀어질수록 큰 양수 혹은 큰 음수가 됩니다.

\-> 이때 중심으로부터 많이 떨어진 값이 이상치인 것입니다.

<img src="https://user-images.githubusercontent.com/97859215/206621758-11c082fe-bf34-4656-ab57-3149f6ec26e6.png" width="50" height="50">

 평균 값을 중심으로 왼쪽과 오른쪽의 형태가 비슷하면 비슷할수록 음수와 양수가 상쇄되어 이 값이 0에 근사하거나 0이 됩니다. 즉, 대칭성을 띄는 것이죠!

## **왜도 내용 마무리**

---

<center><img src="https://user-images.githubusercontent.com/97859215/206621812-6f548ba7-c6b7-4f44-bb2e-cda0143ebd67.png" width="1000" height="50"></center>

## **첨도 (Kurtosis)**

---

얼마나 자료가 뾰족한지 확인하게 해주는 척도입니다! 왜도와 마찬가지로 첨도도 이상치의 유무를 점검하는데 쓰입니다.

<br>

<center><img src="https://user-images.githubusercontent.com/97859215/206621893-6aef8b70-b702-46a5-95f2-39d67f0f39e3.png" width="700" height="170"></center>

> <center>왼쪽부터 정점이 낮고 완만한 자료, 표준 정규 분포인 자료, 정점이 높고 뾰족한 자료</center>

위 그림의 왼쪽에 위치한 자료처럼 정점이 낮고 완만한 자료는 중심 위치가 변할 가능성이 높습니다!

## **첨도 공식**

---


<center><img src="https://user-images.githubusercontent.com/97859215/206621992-fc7d7126-be5f-4908-9f4c-a7c4e3419e42.png" width="300" height="100"></center>

> <center>첨도 공식 (s = 표준 편차)</center>

<img src="https://user-images.githubusercontent.com/97859215/206622082-ce492eec-d5e0-4283-a0d5-ffedfb449985.png" width="100" height="50">

\-> 이 식을 통해 나온 평균을 중심으로 자료가 멀리 있으면 큰 값입니다.

첨도는 항상 양수가 되고, 정점의 높이에 따라 꼬리 부분이 얼마나 두터운지에 영향을 많이 받습니다!

(중심보다는 정점의 높이에 따라!)

첨도 공식에서 3을 빼주는 이유는 정규 분포일 때의 첨도가 3이기 때문입니다!

## **첨도 내용 마무리**

---

<center><img src="https://user-images.githubusercontent.com/97859215/206622174-13f7a66f-af79-4bb6-8c0d-0caa5137b9bb.png" width="1000" height="50"></center>

<br>

이렇게 해서 왜도와 첨도에 대해 알아보았고 긴 글을 읽어주셔서 감사하다는 말씀드리며 글을 마치도록 하겠습니다.

감사합니다!