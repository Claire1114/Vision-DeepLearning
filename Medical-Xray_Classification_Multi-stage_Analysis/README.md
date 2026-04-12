# Medical X-ray Classification & Multi-stage Analysis

## Overview
本專案針對醫療 X 光影像開發自動化分類系統，透過 ResNet50 與 ConvNeXt-Tiny 模型進行多階段分析，並透過 Grad-CAM 提供臨床診斷的可解釋性依據。

> **資料來源說明**：kaggle UNIFESP X-ray身體部位分類資料集 [(https://www.kaggle.com/datasets/felipekitamura/unifesp-xray-bodypart-classification/data<img width="432" height="40" alt="image" src="https://github.com/user-attachments/assets/f91c3e42-0165-4386-8584-18e9f01193ce" />](https://www.kaggle.com/datasets/felipekitamura/unifesp-xray-bodypart-classification/data)）
)

---

## Files
- Source Code (Notebooks):

影像分類專案_8分類.ipynb: 針對基礎 8 類別任務，包含加權抽樣（Weighted Random Sampling）實驗。

影像分類專案_21分類.ipynb: 針對高難度 21/22 類別的細粒度分類任務。

- Model Weights (.pth):

best_model_8class_weight.pth: 8 分類任務中表現最佳之模型權重。

best_convnext_22class.pth: 採用 ConvNeXt-Tiny 架構之 22 分類模型權重。

- Documentation:

Medical_Xray_Analysis_Report.pdf: 完整實驗報告，包含詳細圖表、指標分析與解剖學探討。

---

## Experiments Summary

**1) 抽樣策略緩解類別不平衡 (Class Imbalance)：** 引入加權抽樣 (Weighted Random Sampling)觀察此方法對模型決策影響。

**2) ConvNeXt-Tiny架構提升細粒度分類能力：** 面對更複雜的 22 分類任務，在使用 ConvNeXt-Tiny 架構，測試準確率穩定維持在 92%，驗證此模型在大規模分類任務中具特徵提取能力，能有效修正如脊椎節段等高度相似部位的邊界。 。

**3) Grad-CAM (Gradient-weighted Class Activation Mapping) 視覺化分析：** 證實模型能精確鎖定核心解剖構造（如肺野、腸道、關節），並也可用於錯誤分析，理解模型決策錯誤原因。


---

## How to Run
建議使用 Jupyter / VS Code / Colab 開啟 notebook 執行。

