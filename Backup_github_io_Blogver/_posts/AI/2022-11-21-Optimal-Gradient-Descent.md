---
layout: single
title: '[AI] 최적화 개념과 경사 하강법 원리 도출 과정'
categories: AI
tag: [AI]
toc: true
author_profile: true
sidebar:
    nav: "docs"
sitemap :
    changefreq : weekly
    priority : 1.0
---

**Purpose of this Posting**
- 최적화 개념과 경사 하강법 원리의 도출 과정에 대해 알아봅니다.



## **Optimization**

---



머신러닝 혹은 딥러닝은 실제 값과 예측 값 사이의 오차를 줄이는 것이 주목적입니다.



이때 오차를 확인하기 위한 함수를 손실 함수(목적 함수)라고 합니다.



즉, 손실 함숫값을 줄이는 것이 머신러닝 혹은 딥러닝의 주 목적이며 손실 함수 값을 최소화하는 파라미터를 찾는 과정이 바로 Optimization(최적화)입니다.



Optimization의 종류는 많지만 그중 가장 널리 알려진 Gradient Descent(경사 하강법)에 대해 알아보고자 합니다.




## **Gradient Descent**

---



Gradient Descent(경사 하강법)는 말 그대로 경사를 타고 이동하면서 최솟값을 갖는 지점을 찾는 기법입니다.



예를 들어 아래와 같은 2차 함수가 존재한다고 가정해보도록 하겠습니다.

<br>

<center><img src="https://user-images.githubusercontent.com/97859215/206484723-a593c02a-517f-4364-96de-d4eced9d6cb3.png" width="200" height="200"></center>

> <center>2차 함수와 경사 하강법</center>


위 그림은 2차 함수에서 빨간색 점이 하강하면서 최솟값을 갖는 극점을 찾아내는 과정을 나타낸 것입니다.

이와 같이 방향성과 속도를 갖고 최솟값을 갖는 지점을 찾는 것이 바로 경사 하강법입니다.


다음으로는 경사 하강법의 원리를 식과 함께 알아보도록 하겠습니다.




## **Principles of Gradient Descent -Ⅰ**

---



경사 하강법의 원리를 이해하기 위한 식의 전개를 진행하고자 합니다.



이해를 돕고자 최대한 식이 진행되는 과정을 생략 없이 진행하도록 하겠습니다.

(이해가 되지 않는 부분이 있으시면 댓글로 적어주시면 최대한 자세히 설명해드리도록 하겠습니다.)

<br>

<center><img src="https://user-images.githubusercontent.com/97859215/206484914-63059e83-f629-4873-92f3-bc92274d83be.png" width="400" height="100"></center>

> <center>미분과 도함수의 근사식</center>


∆x는 0과 거의 비슷한 값이 값이기 때문에 0으로 바꿔도 큰 차이는 생기지 않을 것이라고 생각해볼 수 있으며, 이때 극한의 개념을 제거하고 위와 같이 근사식을 사용 가능합니다.



이를 통해 아래와 같은 식을 유도해볼 수 있습니다.


<br>

<center><img src="https://user-images.githubusercontent.com/97859215/206485260-25a18dd0-bcdf-41da-8d50-f325be652e66.png" width="400" height="30"></center>

> <center>미분과 도함수의 근사식에서의 유도</center>



이때, 아래와 같은 자연 상수가 포함된 예를 들어보도록 하겠습니다.

<br>

<center><img src="https://user-images.githubusercontent.com/97859215/206485366-27688d4a-2a7c-4bb0-bb21-2e4455832415.png" width="200" height="30"></center>

> <center>f(x) = e^x</center>





이때 x에 0을 대입하고 ∆x에 x를 대입하면 아래와 같은 근사식을 구할 수 있습니다.

<br>

<center><img src="https://user-images.githubusercontent.com/97859215/206485538-af0380bc-cd5c-4ca3-b84b-0fde270850ef.png" width="300" height="300"></center>

<br>

이를 통해 x=0 근처에서 두 함수의 그래프는 겹쳐 있는 것을 확인 할 수 있으며, y=1+x가 y=e^x를 대체하는 근사식으로 유용하다는 것을 확인할 수 있습니다.


위에서 도출된 내용을 토대로 개념을 확장해 나가보도록 하겠습니다.








## **Principles of Gradient Descent -Ⅱ**

---



이번에는 다변수 함수의 근사식을 <Principles of Gradient Descent -Ⅰ>에서 도출된 내용을 확장시켜 알아보도록 하겠습니다.



f(x, y)라는 이변수 함수가 존재한다고 가정해보도록 하겠습니다.



그렇다면 아래와 같은 근사식을 도출할 수 있습니다.

<br>

<center><img src="https://user-images.githubusercontent.com/97859215/206485736-9552cde0-dc42-4947-9d01-85d68d0d82d6.png" width="400" height="50"></center>

> <center>이변수 함수의 근사식</center>



위 근사식을 이용하여 ∆z를 정의해보도록 하겠습니다.

<br>

<center><img src="https://user-images.githubusercontent.com/97859215/206485926-fa93567d-f01a-4d87-8651-5bca7a8106fb.png" width="300" height="30"></center>

> <center>∆z 정의</center>



그렇다면 ∆z는 x, y를 각각 ∆x, ∆y만큼 변화시켰을 때 함수 f(x, y)의 변화라는 것을 알 수 있습니다.



정의한 ∆z를 이변수 함수의 근사식을 나타낸 식에 대입하면 아래와 같이 간결하게 표현이 가능합니다.

<br>

<center><img src="https://user-images.githubusercontent.com/97859215/206486162-ec29859d-b498-4580-a7b3-7cc8f03f184e.png" width="300" height="60"></center>

> <center>∆z를 이용한 간결한 표현</center>



위 식을 통해 변수가 늘어나도 식 서술에 더욱 용이합니다.

예를 들어 변수 z가 변수 x, y, z 총 세 개의 변수를 포함하는 함수일 때 근사식을 나타내면 아래와 같습니다.

<br>

<center><img src="https://user-images.githubusercontent.com/97859215/206486261-5a90cb42-3504-4316-a4c5-f82a2ebd299f.png" width="300" height="60"></center>

> <center>삼변수 함수일 때의 근사식</center>



이렇게 도출된 식은 아래와 같이 벡터로도 표현이 가능합니다.


<br>

<center><img src="https://user-images.githubusercontent.com/97859215/206486384-2b6a19bb-0aab-4750-b1ef-572ab8f5bf03.png" width="300" height="60"></center>

> <center>벡터 표현</center>


위 ∇z와 ∆X를 내적하면 근사식이 도출되는 것 또한 알아낼 수 있습니다.


다음으로는 위와 같이 내적의 성분을 표시하는 벡터로 나타낸 식을 이용해 경사 하강법의 원리의 끝으로 도달해보도록 하겠습니다!



  
## **Principles of Gradient Descent - Ⅲ**

---



위에서 열심히 f(x), f(x, y)를 지지고 볶고를 반복해보았습니다.



이번에는 그냥 함수 말고 손실 함수를 한 번 지지고 볶는다고 생각해보도록 하겠습니다.



결국은 같은 변수를 가진 "함수"이기 때문에 앞서 알아본 내용을 그대로 적용하면 될 것이기 때문에 큰 어려움 없이 이해하실 수 있을 것입니다!



어떤 손실 함수는 변수를 x_1 ~ x_n까지 갖는다고 가정해보도록 하겠습니다.



위에서 알아본 근사식을 이용하여 이 손실 함수의 근사식을 벡터로 표현해보면 아래와 같습니다.

<br>

<center><img src="https://user-images.githubusercontent.com/97859215/206486576-b6e7a6b0-8142-4aa3-b19c-8023fea4be5a.png" width="300" height="60"></center>

> <center>손실함수의 근사식 벡터 표현</center>





이 또한 동일하게 ∇z와 ∆X를 내적 하면 근사식이 도출되는 것을 알았는데, 이때 근사식이 무엇이었는지 다시 한번 짚고 넘어가 보도록 하겠습니다.



<Principles of Gradient Descent - Ⅰ>의 처음으로 근사식을 나타낸 식을 보시면, 좌변이 f(x)의 미분 함수인 것을 확인할 수 있습니다.



즉,  ∇z와 ∆X의 내적 값이 0이라면 그곳이 바로 극점일 것입니다.



그렇다면 두 벡터를 내적을 할 때 두 벡터의 방향이 반대인 경우에 내적 값이 최소가 되는 성질을 이용하여 아래와 같은 새로운 식을 도출할 수 있습니다.


<br>

<center><img src="https://user-images.githubusercontent.com/97859215/206486725-40fa2377-5b46-4a58-a6aa-fd6eb319d0a9.png" width="500" height="60"></center>

> <center>최종 도출 식</center>




최종으로 도출된 위 식이 바로 경사하강법의 기본 식입니다.



이때 ɳ는 작은 값을 갖는 양의 상수이자 보폭이라고 생각하면 됩니다.


즉, ɳ 값이 너무 크면 최솟값을 뛰어넘어버리는 경우가 생기고, 너무 작으면 최솟값을 찾는데 소요되는 시간이 상당히 걸립니다.


그렇기 때문에 ɳ의 값을 적절하게 설정해야 합니다.








## **Conclusion**

---

이렇게 해서 경사 하강법의 원리를 알아보았습니다.

아무래도 어려운 내용이기에 최대한 쉽게 풀어나가 보고자 어떤 글보다 고심하며 적어 내려 갔던 것 같습니다.

혹시라도 이해가 안 되는 부분이 있으시면 편하게 댓글로 여쭤봐 주시면 정성껏 답글로 설명해드리도록 하겠습니다.



더욱더 좋은 글로 찾아뵙도록 하겠습니다.

긴 글 읽어주셔서 감사합니다!