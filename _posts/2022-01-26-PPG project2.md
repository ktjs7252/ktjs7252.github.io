---
layout : post
title : 아두이노를 활용한 생체신호측정(오실로스코프 개선을 위한)
---

# 실험목표

![image](https://user-images.githubusercontent.com/78638160/151106686-d489e8fd-e04c-47d0-8cf6-7ab55e6331a8.png)

E2-kit 기기를 통해 화면에서 나타난 ECG 신호는 잡음이 나타나며, 반전되어 나옴

잡음은 높은 주파수, 생체신호는 낮은 주파수를 가지기 때문에
작은 주파수를 통과시키는 Low-Pass Filter를 사용하여 노이즈를 줄이고,
반전되어 나오는 신호를 다시 반전시켜서 원하는 ECG 신호를 얻도록 함

<hr/>
<hr/>
![2](https://user-images.githubusercontent.com/78638160/151107132-2c034e13-279d-46dc-9e6d-fce65210124b.png)

<hr/>
<hr/>

# 필터링방법1

*시간영역에서 이전 측정값과 현재 측정값에 가두이를 두어 계산

![image](https://user-images.githubusercontent.com/78638160/151107236-a1c24ccf-55b0-4546-baac-8eaf6a201d7b.png)

이전 측정 값(filteredValue)과 
현재 측정 값(sensorValue)의 비율을 이용하여 
필터링하는 과정을 반복

<hr/>
![image](https://user-images.githubusercontent.com/78638160/151107295-64684607-47d8-4358-ae5d-9d6313a41b55.png)

<hr/>

*sensitivity = 0.3 
![image](https://user-images.githubusercontent.com/78638160/151107333-ebc56477-ea59-459e-8ff8-1064ee8c8cc1.png)
<hr/>

*sensitivity = 0.5
![image](https://user-images.githubusercontent.com/78638160/151107510-5e0796be-5f5c-4b40-b6ed-f5fd8f061408.png)
<hr/>

*sensitivity = 0.7
![image](https://user-images.githubusercontent.com/78638160/151107531-12a3dc3e-8460-4829-b2e2-42538418e674.png)
<hr/>

*sensitivity = 0.9
![image](https://user-images.githubusercontent.com/78638160/151107556-cfc8c5bc-fae4-433d-82c9-3f4559a97192.png)

<hr/>

# 실험결과

sensitivity 값이 과도하게 작으면 이전의 값과 
비슷한 값이 나오기 때문에 잡음이 줄어들고 
그래프가 부드러워짐
<hr/>
→ 하지만 현재 값과 큰 차이가 남
<hr/>
<hr/>
sensitivity 값이 커질수록 
현재 값의 비중이 커지고 이전 값의 비중이 줄어들어
필터링된 그래프가 현재의 그래프와 비슷함
<hr/>
<hr/>
sensitivity 값을 이용하면 주파수를 정할 수 없어 
시간 축 영역에서는 정확히 필터링하기에 어려움이 있음


<hr/>
<hr/><hr/>
<hr/>
 # 필터링 방법2
 시간 축 영역의 신호를 주파수 축 영역으로 바꿔주는 방법
 ![3](https://user-images.githubusercontent.com/78638160/151107719-089a87a7-c8e3-460d-a9ba-de5adaff6e9a.png)

<hr/>
<hr/>

주파수 영역으로 변환해주기 위해 라플라스 변환식을 사용

![image](https://user-images.githubusercontent.com/78638160/151107781-3f40df1a-7611-4e53-bd1b-235c1164c2ac.png)
![image](https://user-images.githubusercontent.com/78638160/151107789-579ebf1e-75e8-4e37-a7be-92f1aa458ec1.png)
![image](https://user-images.githubusercontent.com/78638160/151107792-f60b95f4-cd65-4b11-a695-25c9bf45c4a7.png)
![image](https://user-images.githubusercontent.com/78638160/151107828-8b51f1c3-e3a2-4767-91a0-2bf69ea10d63.png)

<hr/>
![image](https://user-images.githubusercontent.com/78638160/151107816-57864546-60b6-42fa-8e3b-9d8dab524350.png)


# 실험 결과

![image](https://user-images.githubusercontent.com/78638160/151107934-955cc40f-619f-40fa-a288-be9c4cdb8d63.png)
![image](https://user-images.githubusercontent.com/78638160/151107935-03fe4957-6c32-4355-8372-448f85b24277.png)

![image](https://user-images.githubusercontent.com/78638160/151107940-4af8d292-d2ad-41ac-9eca-cfe21b0af7a1.png)





