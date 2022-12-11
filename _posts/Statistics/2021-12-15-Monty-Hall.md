---
layout: single
title: '[Statistics] 몬티홀 문제 (Key : 조건부 확률)'
categories: Statistics
tag: [Statistics]
toc: true
author_profile: true
sidebar:
    nav: "docs"
---

**Purpose of this Posting**
- 몬티홀 문제에 대해 알아봅니다.


## **What is 'Monty Hall Problem'**

---

<Let's Make a Deal>이라는 미국 오락 프로그램에서 유래한 조건부 확률에 관련된 확률 문제입니다.

|    **Suppose you’re on a game show, and you’re given the choice of three doors. Behind one door is a car, behind the others, goats. You pick a door, say #1, and the host, who knows what’s behind the doors, opens another door, say #3, which has a goat. He says to you, "Do you want to pick door #2?" Is it to your advantage to switch your choice of doors?**       |

☞ 게임쇼에 나가서 세 개의 문을 선택했다고 가정해보세요. 한 문 뒤에는 차, 다른 문 뒤에는 염소들이 있습니다. 당신이 1번 문을 고르면, 문 뒤에 뭐가 있는지 아는 호스트는 염소가 있는 3번 문을 엽니다. 그는 당신에게 "2번 문을 고르고 싶으세요?"라고 말합니다. 당신이 선택한 문을 바꾸는 것이 당신에게 유리합니까?

이 문제는 아주 유명한 문제로 아마 많은 분들이 이미 들어보거나 실제로 풀이해보신 분들이 계실 겁니다.

지금부터 그 유명한 몬티홀 문제를 직접 풀이해보도록 하겠습니다!

## **Premise & Rule**

---

풀이를 해보기 앞서서 몬티홀 문제의 전제와 룰에 대해 설명하도록 하겠습니다.

| <전제> |
| --- |
|   -   사회자는 염소가 뒤에 있는 문을 임의로 선택합니다. -   사회자는 어느 문 뒤에 자동차가 존재하는 알고 있습니다.   |

| <룰> |
| --- |
|   -   문 3개 중 하나의 문 뒤에는 자동차가 있고, 나머지 문 뒤에는 염소가 있습니다. 참가자는 3개의 문 중 하나의 문을 골라 문 뒤에 있는 상품을 갖습니다. -   참가자가 문을 선택하면 선택하지 않은 문 중 염소가 뒤에 있는 문을 열어 염소를 보여줍니다. -   그리고 참가자가 처음으로 선택한 문 대신 다른 문으로 바꿀 수 있는 기회를 줍니다.   |

## **Solution Explanation**

---

몬티홀 문제의 풀이 핵심은 조건부 확률입니다.

제가 작성한 조건부 확률 관련 포스팅을 참고하시면 이해하시는데 조금 더 도움이 될 것 같습니다!

[CKtrace의 조건부 확률 관련 포스팅](https://cktrace.github.io/statistics/2021-12-11-Bayes'-theorem/)

우선 몬티홀 문제를 풀기 위해 두 가지 경우를 두고 풀도록 하겠습니다.

> 첫 번째, 처음 선택한 문을 바꾸지 않는 경우

사건 X : 선택한 문을 제외한 두 문 중 호스트가 하나의 문을 여는 사건

사건 X가 일어날 확률 : P(X) = 1/2

사건 Y : 자동차가 처음으로 선택한 문 뒤에 있는 사건

사건 Y가 일어날 확률 : P(Y) = 1/3

<br>

<center><img src="https://user-images.githubusercontent.com/97859215/206622748-e0aa2677-df01-463c-ace2-efb5b4b2866b.png" width="400" height="150"></center>

> <center>처음 선택한 문을 바꾸지 않고 자동차를 얻을 확률을 구하는 식</center>

<br>

사건 X, Y가 일어날 확률들과 조건부 확률을 이용해 처음 선택한 문을 바꾸지 않고 자동차를 얻을 확률은 1/3입니다.

> 두 번째, 처음 선택한 문과 다른 문을 최종으로 선택하는 경우  
>   

사건 X : 선택한 문을 제외한 두 문 중 호스트가 하나의 문을 여는 사건

사건 X가 일어날 확률 : P(X) = 1/2

사건 Y : 자동차가 처음 선택한 문과 호스트가 연 문을 제외한 문 뒤에 있는 사건

사건 Y가 일어날 확률 : P(Y) = 1/3

사건 Z : 자동차가 처음 선택한 문과 호스트가 연 문을 제외한 문 뒤에 있을 때 호스트가 문을 여는 사건

사건 Z가 일어날 확률 : P(Z) = P(X | Y) = 1 

<br>

<center><img src="https://user-images.githubusercontent.com/97859215/206829690-f888891b-f472-430b-822d-58c692d6310a.png" width="400" height="150"></center>

> <center>처음과 다른 문을 선택했을 때 자동차를 얻을 확률을 구하는 식</center>

<br>

## **Solution Explanation +**

---

트리 형식의 그림을 추가하여 이해를 좀 더 쉽게 도와드리는 것이 좋을 것 같다는 판단이 들었습니다.

두 경우를 그림으로 나타낸 것과 각각의 경우에 해당하는 식과 함께 보시면 이해하기 더 쉬울 것입니다.

<br>

<center><img src="https://user-images.githubusercontent.com/97859215/206622884-af7f7747-b4d6-4d99-84d3-5abb2cde9018.png" width="500" height="400"></center>

> <center>첫 번째 경우</center>

<br>

<br>

<center><img src="https://user-images.githubusercontent.com/97859215/206622817-98d9deb2-87c7-4a7d-a3fc-01ff2c41ae24.png" width="500" height="400"></center>

> <center>두 번째 경우</center>

<br>

## **Conclusion**

---

확률 계산에 따르면 몬티홀 문제에서 처음 선택한 문과 다른 문을 최종적으로 선택하면 자동차를 가져갈 확률이 2배 높다는 것을 알 수 있습니다. 

즉, 확률상 참가자가 처음 선택한 문과 다른 문을 최종으로 선택하면 2배 높은 확률로 자동차를 획득할 수 있는 것이죠.

이렇게 해서 몬티홀 문제와 풀이에 대해 알아보았고 긴 글을 읽어주셔서 감사하다는 말씀드리며 글을 마치도록 하겠습니다.

감사합니다!