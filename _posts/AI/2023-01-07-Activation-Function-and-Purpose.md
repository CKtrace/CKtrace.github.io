---
layout: single
title: '[AI] 활성화 함수와 활성화 함수의 사용 목적'
categories: AI
tag: [AI, Deep Learning from Scratch]
toc: true
author_profile: true
sidebar:
    nav: "docs"
sitemap :
    changefreq : weekly
    priority : 1.0
---

**Purpose of this Posting**
- 활성화 함수란 무엇이고, 사용 목적에 대해 알아봅니다.

## **About Activation Function and Purpose of Using it**

활성화 함수란 입력 신호의 총합을 출력 신호로 변환하는 함수입니다.

즉, 입력 신호와 편향의 총합을 바로 출력하는 것이 아니라 이 값을 활성화 함수를 거쳐 새롭게 산출되는 값이 출력값이 되는 것입니다.

그렇다면 아래와 같은 의문이 들 수 있습니다.

> <center> 활성화 함수를 사용하지 않아도 신호가 출력되는데 굳이...? </center>

의문에 대한 답변으로는 활성화 함수를 사용하지 않으면 층을 깊게 하는 의미가 없기 때문입니다.

더 자세히 말하자면, 신경망에서 활성화 함수를 사용하지 않거나, 활성화 함수로 선형 함수를 이용하면 신경망의 층을 깊게 하는 이유가 없어지기 때문입니다.

이해를 돕기 위해 한 가지 예를 들어보도록 하겠습니다.

선형 함수 a(x) = cx를 활성화 함수로 사용하여 3층 신경망을 구현한다고 가정합니다.

본 가정을 식으로 나타내면, y(x) = a(a(a(x))) = c * c * c * x = c^3 * x 가 됩니다.

그런데 c * x 는 선형 함수이므로, c^3 * x 또한 선형 함수로 됩니다.

또한, c^3 을 p 로 치환하면 y = p(x) 로 나타낼 수 있습니다.

즉, hidden Layer(은닉층)이 없는 신경망으로 표현할 수 있기에 선형 함수나 활성화 함수를 사용하지 않으면 여러 층으로 쌓는 이점이 없습니다.

정리하면, 신경망의 층을 쌓아 혜택을 얻고자 한다면 활성화 함수를 비선형 함수로 설정해야 합니다.

이제 활성화 함수와 사용 목적에 대해 알아보았으니, 여러 종류의 활성화 함수와 구현을 해보도록 하겠습니다.


## **Step Function**

**Step Function Expression**

신경망에서 사용하는 계단 함수는 입력이 0을 넘으면 1을 출력하고 그 외에는 0을 출력하는 함수입니다.

<center><img src="https://user-images.githubusercontent.com/97859215/211146426-771df643-57ba-4800-86a0-3bacedd71f9b.png" width="400" height="160"></center>

<br>

**Step Function Shape**

<center><img src="https://user-images.githubusercontent.com/97859215/211146773-530f145b-3572-44d9-8f5e-e1483d4c55db.png" width="300" height="300"></center>

<br>

**Step Function Code Implementation**

```py
import numpy as np

def step_function(x):
    return np.array(x > 0, dtype = np.int)
```


## **Sigmoid Function**

Sigmoid 함수는 신경망에서 자주 사용하는 활성화 함수입니다.

계단 함수의 출력은 0 또는 1인 반면에 Sigmoid 함수의 출력은 실수를 돌려준다는 차이점이 존재합니다.

_(Sigmoid 함수를 거친 배열의 원소들의 총합은 1이 아닌 점을 유의해주세요.)_

하지만 두 함수 모두 입력 값이 작은 경우 출력은 0에 가깝고, 입력 값이 큰 경우 출력은 1에 가깝다는 공통점 또한 존재합니다.


**Sigmoid Function Expression**

<center><img src="https://user-images.githubusercontent.com/97859215/211146636-792628d9-71ea-4fa7-b77f-61b12cacf12b.png" width="400" height="160"></center>

<br>

**Sigmoid Function Shape**

<center><img src="https://user-images.githubusercontent.com/97859215/211147207-8b0036e9-557d-4ffa-9ff5-a1b808520c5f.png" width="300" height="300"></center>

<br>

**Sigmoid Function Code Implementation**

```py
import numpy as np

def sigmoid(x):
    return 1 / (1 + np.exp(-x))
```


## **ReLu Function**

이전에 Sigmoid를 설명드릴 때 신경망에서 자주 사용하는 활성화 함수라고 설명을 드렸었습니다.

최근에는 ReLu를 주로 이용한다고 합니다.

하지만, Sigmoid와 ReLu 모두 자주 사용하는 활성화 함수임은 틀림없습니다.

**ReLu Function Expression**

<center><img src="https://user-images.githubusercontent.com/97859215/211147677-c0282181-7638-4c0d-9aa1-7d7cfe116687.png" width="400" height="160"></center>

<br>

**ReLu Function Shape**

<center><img src="https://user-images.githubusercontent.com/97859215/211147988-fe69fa3c-a187-4e2b-bdc7-b7a99ea7149a.png" width="300" height="300"></center>

<br>

**ReLu Function Code Implementation**

```py
import numpy as np

def relu(x):
    return np.maximum(0, x)
```


## **Softmax Function**

Softmax 함수는 분류 문제에서 자주 사용되는 활성화 함수입니다.

_(회귀 문제에서는 출력층의 활성화 함수로 항등 함수를 주로 사용합니다.)_

Sigmoid와 달리 해당 함수를 거쳐 재구성된 배열의 원소 총합은 1이 됩니다.

일반적으로 Softmax는 출력층에 사용하는데, 각 원소는 정답일 확률이라고 생각하면 될 것 같습니다.

**Softmax Function Expression**

<center><img src="https://user-images.githubusercontent.com/97859215/211149179-1020d93e-bfb2-4f02-b44c-67b7eae9714d.png" width="400" height="100"></center>

<br>


**Softmax Function Code Implementation**

위 Softmax Function의 수식을 코드로 구현할 때는 주의할 점이 있습니다.

Softmax의 수식을 확인하시면 자연 상수의 제곱이 존재하는데 만약 e^1000이면 무한대 값이 출력되고 이렇게 큰 값들 간의 나눗셈을 진행하면 결과 값이 불안정해집니다.

그래서 아래와 같은 식의 변형이 필요합니다.

<center><img src="https://user-images.githubusercontent.com/97859215/211150456-79700562-0428-485a-b2d9-db3ccab788b5.png" width="600" height="700"></center>

<br>

변형된 식을 코드로 구현하면 아래와 같습니다.

```py
import numpy as np

def softmax(a):
    c = np.max(a)
    exp_a = np.exp(a - c)
    sum_exp_a = np.sum(exp_a)
    y = exp_a / sum_exp_a

    return y
```








## **Conclusion**

---

이렇게 활성화 함수란 무엇이고, 사용 목적에 대해 알아보았습니다.

혹시라도 이해가 안 되는 부분이 있으시면 편하게 댓글로 여쭤봐 주시면 정성껏 답글로 설명해드리도록 하겠습니다.

더욱더 좋은 글로 찾아뵙도록 하겠습니다.

긴 글 읽어주셔서 감사합니다!

<br>
<br>

_본 포스팅은 [밑바닥부터 시작하는 딥러닝]을 공부하고 정리한 것입니다._