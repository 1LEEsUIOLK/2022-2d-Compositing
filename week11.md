# ✅ Tracking → Motion Blur 넣어줘야 자연스럽


- tracker 는 따로 노드를 때 두는 게 좋음
- transform  & transform matchmove → 이런 식으로 같은 노드 컬러인 거는 겹쳐서 하면
- 해상도 낮추고 싶으면 원본에다가 reformat 노드 주기

- 얼굴 교체 작업 많이 하는데 로토 → e 키 주면
- merge 에서 union 말고 B box에 맞추면 → 바운딩박스 정리 가능
- shuffle 은 가능한 한 원본 바로 밑에 두는 게 좋음
- transform node 나 다른 노드도 마찬가지로 노드 탭에다가 각각 설명 적어두면 좋음
- alt e 누르면 연결된 초록 선 사라짐
- postage stamp → 선 정리하는 노드 ! ⇒ Read 노드를 굳이 복사하지 않아도 되는 ~ , 렌더링 속도 줄고 메모리 줄고,. 가이드 노드
- grade 같은 것도 로토로 따서 비치는 거 다 표현 해주면 더 좋음 !!!

# ✅ 수업

- cornerpin 2개를 활용해서 핸드폰 화면 같은 경우를 확대해서

cornerpin2D2 2-match screensize

cornerpin2D1 1- from tracker

- cornerpin 해상도가 from 으로 보면 그냥 해상도가 들어가서 그래 보이는 것(원본보다 넘어가 보이는 것)

⇒ set to input 을 누르면 크기 맞춰짐 ! 

from - input 해상도

to - 새로운. ~~

copy from 누르면 from 에 있는 값이 넘어옴

맞춰지고 나서 수동적으로 하나하나 옮겨서 맞춰주면 됨 → 수동으로 맞추다가 밀리는 것들 보이면 키를 잡아줘야 함(레퍼가 되는 프레임을 잡고 파라미터 set 키를 잡아주면 됨)

누크 preference - auto 키가 잡혀 있어서 자동으로 키가 잡힐 거임

transform stabilize 노드 → 사용하면 고정된 곳에서 트래킹 맞춰주고 나중에 영상 움직이게 할 수도 있음

invert 라는 버튼을 눌러주고 하면 

핸드폰 화면때문에 비치는 초록빛은 디스필 

# ✅ 3d


3d 소스 있으면 → readgeo 누르면 바로 불러올 수 있음

scene 에다가 card, cube, sphere 등 을 이어주면 됨

 * 마야에서 텍스쳐, 라이팅 한 거 불러올 때 라이팅은 따로 맞춰줘야 할 것임

3d 같은 경우 position, rotate, scale 다 각각 노드에다가 transform geo 해주는 편 - 교수 피셜

card - 스케일이랑 같이 뒤로 갈수록 depth 조절됨

투사할 이미지 → project3D

Projection cam → project3D

2개를 이어줘야 함

(그냥 캠은 렌더링 용 카메라 노드임~)

project3D에서 card 하나 이어주고 정육면체의 저 먼 벽이라고 생각했을 때 하나 만들어 주고 

또 하나 카드 만들어서 옆 면을 만들어주겠다 하면 그 사진을 옆으로 돌려줘서 (3디 상에서) 벽 세워주고

프로젝션 캠은 카드들을 투사하는 역할이고 

그냥 캠은 최종적으로 ㅂ라보게 될 캠

⇒ 2디를 3디처럼 할 수 있ㅇ는 좋은 방법 ! 저절로 모션블러도 조금 되서 좋음

⇒ 공간을 만들어 놓고 3디만 얹어 놓을 때에도 유용함 (깊이가 이미 있으니까)
