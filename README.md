# LivPulse: Real-time AI Vision for Livestock Detection & Behavior Monitoring
*(실시간 AI 비전 기반 가축 탐지 및 행동 모니터링)*

LivPulse는 실제 축산 현장(양식/사육 시설)에 설치된 카메라 영상을 기반으로 가축을 탐지하고 행동/상태를 모니터링하는 것을 목표로 하는 시스템입니다. 객체 탐지 기반 AI 모델을 활용해 소·돼지·닭 등 다종 가축을 검출 및 분류하며, 이를 통해 개체 수 추정, 이상 행동 징후 관측. 주·야간 환경에서의 지속 모니터링을 지원합니다. 또한 주간/야간 데이터를 함께 활용한 전이학습을 통해 조도 변화(야간, 역광 등)로 인한 성능 저하를 완화하여 시간 제약을 줄이는 탐지를 지향합니다.

## ⚙️ Tech Stacks
- YOLOv5
- Object Detection
- Multiclass Classification
- PyTorch
- Python

## ✨ Features
1. 카메라 영상 기반 **실시간 가축 탐지 및 분류**
2. 탐지 결과를 활용한 **실시간 상태/개체 수 모니러링**
3. **주·야간 데이터 적응(도메인 차이 완화)**을 고려한 가축 행동 데이터 특화 탐지 파이프라인

## 🧭 Overview
- **Input**: CCTV/농장 카메라 영상(스트림 또는 파일)
- **Model**: 객체 탐지 기반 가축 검출/분류
- **Output**: 바운딩 박스 + 클래스(종/행동)

## 🎯 Results

#### Figure 1. Train Curve (Train/Val Loss)
<img width="1235" height="747" alt="Train curve" src="https://github.com/user-attachments/assets/32a6f7d4-05ff-40d9-868a-936737efebbd" />

#### Figure 2. Performance
<img width="1188" height="1139" alt="Performance" src="https://github.com/user-attachments/assets/b39d3cd7-297f-4a5b-a73f-dcd8f5bec733" />

#### Figure 3. Detection Results Examples
<img width="1196" height="957" alt="Image" src="https://github.com/user-attachments/assets/8ab99c17-5352-4df5-81c2-162b091fd93d" />

## 🔮 **Future Work** 
1. 더 강력한 탐지 아키텍처/백본 및 학습 전략을 활용하여 정확도 개선
2. 전체 몸이 프레임에 온전히 포함되지 않는 상황(부분 가림/크롭)에서의 실패를 줄이기 위해 Crop 기반 데이터 증강, multi-class 학습, occlusion augmentation 적용
3. 후면/측면 등 특정 시점에서의 검출 실패를 완화하기 위해 데이터 추가 수집 및 하드 케이스 선별 학습(hard example minig)

## 📜 License
The code in this repository is released under the GPL-3.0 License.