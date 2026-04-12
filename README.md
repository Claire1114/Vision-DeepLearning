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
