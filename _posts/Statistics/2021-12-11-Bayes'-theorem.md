---
layout: single
title: '[Statistics] 베이즈 정리'
categories: Statistics
tag: [Statistics]
toc: true
author_profile: true
sidebar:
    nav: "docs"
---

**Purpose of this Posting**
- 베이즈 정리에 대해 알아봅니다.


<center> 본 포스팅에서 사건 A와 사건 B가 존재한다고 가정하고 시작하겠습니다! </center>






## **feat. 조건부 확률 (Conditional Probability)**
---



사건 A가 발생할 때 사건 B가 발생할 확률 = P (A \| B) -> 이때 이 확률이 __조건부 확률__ 입니다.



P (A \| B)는 사건 A에서 A∩B가 차지하는 비율입니다. 


<br>

<center><img src="https://user-images.githubusercontent.com/97859215/206615885-4fe70745-9ca6-4331-8878-cc4808c0e947.png" width="300" height="70"></center>

<br>



자, 그러면 이 식을 활용해볼까요?


<br>

<center><img src="https://user-images.githubusercontent.com/97859215/206615959-9e527c68-331d-430c-96b8-fac2857d6585.png" width="300" height="70"></center>

<br>

 





## **feat. 독립 사건 (Independent Events)**
---


사건 A와 사건 B가 각자 발생함에 있어 서로 영향을 주지 않을 때 사건 A와 B는 __독립 사건__ 이라고 합니다. 



그렇다면 위에서 설명한 조건부 확률의 개념을 다시 한번 생각해봅시다.



조건부 확률은 사건 A가 발생할 때 사건 B가 발생할 확률입니다. 이때 사건 A와 사건 B는 독립 사건이라면 서로 발생함에 있어 영향을 주지 않죠? 그러면 아래 수식처럼 된다는 것을 우리는 알 수 있습니다.


<br>

<center><img src="https://user-images.githubusercontent.com/97859215/206616063-80d7dff0-d92d-46f2-8a3e-b6bb3867b7d7.png" width="300" height="70"></center>

<br>



그렇다면 아래 수식을 통해 이때 사건 A와 사건 B는 독립사건일 때 P(A∩B)를 알아봅시다!




<br>

<center><img src="https://user-images.githubusercontent.com/97859215/206616107-9c29adf5-90bb-41a2-9722-a48dc340002c.png" width="300" height="200"></center>

<br>




## **Main. 베이즈 정리(Bayes’ theorem)**

---


자... 이제 __베이즈 정리__ 를 들어가보도록 하죠! (feat. 조건부 확률, 독립 사건의 힘이 발휘될 때입니다...)



사건 A가 일어났을 때 사건 B가 일어날 확률이 조건부 확률이었죠?



베이즈 정리는 사건 A를 원인으로 보고 사건 A가 일어났을 때 사건 B가 일어날 확률 예측 과정에서 사용되는 공식입니다. 공식은 아래 수식과 같습니다.






위 공식의 이해를 돕기 위해 수식을 하나 더 추가해보겠습니다.



<br>

<center><img src="https://user-images.githubusercontent.com/97859215/206616211-50314992-bb7b-467e-bf67-bdb3bce23264.png" width="300" height="70"></center>

<br>





> 어... 어디서 봤는데...

네. 맞습니다.

feat. 조건부 확률에서 우리가 활용해본 수식이였죠!



베이즈 정리가 무엇인지 알아보았으니 이제 이리저리 풀어볼까요?



그전에 P(B)가 어떻게 풀어헤쳐지는지 알아봅시다!



<br>

<center><img src="https://user-images.githubusercontent.com/97859215/206616298-4bcdfbab-693c-4bd2-bf34-3edcdc21a73c.png" width="500" height="100"></center>

<br>


P(B)가 어떻게 풀어헤쳐지는지 알아보았으니 이제 베이지 정리를 풀어헤쳐보고 글을 마무리 짓도록 하겠습니다~!

## **Conclusion**
---


<br>

<center><img src="https://user-images.githubusercontent.com/97859215/206616366-0f855b8f-08e3-4b80-80a0-0425f68a2165.png" width="600" height="100"></center>

<br>






