---
layout: single
title: '[AI] 퍼셉트론과 퍼셉트론의 한계'
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
- 퍼셉트론이란 무엇이고, 퍼셉트론의 한계에 대해 알아봅니다. 또한 퍼셉트론의 한계를 


## **About Perceptron**

퍼셉트론은 다수의 신호를 입력으로 받고 하나의 신호를 출력하는 알고리즘입니다.

AI 파트에서 퍼셉트론을 알아보는 이유는 신경망의 기원이 되는 알고리즘이기 때문입니다.

결과는 신호 출력 여부로 두 가지의 값을 가질 수 있습니다.
(신호가 흐른다 / 신호가 흐르지 않는다)

<center><img src="https://user-images.githubusercontent.com/97859215/210366640-8c68adda-13de-4be1-98a3-ad2a6122628c.png" width="300" height="300"></center>

> <center>2개의 입력을 소유한 퍼셉트론</center>


이때 $ x_1 $ 과 $x_2$ 은 입력 신호이며, $w_1$ 과 $w_2$ 는 가중치입니다. 또한 $y$ 는 출력 신호입니다.

각각의 입력 신호에 해당 가중치가 곱해진 값들의 합이 임계값 $theta$ 를 넘을 시에만 1을 출력합니다.

위와 같은 과정을 식으로 나타내면 아래의 그림과 같습니다.

<center><img src="https://user-images.githubusercontent.com/97859215/210367906-89d0a7c9-61b2-4ffb-a57c-3a1706c7e1bc.png" width="200" height="80"></center>

<br>

이때, 가중치 값의 크기에 따라 해당 신호의 중요도가 달라집니다.

가중치의 값이 크면 해당 신호의 중요도는 크다는 것이고, 가중치의 값이 작으면 해당 신호의 중요도는 작다는 것입니다.

위 식에서 임계값을 $-b$ 로 치환하고 왼쪽 변으로 이항해주면 아래의 식으로 표현해줄 수 있습니다.

<center><img src="https://user-images.githubusercontent.com/97859215/210371780-297dc892-ddd1-4534-9f97-a1db4a72489f.png" width="200" height="80"></center>

$b$ 를 편향이라 하며 재구성한 식을 해석해보면 퍼셉트론은 각각의 입력 신호에 해당 가중치가 곱해진 값에 추가적으로 편향을 합한 값들의 합이 0보다 크거나 같을 때 1을 출력한다는 것입니다. 

편향의 값은 노드(뉴런)이 얼마나 쉽게 활성화하느냐, 즉 얼마나 쉽게 1이란느 결과를 출력하느냐를 조정하는 매개변수입니다. 

퍼셉트론으로 구현 가능한 AND Gate, NAND Gate, OR Gate가 존재하며, 각각의 Gate의 출력 결과와 코드 구현 방법에 대해 알아보고 퍼셉트론의 한계를 알아보도록 하겠습니다.


## **AND Gate** 

AND Gate는 두 개의 입력, 하나의 출력을 가집니다.

AND Gate는 두 개의 입력 모두 1인 경우에만 1을 출력하고 이외의 경우에는 모두 0을 출력합니다.

입력 신호와 출력 신호의 대응 표를 진리표라 하며, AND Gate의 진리표는 아래와 같습니다.

| $x_1$ | $x_2$ | $y$ |
|:---:|:---:|:---:|
|0|0|0|
|0|1|0|
|1|0|0|
|1|1|1|

AND Gate를 코드로 구현하기 위해서는 각 신호에 해당하는 가중치, 임계값, 편향을 지정해주면 됩니다. 

```py
import numpy as np

def AND(x1, x2):
    x = np.array([x1, x2])
    w = np.array([0.5, 0.5])
    b = -0.7

    tmp = np.sum(w*x) + b

    if tmp <= 0:
        return 0
    else:
        return 1
```


## **NAND Gate** 

NAND Gate는 Not AND를 의미하며 AND Gate의 출력을 뒤집은 것입니다.

즉, 두 입력 신호가 1인 경우를 제외하고 모두 1을 출력하는 것입니다.

NAND Gate의 진리표는 아래와 같습니다.

| $x_1$ | $x_2$ | $y$ |
|:---:|:---:|:---:|
|0|0|1|
|0|1|1|
|1|0|1|
|1|1|0|

NAND Gate 또한 코드로 구현하면 아래와 같습니다.

```py
import numpy as np

def NAND(x1, x2):
    x = np.array([x1, x2])
    w = np.array([-0.5, -0.5])
    b = 0.7

    tmp = np.sum(w*x) + b

    if tmp <= 0:
        return 0
    else:
        return 1
```


## **OR Gate** 

OR Gate는 두 입력 신호 중 하나라도 입력 신호가 1인 경우에 1을 출력하는 Gate입니다.

OR Gate의 진리표는 아래와 같습니다.

| $x_1$ | $x_2$ | $y$ |
|:---:|:---:|:---:|
|0|0|0|
|0|1|1|
|1|0|1|
|1|1|1|

OR Gate 또한 코드로 구현하면 아래와 같습니다.

```py
import numpy as np

def OR(x1, x2):
    x = np.array([x1, x2])
    w = np.array([0.5, 0.5])
    b = -0.2

    tmp = np.sum(w*x) + b

    if tmp <= 0:
        return 0
    else:
        return 1
```


## **XOR GATE & Limitation of Perceptron** 

퍼셉트론의 한계는 앞서 알아본 Gate의 결과와 XOR Gate의 결과를 시각적으로 비교해보면 알 수 있습니다.

<center><img src="https://user-images.githubusercontent.com/97859215/210391661-ec26c726-0b49-4322-85d9-a3e9094a5309.png" width="300" height="300"></center>

> <center>AND Gate</center>

<br>

<center><img src="https://user-images.githubusercontent.com/97859215/210392584-eaed4167-033b-4c4b-9ffa-daf6c21fd028.png" width="300" height="300"></center>

> <center>NAND Gate</center>

<br>

<center><img src="https://user-images.githubusercontent.com/97859215/210393058-b9854377-f429-4ec9-bb52-aef797d71ec9.png" width="300" height="300"></center>

> <center>OR Gate</center>

앞서 알아본 세 가지 Gate를 시각적으로 나타내면 위와 그림들과 같은데 세 그림에서의 공통점을 확인할 수 있습니다.

바로 직선으로 두 영역을 나눌 수 있으며, 각각의 영역 중 하나는 1을 출력하고 하나는 0을 출력합니다.

그런데, Gate 중에 __XOR Gate__ 가 존재하는데 본 게이트는 입력 신호 중 하나만 1일 때 1을 출력합니다.

XOR Gate의 진리표는 아래와 같습니다.

| $x_1$ | $x_2$ | $y$ |
|:---:|:---:|:---:|
|0|0|0|
|0|1|1|
|1|0|1|
|1|1|0|

또한 XOR Gate를 AND Gate, NAND Gate, OR Gate와 같이 시각적으로 나타내면 아래와 같습니다.

<center><img src="https://user-images.githubusercontent.com/97859215/210397546-e4e0927a-5e1e-4a32-8b67-0d0cb8baac24.png" width="300" height="300"></center>

> <center>XOR Gate</center>

위 사진을 통해 AND Gate, NAND Gate, OR Gate와 차이점이 존재한다는 것을 알 수 있습니다.

바로 차이점은 직선으로 두 영역을 나눌 수 없다는 것입니다.

만약 두 영역을 나누고자 한다면 아래와 같이 곡선을 이용해야 합니다.

<center><img src="https://user-images.githubusercontent.com/97859215/210399265-3b462693-b96b-428c-88ac-1d8aea8ee076.png" width="300" height="300"></center>

> <center>XOR Gate</center>


정리를 하자면, 직선의 영역을 선형 영역이라 하고 곡선의 영역을 비선형 영역이라 합니다.

또한 퍼셉트론은 직선 하나로 나눈 영역만 표현할 수 있다는 한계가 존재합니다.

이러한 한계는 퍼셉트론을 _"층을 쌓아"_ 해결할 수 있습니다.

<center><img src="https://user-images.githubusercontent.com/97859215/210401778-5cad9aa7-2376-4e3f-ad22-0da8601679b7.png" width="300" height="300"></center>

> <center>XOR 퍼셉트론</center>

가중치를 갖는 층이 2개이므로, XOR 퍼셉트론을 2층 퍼셉트론(다층 퍼셉트론)으로 부른다면, AND 퍼셉트론, NAND 퍼셉트론, OR 퍼셉트론은 1층 퍼셉트론(단층 퍼셉트론)입니다.

이런 구조때문에 XOR 퍼셉트론은 퍼셉트론을 층을 쌓아 한계를 해결한다고 하는 것입니다.

XOR Gate는 단층 퍼셉트론인 AND 퍼셉트론, NAND 퍼셉트론, OR 퍼셉트론을 조합하여 구현할 수 있으며, 이를 코드로 구현하면 아래와 같습니다.

```py
import numpy as np

def XOR(x1, x2):
    s1 = NAND(x1, x2)
    s2 = OR(x1, x2)
    y = AND(s1, s2)

    return y
```

정리하자면, 단층 퍼셉트론으로 구현 불가한 것은 층을 늘려 구현 가능하다는 것이며 단층 퍼셉트론은 직선 영역만 구현 가능하고, 다층 퍼셉트론은 비선형 영역도 표현 가능합니다.








## **Conclusion**

---

이렇게 해서 퍼셉트론, 퍼셉트론의 한계와 해결 방법에 대해 알아보았습니다.

혹시라도 이해가 안 되는 부분이 있으시면 편하게 댓글로 여쭤봐 주시면 정성껏 답글로 설명해드리도록 하겠습니다.

더욱더 좋은 글로 찾아뵙도록 하겠습니다.

긴 글 읽어주셔서 감사합니다!

<br>
<br>

_본 포스팅은 [밑바닥부터 시작하는 딥러닝]을 공부하고 정리한 것입니다._