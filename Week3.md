Week3
---

Q. VFX 에서는 왜 누크를 사용할까?

A. 아마 Rotoscoping 과 3D Digital Matte Painting and 3D compositing 때문에 쓰이는 듯하다.


# Visual Language 



# Matte Painting

1. **Matte Painting 이란?**

: 두 개의 화면을 합성할 때, 인물과 합성하기 위해 유리 면에 배경 화면을 그리는 일.

(=미리 세트로 구성하기 어려운 것을 페인트하는 방식)

<img width="336" alt="스크린샷 2022-10-03 오후 10 46 15" src="https://user-images.githubusercontent.com/114202118/193593412-d81deb55-49d8-4ef2-aef2-eaff446353fb.png">

ex. paint on glass _ 마치 레이어처럼 겹겹이 쌓이는
___
2. **How it works?**

First, plate glass with paintnig of specific part of structure 

Second, combine the picture of paining with real structure

Third, film the combined picture of painting and real structure with camera

<img width="620" alt="스크린샷 2022-10-03 오후 9 00 44" src="https://user-images.githubusercontent.com/114202118/193571887-e338ac03-eb45-41da-babc-da8da7b51855.png">

The black part would be an **Alpha area** which distinguish the painting and the real ones.
___
3. **기타 설명**

- 배경 촬영이 어려운 시절/CG 기술이 부족하던 시절, background 묘사를 위해 사실적인 화풍으로 배경을 미리 그렸다.

- 세트를 확장(Set extension)하고 넓은 배경(large environment)을 대체하기 위한 수단으로도 사용되었다. 

(검은 부분 = alpha)

<img width="630" alt="스크린샷 2022-10-03 오후 10 06 37" src="https://user-images.githubusercontent.com/114202118/193583854-09b7ddce-9983-4d41-93eb-fa9fb8f053f2.png">

ex. Star Wars _ many soldiers in the background

ex. 구인공고 matte painter(spinvfx) _ photorealistic painting 가능 + concept drawing 

<https://www.spinvfx.com/careers/matte-painter/>

- Matte Painter

Albert Whitlock _ 가장 유명한 Matte Painter 중 1명

<img width="209" alt="스크린샷 2022-10-04 오전 1 09 12" src="https://user-images.githubusercontent.com/114202118/193626178-add1b2a7-a95f-4e32-ae21-d3adb8fd63fb.png">

그는 1929년, 14살의 어린 나이때부터 matte painter 로서의 삶을 살기 시작했다.

Alfred Hitchcock 와 일하기도 했으며 그때 미니어쳐 작업을 했는데 그 작품은 The Man Who Knew Too Much(1934) 이다.

2차 세계대전이 발발할 당시, 그는 월트 디즈니에 들어가 유니버셜 스튜디오로 들어가기 1961년 전까지 Matte 부서에서 일했다. 

그의 가장 훌륭하다고 평가받는 작품은 Disaster Film Earthquake(1974) 이고, 알버트는 이 작품을 통해 아카데미 수상도 이뤘다. 

그 다음 해 오스카 상도 수상하는 등 그는 matte painter 로서의 명성을 유지했다. 


# Photoshop 

**작업 시 주의사항**

1. 배경부터 그리는 것 추천

Far(atmosphere set/concept set) > mid > near

멀리 있는 물체 및 배경부터 작업하므로써 분위기와 그 작업의 컨셉을 잡아두면 나중이 편해진다.

2. 가깝고 중간 멀리 있는 것들을 각각의 레이어로 나누면 좋다. 

3. Layer mask 는 다른 파일로 export 할 때에는 같이 안 온다 -> 같은 layer 로 merge 해야 함.

4. 신경쓸 것들

light / adjust layer / RGB channel / film noise(grain) effect use

___

**Thing that you should know about ALPHA CHANNEL** 

- You should be aware of alpha channel b/c it differs your work depending on how you use it.

- Alpha could go bad occuring **BLACK FRINGING** which is some kind of bothersome error.

<img width="1266" alt="스크린샷 2022-10-03 오후 11 31 21" src="https://user-images.githubusercontent.com/114202118/193603388-bf63416f-7b08-4899-9802-e509644726d6.png">

- If you do not set an alpha channel on an image, the image will have black around its edges where the semi transparent pixels are. 

- But if you set an alpha channel on an image, it would have full pixels where the semi transparent pixels are. 

That is, ALPHA CHANNEL helps us to divide an image with no leftover pixels that would make an image imperfect.


___
# **출처**

Matte Painting definition <https://ko.dict.naver.com/#/search?query=matte%20painting>

3주차 수업자료 pdf_Images & Description

Matte Painter_Albert Whitlock <https://www.imdb.com/name/nm0926087/?ref_=nmbio_bio_nm>

Alpha Channel description [Garret Fry's Youtube Channel](Issues With Alphas For Matte Painters - YouTube)


  
  
