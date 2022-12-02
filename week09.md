# 📌 중간과제 Feedback

</aside>

- 커스틱
- 완전 그린이면 오히려 크로마키 잘 안 빠짐 → 그래서 소스 잘 확인하기
- 3D 작업을 하면 바로 렌더링 돌려도 됨 → 누크에서 알파값을 인지하고 있으므로
- frame range 정하면 over 되지 않게 작업 가능
- time offset 노드 → 원하는프레임까지 정할 수 있음
- actionvfx → 학생용으로 구독가능할 거라고 예상.

⇒ 소스 여기서 찾으면 좋음 / 무료 소스들도 있음

[ActionVFX | The Best Stock Footage for Visual Effects](https://www.actionvfx.com/)

- 흑백→ 알파로 바꿀 수 있음 how? ⇒ channel r g b a 각각으로 바꿀 수 있는데
    
    ex. 소스가 그린이 거의 없으면 shuffle 에서 그린을 알파로 연결해주면 됨
    
    ⇒ black screen source 도 그럼 찾아볼 만 하겠다
    
- 마이클 베이 감독 + 놀란 감독 → VFX 효과 대신 실제로 터뜨린다고 함
- surface imperfections - 사물의 리얼리즘을 위해 활용 가능

[Surface Imperfections](https://surfaceimperfections.com/)

- 안경같은 경우에는 따로 작업을 해줘야 함(뚫리는 경우_크로마키)
- 뒤에 배경이 픽셀화 된다면 앞에도 그렇게 맞춰줘야 함
- 카메라 움직임을 준다면 뒤에 블러링을 준다면 앞 대상에 포커스 가능
- god ray node → 빛을 비춰주는 듯한 느낌
- 인물 넣을 때 주의점 : grade로 복제해서 그림자 만들고  transform, 바닥 투명도 조절
- 생동감 주는 방법 : 비행기, 새 들어가면 무조건..? 그래보임 / 꽃이 흔들리거나(로토따야함)
- idistort node → 가만히 있는 것에 뭔가 물에 비치는 듯한 표현 만들어주라고 하면
- 폭발 터뜨릴 거면 주변에도 그 색상과 비슷하게 비추도록 해줘야 함(빛 신경쓰기)
- noise node 도 있음
- roto 로 영역 지정하고 noise node 활용하면 연기처럼 보임(크기를 늘리면 구름처럼도 활용 가능!)
- volume ray node 랑 noise node 많이 같이 활용함
- 깜빡이는 효과 → 실제처럼 연출하고 싶으면 네온사인이나 깜빡이게 하면 좋음
- 공간 뒤로 뺄 때 날라가는 새같은 경우 레이어 하나로만 뒤로 보냈어도 좋았을 듯

**기말과제** 

2d tracking 3d tracking 공부하기

1024 1024

16:9 or 1:1 세로도 가능 → 나중에 인스타에 업로드 될 거임

포맷은 중간과제 때와 동일_ mov h.264
