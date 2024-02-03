+++
title = '4일만에 자바스크립트로 만든 직관력 테스트'
date = 2024-02-01T10:26:34+09:00
draft = false
+++
## 바닐라 자바스크립트로 테스트/퀴즈 만들기
승현님과 한팀으로 4일동안 열심히 만든 '직관력 테스트'의 개발 후기를 작성해보려 한다.<br>
이 테스트는 2명이서 개발을 했기 때문에
현재 수강중인 강의에도 뒤쳐지지 않으면서 진행 하려면<br>
많은 기능 구현으로 높은 퀄리티를 지향 하기보다는
끝까지 완주하는 것과 자바스크립트의 실력 향상을 목표로 하자며 프로젝트에 돌입했다.<br>
<br>
![](https://velog.velcdn.com/images/greysu1/post/9b8745b3-ad72-42c6-a674-97d4786ea3b6/image.png)
<br>
<br>

## 1. 아이디어 기획
첫날 하루정도는 각자 어떤 테스트(or 퀴즈)를 할지 생각해 보았고
총 3가지 주제가 나왔다.<br>
<br>

### 1. 짱구는 못말려 심리테스트
![](https://velog.velcdn.com/images/greysu1/post/e3ca23dc-f289-4f5f-9a64-fca1323946a4/image.png)
  - 짱구와 훈이, 철수, 맹구 등 짱구는 못말려에 나오는 캐릭터들의 성격을 빗대어
    <br>소심한 성격인지 대범한지 성향을 알아보는 테스트인데 개인적으로 이런 테스트는 귀여운 캐릭터들로 아기자기하게 만들면 어린 학생들한테 인기가 있지 않을까 싶다.
    <br>
### 2. 무한도전 밈 테스트
![](https://velog.velcdn.com/images/greysu1/post/383abb00-d940-4af6-94cc-01bd771724e4/image.png)
  - 역대 무한도전에서 유명한 짤들을 가져온 뒤 자막을 지우고 당시 어떤 대사를 쳤는지 맞추는   테스트이다. 이것도 만들면 재미있었을거 같은데 하나만 선택해야 하니 패스했다.<br>
   (개인적으로 혼자 만들어 볼 예정)
    <br>
### 3. 직관력 테스트
  - 일반적으로 생각하는 테스트(mbti테스트 등..)와 차별화를 두고 싶어 이색 테스트를 알아보다가 이 테스트를 알게 되었고 직감적으로 답을 선택하는 게 꽤 재밌어 보였다. <br>
  난 모든 아이디어가 다 좋았고 승현님께 다음날까지 주제를 선택해주시기를 요청드렸다.

<br>
<br>

## 2. 디자인 & 퍼블리싱

  우리팀은 '직관력 테스트'를 만들어보기로 결정했고 디자인은 승현님이, 퍼블리싱은 내가 맡았다.
  ![](https://velog.velcdn.com/images/greysu1/post/cad0e284-f9b6-4e54-95bc-cfb88b9152b2/image.png)
  ![](https://velog.velcdn.com/images/greysu1/post/d0107170-a84e-4b6d-8fbc-fa3be4626394/image.png)
  
  <br>
  역시 전공자셔서 그런지 심플하면서 귀여운 캐릭터가 돋보이는 디자인이다.<br>
  내가 직접 디자인했으면 이 정도는 못했을것 같다.<br>
  아무튼 피그마로 작업한 디자인을 참고해 퍼블리싱에 들어갔다.<br>
  복잡한 구조의 컨테이너는 없었기에 퍼블리싱 작업 역시 수월하게 진행되었다.<br>
<br>

## 3. 자바스크립트 기능 구현

  이 직관력 테스트에 들어가야 할 대표적인 기능 몇가지가 있었다.<br>
  ### 1. 메인페이지에서 초조함(?)을 끌어올릴 bgm 재생 기능
   ![](https://velog.velcdn.com/images/greysu1/post/69e3b53b-a1eb-4cf9-8787-e109d6b758b9/image.png)<br>
  ### 2. 각 문제당 3초의 카운트다운, 프로그레스 바
  ![](https://velog.velcdn.com/images/greysu1/post/e890ae67-dac1-4907-9d7d-8e698af3680b/image.png)<br>
  ### 3. 결과페이지에서 합산한 점수(이미지, 문구)출력 / 정답 확인 모달창
  ![](https://velog.velcdn.com/images/greysu1/post/42b47c7d-5e7d-4f32-8132-7d316951f7ef/image.png)<br>
  <br>
  직관력 테스트이니 3초안에 답을 선택해야 하는 게 더 어울리고 또 재밌을거 같았다.<br>
  
## 4. 어려웠던 부분들

  우선 SPA(Single page application)방식으로 하나의 html파일로 개발을 시작했고
  display:"none" 으로 다음페이지로 넘어가는 것처럼 구현을 했다.

  ![](https://velog.velcdn.com/images/greysu1/post/55fa5587-18e0-4d0a-8c40-9865fc6b90c1/image.png)
  <br>
  JS파일들은 이렇게 나눴는데 멘토님이 잘한거라고 말씀해주셨다.👍<br>
  다른 건 어려워도 잘 넘어갔는데 꽤 오랜시간 정체되어 있던 부분이 있다.<br>
  ![](https://velog.velcdn.com/images/greysu1/post/9081574f-07b2-46e0-b61b-fefdf9e06927/image.png)
  <br>
  이런식으로 question이라는 배열안 img,question,option을 각 객체로 담고<br>
  option은 또 하나의 배열이고 그 안에 2개의 객체로 담았는데<br>
  문제는 정답을 클릭했을 때는 1점, 틀린 답을 클릭했을 때는 0점으로 합산을 하려고<br>
  해당 객체의 값들을 출력하려는데 계속해서 undefined가 뜨거나<br>
  모든 문제의 보기가 1번 문제의 보기만 출력되는 부분에서 많은 어려움을 느꼈다.<br>
  
  ![](https://velog.velcdn.com/images/greysu1/post/27d1874d-158f-413d-91db-1dfe653d3c91/image.png)
  <br>
  보기를 선택했을 때 이 함수를 실행하는데<br>
  let currentButtonindex = 0; 으로 초기화를 하고<br>
  위에 qustions배열의 길이 동안 options라는 변수에 option배열을 담고<br>
  다시 그 배열에 forEach메서드로 selectBtns라는 빈 배열에 담았다.<br>
  <br>
  그리고 button을 만들어서 클래스명 choice를 add하고 innerHTML로<br>
  보기(answer)를 출력했다.<br>
  <br>
  <br>
  그렇게 겨우 한 고비를 넘기고 보니 다음 문제가 기다리고 있었다.<br>
  그 문제는 3초 출력이었는데 마지막 문제를 stepIndex = 10;이라고 했을때<br>
  해당 조건으로 setTimeout을 통해 로딩페이지로 넘기고 로딩페이지에서 다시 한 3초 대기 후<br>
  결과 페이지 이동이었는데 클릭을 안하고 3초뒤에 넘어 갔을때는 9번 문제에서 바로 로딩페이지로<br>
  넘어간 뒤에 결과페이지로 갔고,<br>
  버튼을 클릭했을 때는 정상적으로 넘어갔다.<br>
  <br>
  문제는 **마지막 문제의 보기를 클릭했을때와 3초가 지나서 자동으로 넘어갔을 때**<br>
  각각의 setTimeout이 꼬였던 것 같다.

  ![](https://velog.velcdn.com/images/greysu1/post/881abf34-fe4d-442f-b686-c3d26a672055/image.png)

  원래는 위 사진에서 하나의 조건문 안에 각각의 setTimeout을 넣었는데<br>
  사진과 같이 조건문을 분리해서 적용시키니 원하는대로 작동되었다.<br>
  사실 이 setTimeout은 더 다뤄봐야 자세히 알것 같다.<br>
  분명히 문제는 해결됐는데 "어째서 되는거지?"하는 찝찝한 의문이 들기 때문이다...<br>
  해결방안을 100% 완벽하게 이해하고 있지 않다는 뜻😭
<br>
<br>
  ## 5.팀 프로젝트를 하면서 느낀 점

  혼자 했을때 장점도 분명 존재하지만 같이 했을때의 시너지는 이루 말할 수 없었다.<br>

  객체로 각 보기에서 보기와 점수를 부여하는 부분도 승현님의 코드를 보고 뒤늦게 깨달았다.<br>
  나는 배열로 작업을 시작했는데...
  되게 사소하지만 이런 디테일한 부분에서<br>
  분명하게 내가 팀원에게 배웠다고 느꼈고 이래서 팀 과제를 해봐야 하는구나 싶었다.<br>
  <br>
  그리고 디자인적인🎨 부분도 혼자 했으면 미리캔버스로 대충 이미지 만들어서 했겠지만<br>
  승현님이 디자인을 전공하셔서 사실상 웹개발 공부중인 웹디자이너와 팀을 먹고 과제를 진행한거라<br>
  디자이너, 퍼블리셔, 개발자 등 협업자들 역할의 중요성도 간접적으로나마 깨닫게 되었다.<br>
  <br>
  마지막으로 "우리가 했다" 이 하나만으로 팀 프로젝트의 필요성을 제대로 느꼈다.<br>
  프론트엔드 2기분들과는 너무나도 어색한 사이이기 때문에 *유난히도 내성적인 나*는<br>
  혼자 하려고 했다가 멘토링 같은 조(면서 바로 앞자리에 계신)인 승현님도 따로 팀 구성을 하신것 같지 않아서 먼저 DM으로 물어보았고 흔쾌히 수락해주셔서 같이 하게 됐는데<br>
  결과적으로 우리가 한 팀으로 끝까지 했다는 것만으로도 난 엄청난 자신감이 생겼다.<br>
  완성도는 꽤 떨어질 수 있지만 우리 수준에서 끝까지 해낸 것, 그거 하나만으로도<br>
  "나는 팀으로도 할 수 있구나", "나는 spa방식으로 웹페이지를 만들 수 있구나" 하며<br>
  나 자신에 대한 믿음이 생기는 계기가 되었다.<br>
  
  ---
  
  곧 리액트를 배우고 나면 팀 프로젝트를 제대로(?)하게 될거 같은데
  그 전에 경험삼아 해 본 미니 프로젝트로 다음에 또 기회가 된다면
  이런 작은 규모의 팀 프로젝트를 또 해보고 싶다.


  ### 직관력 테스트 해보고 싶으신 분들은 👉 https://intuition-test.netlify.app