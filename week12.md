시그라프? 행사 - 매년 두 차례 열리는 행사(전세계의 개발자들, 아티스트, 시지 작업자들) 

논문, 기술 등 공유함

[Home Page | SIGGRAPH 2022](https://s2022.siggraph.org/)

# ✅ 실사에 3D 넣기 많이 활용됨


렌더 상에서 다 하려고 하지 말고 합성에서 텍스쳐나 variation 넣을 요소는 남겨두고 하는 게 시간 경제적임. 

→ 렌더를 두 개 관리해야 하지만 그래도 빠르고 편리

→ 합성에서도 충분히 텍스쳐나 그런거 충당 가능

** 크리토매트

cryptomatte 

** Rendering Setting _ Sampling

Camera (AA) 높인다고 좋은 게 아님 _ 노이즈 조금 나아지기 때문에 나중에 시간 오래 걸림 → 좋은 퀄리티를 보장하지는 않음

AOV 활용 잘 하면 좋음 ~~ → 사진 참고

## Unpremult & premult

사이에 컬러 관련 노드를 둬야 함 !!

why? 

⇒ unpremult 하면 확장 ? 거칠? → 그리고 나서 노드 grade … 하고 premult 하면 알파값을 봤을 때 알파가 조금 더 안쪽으로 들어옴 

그래서 grade. … 그런 설정들 외곽을 자연스럽게 살짝 깎으면서 premult 됨. 

** 초반부터 premult 하면 외곽에 검은 선 남을 수 있음 → 왜냐하면 처음부터 premult 하고 픽셀을 없앴기 때문

## ** log space → 뿌옇게 됨(black & white 업)

log 로 왜 찍느냐 → boost 미리 시켜두자 = 중간톤 영역을 확장시켜두는 의미

중간영역 contrast 강화

lin 2 log 노드 ~~~ 작업 하고 나서 다시 linear 로 바꿔줘야 함(원래 카메라 촬영시 사용되는 linear 로) log 2 lin 노드

→ 왜 바꾸느냐 : linear 로 누크에서 모두 다 바꿔줘야 함 ! 그래야 colorspace 가 일정해지기 때문. log 는 rgb 따로.. srgb …. 이러기 때문

## ** Shuffle

Add reflection

- arnold → 조명 합성
- merge divide 하면 빛 정보만 남게 됨
- uv 를 3디에다가 붙여주면 크기에 따라 챡 붙음..

## ** zdefocus

focal point 움직여주면서 차이 줄 수 있음

## ** Position to point NODE

position path → dot 점으로 바꿔주는 

인풋이 3개임 pos가 position input 임

normal → world normal path에 연결해주면 

⇒ 2디 render 도 3d render 로 바꿀 수 있음

—> why use : object 를 추가할 경우가 반드시 생기는데 → 3d data 가 오면 교수님이 주신 자료에서 카메라 랑 연결하면 됨

마야에서의 카메라 정보는 export selection - FBX !!  / USD / ABC 

알렌비 캐시??? 

마야에서 가져올 때는 camera 노드를 만들고 read ~
