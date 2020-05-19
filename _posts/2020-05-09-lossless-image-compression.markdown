---
layout: post
title:  "lossless image compression"
subtitle: "lossless image compression"
categories: study
tags: study
comments: true
---
https://arxiv.org/pdf/2004.02872.pdf  

#### 요약정리
이미지를 딥러닝을 이용해서 "저해상도 + 코드파일"로 압축하는 방식입니다.  
![1](../assets/img/lossless/1.png)  
![2](../assets/img/lossless/2.png)  
논문의 주장으로는 무손실 압축방식으로
bpsp 2.7대로 압축할 수 있으며 (2.7/8 ~= 33%, 1MB 이미지를 330KB)
AMD Ryzen 5 1600, NVIDIA GTX 1060 머신에서 960x960 이미지를 압축을 푸는데 2.3초정도 걸린다고 합니다.

---

#### Introduction
사람들은 매년 1조 개의 새로운 사진을 생산한다고 합니다. 이미지는 다양한 실제 세계와 복잡함을 갖지만, 모든 픽셀의 arrangement가 실제 사진 모양을 하고 있진 않습니다. 대부분은 읽을 수 없는 노이즈입니다.  
모든 픽셀의 arrangement 중 일부분만이 실제 사진이라는게 이 논문의 메인 insight입니다. Shannon source coding theorem은 실제 사진들의 픽셀 그룹의 likelihood와 이미지 압축하는 능력을 연결 시킨 것입니다.  
(샤넌 소스코딩 정리는 데이터 압축 가능한 한계와 정보량을 확립하는 정리인데, 여기서 실제 사진의 픽셀 그룹의 likelihood는 정보량이라고 할 수 있고, 압축 가능한 한계가 압축률이라고 할 수 있는 것 같아요.)  

---