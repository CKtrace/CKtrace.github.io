---
layout: single
title: '[Statistics] 이항 분포 vs 초기하 분포 (feat. 야코프 베르누이)'
categories: Statistics
tag: [Statistics]
toc: true
author_profile: true
sidebar:
    nav: "docs"
---

**Purpose of this Posting**
- 이항 분포와 초기화 분포에 대해 알아봅니다.



## **베르누이 분포(Bernoulli Distribution)** 

---

<br>

> <center>베르누이 분포는 왜???</center>

<br>

__바로 베르누이 분포는 이항 분포의 기초가 되는 중요한 분포이기 때문입니다!__

<br>

||
|:---:|
① 시행에서 발생 가능한 결과는 2가지입니다.	
② 각 시행은 독립적으로 시행됩니다.
③  각 시행에서 결과의 확률은 항상 동일합니다.
①, ②, ③ 만족시키는 시행 -> 베르누이 시행(Bernoulli Trial)


베르누이 시행에서 결과 A와 결과 B가 있다고 할 때,  결과 A이면 0, 성공이면 1의 값을 갖는 확률변수 X와 확률분포는 아래와 같습니다.



<br>

<center><img src="https://user-images.githubusercontent.com/97859215/206619203-28d5f84f-3bc7-477d-8fa9-9c60906b1be7.png" width="300" height="100"></center>

<br>


이러한 확률 분포를 __베르누이 분포(Bernoulli Distribution)__ 라고 하고, 베르누이 분포를 따르는 따르는 확률 변수를 __베르누이 변수(Bernoulli Random Variable)__ 라고 합니다. 







## **이항 분포 (Binomial Distribution)**

---

시행에서 발생할 결과가 두 가지(R1, R2)인 베르누이 시행에서 확률 변수는 R1일 경우 1, R2일 경우 0인 베르누이 확률 변수를 갖는 시행이 있다고 해보겠습니다. 



R1일 확률이 p인 이 시행(베르누이 시행)을 n번 반복했을 때 R1 횟수의 분포를 __이항 분포(Binomial Distribution)__ 라고 합니다.  

<br>

<center><img src="https://user-images.githubusercontent.com/97859215/206619351-0edf4437-3604-47b6-a6a4-7c2ad6bc2329.png" width="700" height="100"></center>

> <center>이항분포의 일반식과 표현</center>



만약, 시행 횟수 n = 1이면 이항 분포는 베르누이 분포입니다.

> <center>쉽게 말해 이항 분포는 베르누이 시행을 한 번, 혹은 두 번 이상을 했을 때 어떤 결과가 나올 횟수의 분포입니다. </center>



베르누이 시행의 조건 ②(각 시행은 독립적으로 시행됩니다.)를 통해 이항 분포는 복원 추출을 통해 진행된다는 것을 알 수 있습니다. 그러면 비복원 추출을 통해 진행되는 것도 있겠죠...?

그것은 바로 초기하 분포입니다. 




## **초기하 분포(Hypergeometric Distribution)**

---


__초기하 분포(Hypergeometric Distribution)__ 에서의 시행은 베르누이 시행의 세 가지 조건 중 ②(각 시행은 독립적으로 시행됩니다.)이 충족되지 않은 시행입니다. -> 비복원으로 추출합니다.



한 마디로 이항 분포와 초기하 분포의 차이는 추출 방식에 있다는거죠!

이항 분포는 복원 추출! 초기하 분포는 비복원 추출!



초기하 분포의 구조를 이해하기 쉽도록 그림을 그려보았습니다!

<br>

<center><img src="https://user-images.githubusercontent.com/97859215/206619555-12b93de1-2d5f-4bc3-af27-1638d8fa6fb4.png" width="400" height="300"></center>

> <center>초기하 분포</center>



이제 초기화 분포란 무엇이고, 구조까지 알아보았으니 일반식도 한 번 알아보도록 하겠습니다.

(M : 부모 집단 A의 크기, N : 모집단의 크기, n : 시행 횟수, x : 시행 횟수 중에서 하나의 결과가 나올 횟수)

<br>

<center><img src="https://user-images.githubusercontent.com/97859215/206619613-930d0c3f-4bee-4a24-aa0e-755817b08b03.png" width="400" height="200"></center>

> <center>초기화 분포의 일반식</center>





여기서 한 가지 재밌는 생각이 들 수 있습니다.





> <center>초기하 분포를 이항 분포처럼 사용할 수는 없을까..?</center>




초기하 분포는 비복원 추출을 하기에 베르누이 시행에서 세 가지 조건 중 ②(각 시행은 독립적으로 시행됩니다.)이 충족되지 않은 시행을 한 것인데 이 조건만 충족해주면 베르누이 시행이고 초기하 분포를 이항 분포처럼 사용할 수 있지 않을까요..?



네. 초기하 분포를 이항 분포로 근사해서 사용할 수 있습니다!



단, 시행 횟수에 비해 모집단의 크기가 상대적으로 큰 경우에만 가능합니다.

∴ 시행 횟수(n)에 비해 모집단의 크기(N)가 상대적으로 크면 비복원의 효과가 적어서 베르누이 실험으로 근사되고, 초기하 분포는 p = M/n인 이항 분포로 근사되기 때문이죠~!





이렇게 해서 베르누이 분포, 이항 분포, 초기하 분포에 대해 알아보았습니다! 감사합니다!





