# Feedback

### Ibk gizmo

- Image based Keyer
- 장점 : Keylight 보다 더 키가 잘 빠짐
- Gizmo 를 사용해서 배경에 들어가는 greenscreen 을 만든다.
- 그린 배경과 얹어져 있는 이미지의 차이를 이용해서 키를 빼내는 방식

 

### Key light

- Fill other color into original one(image)

Grade - channel alpha 

grade - channel alpha로 바꿀 수 있는데 

이렇게 하고 grain 조절하면 = 알파 조절

y key를 조절해서 확인  알파 값에 0.00000 이런 식으로 뜨면 완벽히 안 빠짐

** original -

huecorrect - rgb change nono  요렇게 해보기

<img width="527" alt="스크린샷 2022-12-01 오후 7 45 13" src="https://user-images.githubusercontent.com/114202118/205033018-ed553204-218a-46e3-98aa-4ee1dfed29ba.png">

ctrl + alt  → color more key make

미세하게는 이렇게 하면 좋지만

소개해준 대로 하면 dispill 빠르게 가능

원본은 그대로 내려오고 키 작업을 해서 알파를 빼놓으면 거기다가 원본이랑 이어주고 

filter erode → 소프트 매트랑 합칠 건데 외곽에 영향을 받을 수 있어서 살짝 erode로 줄여주기

<aside>
👻 Github _ Lumapictures 가면 많은 유용 정보 많음

</aside>

## 단축키 Shift S 누르면 Preferences 창이 뜸

nodes  - new merge nodes connect A input 끄기 (그러면 추가되는 것에 A 바로 넣을 수 있으니까)

<img width="443" alt="스크린샷 2022-12-01 오후 7 45 30" src="https://user-images.githubusercontent.com/114202118/205033084-d66b5578-fb5c-4b90-8614-3131260d4de8.png">

- Nodes - Tab Search Menu - Favorites → if you want it use it
- Nodes - Tab Search Menu - Weighting  → professor don’t use

<img width="533" alt="스크린샷 2022-12-01 오후 7 45 49" src="https://user-images.githubusercontent.com/114202118/205033162-4c2c72a0-fa93-4478-8559-c7b81881a7cf.png">

- Professor changed it into 60 GB.
- localize one → green up above the ‘read’ file → it helps your work speed up

# Grade

blackpoint - spoid

whitepoint. -spoid 

→ green part increase 

## lift

블랙에 영향이 많이 가고 밝은 부분에는 영향이 안 감

어두운 정도를 맞춰줘야 함 → 그러고 나서 gain

## gain

밝은 영역에 많은 영향을 줌 

그래서 높여주면 밝은 부분이 확 밝아짐

multiply = gain  비슷(가능하면 gain 수치를 먼저 잡고 multiply 로 보정하는 방식 추천)

## Offset

위의 값들이 통째로 이동한다는 개념

<img width="528" alt="스크린샷 2022-12-01 오후 7 46 04" src="https://user-images.githubusercontent.com/114202118/205033210-b0f23af8-609a-4d0a-9e16-0e9211f39790.png">

## Gamma

중간톤을 관리하는 커브

Prof. → 가능한 한 don’t change any value

## Black clamp / white clamp

8bit work → values should be in 0~1 value

ex. G&B 1을 넘어가는 경우 —> 나중에 저장 시 최대인 1로만 나옴

White(node) 

# Constant → format 맞춤

Matte-paint 할 때 밑 배경이라고 생각하면 됨

merge → original & constant

<img width="528" alt="스크린샷 2022-12-01 오후 7 47 22" src="https://user-images.githubusercontent.com/114202118/205033493-3fbc2c76-c160-45a4-8524-c8122c8017bf.png">

크기 해상도 안 맞을 경우

set bbokx to → B

## transform → reformat

## reformat → transform

→ filter 맞춰주기(위아래 수직으로 되어 있는 노드들 끼리)

# Concatenation node

[Naver Dictionary] Concatenate : 사슬같이 잇다; 연쇄시키다

Summary _ filter 자동 한번에 계산해서 원본훼손을 최소화 하면서 작업가능

Concatenation 노드는 transform 노드가 일렬 상에 반복해서 사용될 경우, 필터를 거치며 원본이 훼손되는 과정을 막기 위해 인접한 transform 노드들 중 가장 마지막의 필터 노드만 작용하도록 하는 기능을 한다. 

Ex. 일렬 상의 transform 노드를 개별 하나씩 적용하지 않고 가장 마지막의 노드에 해당 필터의 기능이 Read 노드에서 적용됨을 뜻한다. 

<img width="260" alt="스크린샷 2022-12-01 오후 7 47 45" src="https://user-images.githubusercontent.com/114202118/205033581-e11797e8-8559-4567-a137-5305a77e8d87.png">

## Grade → 명도로 색 맞춰주면 됨

(rgb 각각으로 들어가서 확인 )

## Colorcorrect

Prof. -채도만 많이 쓰심

## Appendclip - 다음 컷 다른 경우 이어줌

## **참고 사이트 : Nuke is fun.com**

# 출처

Dimension explanation  <[Visualizing the Fourth Dimension - Research Blog (duke.edu)](https://researchblog.duke.edu/2017/04/26/visualizing-the-fourth-dimension/)>

Color explanation <[RGB vs CMYK: What's the Difference? (99designs.com)](https://99designs.com/blog/tips/correct-file-formats-rgb-and-cmyk/)>

Alpha Channel definition <[알파 채널 (naver.com)](https://terms.naver.com/entry.naver?docId=852484&cid=42346&categoryId=42346)>

