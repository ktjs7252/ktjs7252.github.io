---
layout : post
title: LPF와 FFT를 이용한 생체신호 측정(아두이노 개선)
---


# 실험목표
<br/>
## 이전보다 더 완벽한 생체신호측정을 위해 LPF와 FFT를 코드로 구현하여 출력하는것

필터전의 ECG신호를 FFT한 결과와 필터후의 ECG신호를 FFT한 결과를 비교한다. 
LPF: FFT를 이용해 주파수축으로 바뀐 신호 중 원하지 않는 신호를 제거한다.
FFT: 시간축에서의 신호로는 정보를 알 수 없어 주파수 축으로 변환한다.

<br/>
<br/>

# 실험방법

* FFT: 시간 도메인을 주파수 도메인으로 변환시키는, 즉 시간에 대한 함수를 구성하고 있는 주파수 성분으로 분해하는 과정
다음식을 이용
![image](https://user-images.githubusercontent.com/78638160/151109349-9dbaa0cf-846c-4f36-b2e0-9021a5d6d526.png)
<br/>
* 샘플링: 아날로그 데이터를 디지털 데이터로 추출하는 것
샘플링을 코드로 구현
![image](https://user-images.githubusercontent.com/78638160/151109550-64d2aeea-e42b-4c31-afd4-2449a4d96d99.png)
![image](https://user-images.githubusercontent.com/78638160/151109559-e444cb4a-1bd0-46c9-9280-f75e2b47eb95.png)
<br/>
* LPF: 특정한 차단 주파수 이상 주파수의 신호를 감쇠시켜 차단 주파수 이하의 주파수 신호만 통과시키는 필터
로우패스 필터를 코드로 구현
![image](https://user-images.githubusercontent.com/78638160/151109627-ddf4cf31-c021-480f-a71f-01a80b569a11.png)

<br/>
<br/>
<br/>
# 전체 코드
![4](https://user-images.githubusercontent.com/78638160/151110185-ef5f143f-4a69-48f7-a5fa-0901cf717fca.png)
![5](https://user-images.githubusercontent.com/78638160/151110205-86243700-48e2-422b-b50e-8ba3a9c0355b.png)

<br/>
<br/>
<br/>
# 실험 결과

![44](https://user-images.githubusercontent.com/78638160/151110559-5a0afd39-c76c-4cc5-b769-6eefe9db7faa.png)

![7](https://user-images.githubusercontent.com/78638160/151110575-b4704d0d-4c07-4b39-af89-6d1455ed9111.png)
![6](https://user-images.githubusercontent.com/78638160/151110581-e52a7eda-89ea-4a9a-a6f8-96be4b6096b2.png)

<br/>
<br/>
![9](https://user-images.githubusercontent.com/78638160/151110612-0dcbc26e-7d68-414f-99b1-f04a644324b3.png)


