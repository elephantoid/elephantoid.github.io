---
title: "[Learning] Simple RNN"
date: 2020-10-30
#pemalink: /clouders/
tages: [RNN, Deeplearning, Machinelearning]
header:
  #image: "/assets/images/IBM.jpeg"
excerpt: "RNN, Deep learning, Machine learning"
---

# H1 RNN(Recurrent Neural Network)


# H2 들어가기 앞서,,,
가정해봅시다. 특정한 날에 저녁으로 저는 중국집에 전화를합니다.
중국집 배달 규칙 = 짜장 짬뽕 볶음밥 순으로 시킵니다. 
저번주에 짬뽕을 시켰다면 오늘은 볶음밥을 시켜야 할테고
저번 주에 짜장을 시켜먹었다면 오늘은 짬뽕을 시켜먹는 날이 될 것입니다.
여기서 한 가지 더 나아가보자면 2일 후으로 넘어가는 것입니다.
<img width="343" alt="중식배달규칙" src="https://user-images.githubusercontent.com/70086728/97666865-e224b980-1ac1-11eb-80e0-eda29612f78b.PNG">
2일 전에는 짜장을 먹었습니다. 그럼 하루 전에는 짬뽕을 먹어야한다고 _예측_ 할 테고 오늘은 볶음밥을 먹어야한다고 _예측_ 할 것입니다. 왜냐면 저희의 중국집 배달 규칙은 그대로 이기 때문입니다. 
컴퓨터에서 오늘 볶음밥을 먹어야한다는 것을 예측한 것을 one_hot vector로 표현하자면 [0,0,1]이 됩니다. 

# H2 RNN이란?
순환 신경망은 인공 신경망의 한 종류로, 유닛간의 연결이 순환적 구조를 갖는 특징을 갖고 있다. 이러한 구조는 시변적 동적 특징을 모델링 할 수 있도록 신경망 내부에 상태를 저장할 수 있게 해주므로, 순방향 신경망과 달리 내부의 메모리를 이용해 시퀀스 형태의 입력을 처리할 수 있다.


앞서 말했던 대로 RNN의 기본 개념(Concept)
1. 벡터로 구성된 시퀀시 데이터를 인풋으로 넣고 + RNN결과는 히스토리가 있는 이전 결과의 아웃풋
2. 은닉층(Hidden layer)가 과거의정보로 루프가 반복되고 그걸 통해서 미래를 예측하는 방법입니다.
3. 아웃풋은 Softmax layer이며 다음 단계를 위해서입니다. 

간단한 Fomula
<img width="504" alt="포뮬라" src="https://user-images.githubusercontent.com/70086728/97666899-f799e380-1ac1-11eb-82e9-89ed9a0aec53.PNG">
이 모델을 어떻게 활용할 수 있을까요?

# H2 예제

<img width="446" alt="다양한모델들" src="https://user-images.githubusercontent.com/70086728/97666924-07192c80-1ac2-11eb-989a-5802b8b998ff.PNG">
one to one - Classification
one to many - Image Caption(image > sequence of words)
many to one - Sentiment Classification
many to many - Machine Traslation(구글번역기)
             - Video Calssfication on frame level


# H2 References

출처:[위키백과], [link][https://ko.wikipedia.org/wiki/%EC%88%9C%ED%99%98_%EC%8B%A0%EA%B2%BD%EB%A7%9D]? 

출처:[link][https://calvinfeng.gitbook.io/machine-learning-notebook/supervised-learning/recurrent-neural-network/recurrent_neural_networks]?

[link][https://www.youtube.com/watch?v=WCUNPb-5EYI&t=129s&ab_channel=BrandonRohrer]?