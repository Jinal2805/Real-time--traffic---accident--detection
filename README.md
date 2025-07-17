
# 🚦 Real-Time Traffic Flow Analysis and Accident Detection using Deep Learning

This project presents a real-time traffic monitoring system that uses **YOLOv8**, **CNN**, and **LSTM** to detect traffic congestion and road accidents from surveillance video feeds. The system is built to support **smart city infrastructure** by improving emergency response, enhancing road safety, and reducing congestion.

## 📌 Project Overview

In fast-growing urban areas, traditional rule-based systems fail to handle traffic anomalies in real-time. This system leverages **video data mining** and **deep learning** to automatically detect and alert authorities about accidents or traffic congestion using:

- **YOLOv8** for high-speed vehicle detection and counting
- **CNN + LSTM** hybrid for spatial-temporal anomaly detection
- **IEEE DataPort** dataset for training and testing

---

## 🧠 Core Technologies Used

| Component        | Description                                                                 |
|------------------|-----------------------------------------------------------------------------|
| YOLOv8           | Real-time object detection for locating vehicles in each video frame        |
| CNN              | Extracts spatial patterns like vehicle density, clusters, and anomalies      |
| LSTM             | Detects temporal behavior over time for accident prediction                  |
| Pandas           | Structured handling of frame-level vehicle count data                        |

---
## 📊 Dataset

**Source**: [IEEE DataPort - Traffic Accident Detection Dataset](https://ieee-dataport.org/)  
The dataset is designed for training real-time traffic incident detection systems using video data.

### 🔍 Modalities:
- **Visual Data**: Extracted from video frames (bounding boxes of detected vehicles)
- **Count Data**: Frame-wise vehicle count time series for traffic flow and anomaly patterns

### 🛠️ Preprocessing Techniques:
- Oversampling of rare accident classes to address data imbalance
- Temporal data augmentation for better LSTM sequence learning
- Class balancing using SMOTE and strategic under-sampling

---

## 🧪 Performance Metrics

The model was evaluated using **10-fold cross-validation** and standard classification metrics:

| Class        | Precision | Recall | F1-Score | Support |
|--------------|-----------|--------|----------|---------|
| No Accident  | 99.80%    | 99.85% | 99.90%   | 13,071  |
| Accident     | 99.62%    | 99.80% | 99.81%   | 6,799   |
| **Overall**  | **99.87%**|        | **99.87%**| 19,870  |

### ✅ Model Info:
- **Architecture**: YOLOv8 + CNN + LSTM (Hybrid Deep Learning Pipeline)
- **Cross-Validation**: 10-fold
- **Overall Accuracy**: `99.86%`
- **F1-Score**: `99.86%`
- **Mean Absolute Error (MAE)**: `0.013`
- **Correlation Coefficient**: `0.927`

This result confirms the **robustness, generalization ability**, and **real-time effectiveness** of the proposed system for intelligent traffic monitoring.

## 🌐 Use Cases

This system is designed to serve a wide range of real-world applications, particularly in smart city environments:

- 🚦 **Smart Traffic Control Centers**: Enables centralized traffic flow and accident monitoring
- 🛣️ **Urban and Highway Surveillance**: Detects incidents across varied environments
- 🚑 **Automated Emergency Dispatch**: Triggers real-time alerts for rapid response and rescue
- 🗺️ **Traffic App Integrations**: Can support rerouting in platforms like Google Maps or Waze using detected incident data

---

## 🏁 Future Scope

To further enhance the system's intelligence and scalability, the following improvements are considered for future versions:

- 📷 **Real-time CCTV Integrations**: Directly connect to live city surveillance camera feeds
- 🚶 **Pedestrian Accident Detection**: Extend detection to pedestrian-related incidents
- 🚁 **Drone-based Traffic Monitoring**: Monitor larger areas using UAVs for aerial video analysis
- 🤖 **Transformer-based Models**: Leverage attention-based architectures for better temporal reasoning and multi-class event detection
