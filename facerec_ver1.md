# 이미지 처리 진행과정 - 10주차

## Face-Landmark
opencv 및 dilb를 활용하여 마스크착용 사진 및 미착용 사진을 각각 face-landmark을 진행하였다.

## 윤곽선 검출
<center><img src="https://user-images.githubusercontent.com/80964083/117542634-66995b80-b054-11eb-8935-dbb561badfee.png" width="128" height="128"></center>
face1.jpg
<center><img src="https://user-images.githubusercontent.com/80964083/117542700-a2342580-b054-11eb-9a9b-5ce92aed5613.png" width="128" height="128"></center>
face2.jpg


아래의 예시는 위의 두 이미지를 통해서 진행되었다.
<center><img src="https://user-images.githubusercontent.com/80964083/117543134-7fa30c00-b056-11eb-8808-2e307355e546.png" width="256" height="256"></center>

face-landmark 좌표를 통해서 얻어낸 얼굴의 윤곽, 눈의 하단에서 코로 이어지는 선에 대해서 경계를 설정한 후, 

## 잘라낸 사진 합성 후 재배치

## 영상 Frame 단위로 자르기
우리 프로젝트의 input은 마스크를 낀 사진과, 얼굴이 다 나오는 "동영상"이다. 따라서, 동영상에서 프레임 단위로 자른 후에,
이중 한 이미지를 합성에 사용하고, 다른 모든 이미지들은 autoencoder에 사용한다.
<center><img src="https://user-images.githubusercontent.com/71958885/118405550-7992d800-b6b3-11eb-9bce-f71ef02bc289.gif"></center>
다음의 동영상에서 얼굴부분만 crop하여 프레임단위로 저장하였다.
<center><img src="https://user-images.githubusercontent.com/71958885/118405586-ad6dfd80-b6b3-11eb-95de-c8f666d795e1.PNG"></center>



# 이미지 처리 진행과정 - 11주차

## 피부톤 조정
합성될 이미지와, 합성시킬 이미지의 조명차이 때문에, 합성된 사진의 피부톤의 차이가 클 수 있기 때문에,
이를 고려하여 피부톤을 조정하고자 하였다.
<center><img src="https://user-images.githubusercontent.com/71958885/118405766-32591700-b6b4-11eb-93b4-90c59b71f64e.png" width="256" height="256"></center>
<center><img src="https://user-images.githubusercontent.com/71958885/118405774-3f760600-b6b4-11eb-9262-e0d27e8e1009.png" width="256" height="256"></center>
위의 합성된 사진이 아래 사진과 같이 피부톤이 어둡게 변화된 것을 확인할 수 있었다.


## 이미지 rotate
