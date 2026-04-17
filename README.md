# Vision-DeepLearning
影像處理相關專案 

收錄Vision-DeepLearning相關兩個專案，涵蓋：
- **影像分類任務**：識別放射科影像部位的深度學習系統



---

## Project 1 — Medical X-ray Image Classification
📁 Folder: Medical-Xray_Classification_Multi-stage_Analysis/

**重點內容**
- 模型對照與架構優化：比較 ResNet50 與 ConvNeXt-Tiny 在 8 分類與 22 分類任務中的表現，ConvNeXt 在細粒度任務維持 92% 以上準確率。

- 類別不平衡解決方案：引入加權抽樣 (Weighted Random Sampling) 與權重平滑化，將少數類別（如 Skull）敏感度從 71% 提升至 100%，有效降低臨床漏診風險。

- 可解釋性 AI：利用 Grad-CAM 技術進行視覺化分析，證實模型決策精確鎖定核心解剖構造（如肺野、腸道），符合臨床解剖邏輯。

➡️ 詳細方法、實驗設定與結果請見該資料夾內 README / 報告。

---

## Project 2 — Automated Rib Segmentation in Chest X-rays
📁 Folder: Rib-Segmentation_UNet_ResNet50_Analysis/

**重點內容**
- 架構與微調：採用 U-Net + ResNet50，透過解凍部分層級進行半微調，讓預訓練模型精確適應醫療影像的灰階特徵。

- 小樣本強健度：在有限資料（n=196）下透過多重資料擴增與 Dynamic Padding，達成 IoU 0.8968，驗證了模型在小樣本下的泛化潛力。

- 錯誤分析：建立 FP/FN 顏色編碼疊圖分析，精確鎖定低對比區的識別瓶頸，釐清模型判別問題。

➡️ 詳細方法、實驗設定與結果請見該資料夾內 README / 報告。
