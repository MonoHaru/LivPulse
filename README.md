🌐 Languages: [[English](README.md)] | [[한국어](README-KR.md)]

# LivPulse: Real-time AI Vision for Livestock Detection & Behavior Monitoring
*(Real-time AI vision-based livestock detection and behavior monitoring)*

LivPulse is a system designed to detect livestock and monitor their behavior and condition using camera footage captured in real-world livestock farming environments (aquaculture and breeding facilities). It leverages an object detection-based AI model to detect and classify multiple livestock species such as cattle, pigs, and chickens. This enables livestock counting and observation of abnormal behavior signals, while supporting continuous monitoring in both daytime and nighttime environments. In addition, LivPulse aims to reduce time constraints on detection by mitigating performance degradation caused by illumination changes (nighttime, backlighting, etc.) through transfer learning that jointly utilizes daytime and nighttime data.


## ⚙️ Tech Stacks
- YOLOv5
- Object Detection
- Multiclass Classification
- PyTorch
- Python


## ✨ Features
1. Camera footage-based **real-time livestock detection and classification**
2. **Real-time condition and population monitoring** using detection results
3. A livestock behavior-focused detection pipeline that considers **day and night data adaptation (reduced domain gap)**


## 🧭 Overview
- **Input**: CCTV or farm camera footage (stream or file)
- **Model**: Object detection-based livestock detection and classification
- **Output**: Bounding boxes plus classes (species and behavior)


## 🎯 Results

#### Figure 1. Train Curve (Train/Val Loss)
<img width="1235" height="747" alt="Train curve" src="https://github.com/user-attachments/assets/32a6f7d4-05ff-40d9-868a-936737efebbd" />

#### Figure 2. Performance
<img width="1188" height="1139" alt="Performance" src="https://github.com/user-attachments/assets/b39d3cd7-297f-4a5b-a73f-dcd8f5bec733" />

#### Figure 3. Detection Results Examples
<img width="1196" height="957" alt="Image" src="https://github.com/user-attachments/assets/8ab99c17-5352-4df5-81c2-162b091fd93d" />


## 🔮 **Future Work** 
1. Improve accuracy by using stronger detection architectures or backbones, along with better training strategies
2. Apply crop-based data augmentation, multi-class training, and occlusion augmentation to reduce failures in cases where the full body is not fully visible in the frame (partial occlusion or cropping)
3. Collect additional data and train with selected hard cases (hard example mining) to mitigate detection failures from specific viewpoints such as rear or side views


## 📜 License
The code in this repository is released under the GPL-3.0 License.