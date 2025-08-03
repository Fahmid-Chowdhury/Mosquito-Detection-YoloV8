# 🦟 Mosquito Detection on Conveyor System using YOLOv8

This project supports a startup initiative to survey the **distribution of mosquito species across Dhaka** by building an automated **real-time mosquito detection system**. We developed and trained a custom **YOLOv8 model** to **detect and count mosquitoes** on a conveyor belt while **ignoring other insects or debris**. The identification of specific mosquito species is handled separately.

---

## 🔍 Project Objective

The startup designed a hardware machine that:
- Kills and collects mosquitoes.
- Transports individual mosquitoes via a **conveyor belt**.
- Uses a **webcam** to capture real-time images for analysis.

Our role was to:
- Train a YOLOv8 model that **detects mosquitoes only**.
- Reject other insects or foreign particles.
- Enable **live detection and counting** using a webcam.

---

## 🧠 Model Details

- **Framework**: [Ultralytics YOLOv8](https://github.com/ultralytics/ultralytics)
- **Classes**:
  - `0`: mosquito
  - `1`: other (non-mosquito objects)
- **Training Specs**:
  - Model: `yolov8n`
  - Epochs: 30
  - Image size: 640x640
  - Dataset split: 80% train / 20% val

---

## 📊 Sample Metrics

| Metric        | Score |
| ------------- | ----- |
| Precision     | 0.96  |
| Recall        | 0.93  |
| mAP\@0.5      | 0.94  |
| mAP\@0.5:0.95 | 0.50  |

> ⚠️ These scores are based on 56 validation images with 60 mosquito instances.


## 🧩 Future Enhancements

* Integrate with **species identification module**.
* Add **DeepSORT tracking** for more robust counting.
* Deploy on **edge devices** like Jetson Nano or Raspberry Pi + Coral.

---

## 🤝 Contribution

Feel free to fork this repo and contribute if you'd like to enhance detection, tracking, or deployment capabilities.



