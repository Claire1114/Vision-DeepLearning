# Automated Rib Segmentation in Chest X-rays

本專案開發一套基於深度學習的自動化肋骨分割系統，旨在協助放射科醫師更精確地定位肋骨解剖構造。

## 🛠 技術重點
- **模型架構**：採用 **U-Net** 搭配 **ResNet50** 預訓練編碼器。
- **微調策略**：實施 **Semi-Fine-tuning**，解凍 Layer 1-4 以適應醫療影像特徵。
- **效能表現**：在獨立測試集達成 **IoU: 0.8968** 與 **Dice Loss: 0.0559**。
- **資料增強**：針對 196 張小規模樣本，使用隨機裁剪、亮度對比調整及 Dynamic Padding 提升模型穩健性。

## 🔍 錯誤分析 (Bad Case Diagnosis)
透過 FP (紅色) / FN (藍色) 疊圖分析，精確診斷模型在以下區域的局限性：
1. **解剖重疊區**：鎖骨與高位肋骨重疊導致局部假陽性。
2. **低對比區域**：肺底與橫隔膜遮蔽處易產生漏偵測。

## 📁 檔案說明
- `Rib-Segmentation.ipynb`: 完整訓練流程、資料預處理與評估代碼。
- `Rib Segmentation in Chest X-ray Images.pdf`: 詳細專案報告與視覺化分析結果。
