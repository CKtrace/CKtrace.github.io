---
title: '[AI] 인공신경망의 편향과 활성화 함수'
layout: post
categories: ai
tags: AI
comments: true
---

**Purpose of this Posting**
- 인공 신경망의 활성화 함수와 매개변수인 편향에 대해 알아봅니다. 



## **What is Bias?**

---


<center><img src="https://user-images.githubusercontent.com/97859215/206476624-3e4e0889-440c-461c-83f3-3ec2db0aa6bd.png" width="400" height="150"></center>

> <center>출력 신호 전달 여부 표현식</center>


출력 신호 전달 여부는 각 입력 신호와 가중치의 곱의 합이 임계값 이상이면 신호를 전달하고, 임계값 미만이면 신호를 전달하지 않습니다.

이 식을 변형해보면 조금 다른 방향으로 해석이 가능합니다.

<br>

<center><img src="https://user-images.githubusercontent.com/97859215/206477038-4ef8a055-fb51-4d74-978e-e8dfeef6086e.png" width="400" height="200"></center>

> <center>변형된 출력 신호 전달 여부 표현식 - (1)</center>



위 식과 같이 "- (임계값)"을 "+b"로 치환할 수 있으며, 이때 b를 편향(Bias)라고 합니다.



그렇다면 변형된 식을 이용하여 출력 신호 여부를 표현해본다면 아래와 같이 나타낼 수 있습니다.

<br>

<center><img src="https://user-images.githubusercontent.com/97859215/206478554-e8269192-4cca-46c0-8e33-acf2470f7ea2.png" width="400" height="150"></center>

> <center>변형된 출력 신호 전달 여부 표현식 - (2)</center>


  

단순 모형으로 표현해보면 아래와 같이 편향을 하나의 입력 신호로 볼 수 있으며, 이때 가중치는 1이라고 볼 수 있습니다. 

<br>

<center><img src="https://user-images.githubusercontent.com/97859215/206479056-2d025f61-0f43-4a2c-8055-5df620a0f6cd.png" width="400" height="300"></center>

> <center>단순 모형으로 표현한 신호 전달 과정</center>





## **What is Activation Function?**

---


먼저 이전 포스팅에서 뉴런의 신호 전달 과정을 알아보았습니다.


이때 출력 신호는 0 또는 1이었지만, 이것은 생물학적인 관점에서 바라보았기 때문입니다.

(이 부분에 대해 좀 더 자세히 알아보고 싶으신 분은 이전에 작성했던 제 포스트를 참고하시면 도움이 되실 것이라 생각이 들어 첨부하도록 하겠습니다!)

+ [이전 포스팅 알아보기](https://cktrace.github.io/ai/2022-11-07-Artificial-Neural-Networks/)




생물학적인 관점을 배제하고 인공신경망의 출력 신호를 생각해보았을 때, 출력 신호가 0 또는 1로 굳이 이분법적으로 표현하지 않아도 됩니다.


이러한 생각을 충족시켜주는 함수 a가 있다고 가정해보도록 하겠습니다.

<br>

<center><img src="https://user-images.githubusercontent.com/97859215/206479788-4de28028-f918-4b12-a0bc-cab46aff6f41.png" width="300" height="100"></center>

<br>


위의 식과 같이 함수를 a를 적용해줄 수 있으며, 사용자가 함수 a를 어떻게 설정하느냐에 따라 출력 신호의 범위나 출력 신호의 값이 변할 수 있습니다.



대표적인 활성화 함수 중에는 시그모이드(Sigmoid) 함수가 존재합니다.


<br>

<center><img src="https://user-images.githubusercontent.com/97859215/206480065-5b827683-6d4b-446e-a409-d77bf4e82891.png" width="500" height="300"></center>

> <center>Sigmoid Function</center>




예를 들어, 임의의 함수 a를 시그모이드 함수로 설정한다면, 출력 값은 0과 1 사이의 값이 도출될 것입니다.



이때, 출력 값이 0에 가까울수록 흥분도(or 반응도)가 낮다고 보고, 1에 가까울수록 흥분도(or 반응도)가 높다고 생각합니다.



물론 임의의 함수 a는 시그모이드 함수 뿐만 아니라 값이 증가하는 미분 가능 함수로 대체해도 가능합니다.



그렇다면, 여기서 아래와 같은 의문이 들 수 있습니다.



> 기존의 계단 함수를 이용해도 출력 값이 나오는데
굳이 미분 가능한 함수인 활성화 함수를 사용해야 하는 이유가 무엇일까?




활성화 함수 아직까지는 왜 써야하는지 정확하게 와닿지 않으신 것이 당연합니다.



이번 포스팅에서는 활성화 함수가 이런거고 이렇게 적용을 해볼 수가 있구나 정도만 이해하셨다면 충분합니다.



추후 포스팅에서는 활성화 함수를 왜 써야 하는지 알아보도록 하겠습니다.











이상으로 글을 마치도록 하겠습니다.



더욱 더 좋은 글로 다시 찾아뵙도록 하겠습니다.



감사합니다.









