---
layout : post
title : 오실로스코프를 이용한 생체신호 측정
---

*실험목표
![그림01](https://user-images.githubusercontent.com/78638160/151104759-5e44ecd7-6f70-4b2a-afd2-88ccc6382307.jpg)

ECG 원신호는 잡음을 가지고 있어 저역 통과 필터를 사용해 잡음을 줄여주도록 함
ECG 신호의 R peak가 아래쪽으로 향해있어 반전시키도록 함
 
![제목 없음](https://user-images.githubusercontent.com/78638160/151104826-726e3ea4-015c-4338-9ee8-8f6ea5cabb5c.png)


* ECG( ElectroCardiogram)란?

* 심전도
심장의 전기적 활동을 분석하여 파장 형태로 기록한 것을 말한다. 심장의 근육 세포들은 전류에 반응하여 수축·이완하며, 이러한 활동은 심장의 전도계에서 흘려보내는 전류에 의해 통제된다
심전도 주파수 대역: 0.5 ~ 150Hz
-심전도 측정 방법
ECG를 실시하기 위해서, 검사자는 전극(피부에 부착되는 작고 둥근 센서)을 환자의 팔, 다리와 가슴에 올려 놓습니다.![image](https://user-images.githubusercontent.com/78638160/151104837-12b2b43a-e4d0-4b21-93d9-eaf8d4e78870.png)


*싫험원리
- 전압분배
교류 전압 : -와 +의 전압을 번갈아가는 신호
예를 들어 신호의 범위가 -5v ~ +5v라고 할 때
E2kit은 –신호를 표현할 수 없어 –신호는 무시된다.
따라서 전압 분배를 이용해 GND의 기준점을 0v에서 2.5v로 올려준다.![image](https://user-images.githubusercontent.com/78638160/151105017-9af51ccd-39dc-4d15-b934-e59de32e5f1f.png)


- 필터
오실로스코프를 통해 신호를 확인하면
노이즈 신호가 많이 나타나고 신호가 반전되어 나와
원하는 신호를 얻어내기 위해 필터를 사용한다.![image](https://user-images.githubusercontent.com/78638160/151105024-f297377b-d27c-4256-800a-05212759d58a.png)


*실험방법

![image](https://user-images.githubusercontent.com/78638160/151105068-1f273127-555f-46d6-9ada-8ac5fc07c550.png)
![image](https://user-images.githubusercontent.com/78638160/151105075-4883359b-3158-4e53-99b9-c5753d8448b0.png)

전압분배한 값을 증폭기의 그라운드에 넣어Vref값을 설정해주고, 반전시켜준다.

![1](https://user-images.githubusercontent.com/78638160/151105170-d66e5095-55e9-4073-9037-47e7b1ccb31a.png)



*실험결과

![image](https://user-images.githubusercontent.com/78638160/151105196-283aae50-8856-4fce-97e4-c351c40d27dd.png)


- 약 75Hz이상의 신호는 필터링 되어 잡음이 많이 사라진 것을 볼 수 있음.

- ECG신호가 반전되어 나오는 것을 볼 수 있음. 
 
