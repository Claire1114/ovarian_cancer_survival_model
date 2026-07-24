# Ovarian Cancer Survival Analysis and Feature Interpretation Using Explainable AI

## 簡述
本專案旨在探討卵巢癌病人之存活分析與預後因子。結合臨床變數與治療前身體組成指標（如骨骼肌指數 SMI），利用機器學習模型與可解釋性人工智慧（XAI）技術，評估各項特徵對病人預後之影響力與非線性關係。

## 研究目的
1. **建構與評估存活預測模型**：比較傳統 Cox 比例風險模型與機器/深度學習存活模型（如Random Survival Forest, DeepSurv等）在卵巢癌預測上的表現。
2. **評估身體組成與臨床特徵之影響力**：透過 SHAP（SHapley Additive exPlanations）全域解釋，分析治療前 SMI 及各臨床風險因子（如 FIGO 分期、腫瘤狀態）對預測結果的邊際貢獻與重要性排序。
3. **探討模型限制與挑戰**：檢視在強烈臨床主導因子（如手術殘留狀態）壓制下，次要生物標記在自動化風險切點劃分上的方法學瓶頸。

## 方法與結果
* **研究對象**：納入 627 位卵巢癌患者之臨床與治療前造影資料。
* **模型表現**：傳統 Cox 模型與隨機生存森林（RSF）在測試集上皆展現穩定的預測效能（C-index 約 $0.828$）。
* **重要發現**：分析顯示，病人的存活預後主要受腫瘤分期、腹水狀況及手術殘留狀態（Residual Status）等臨床因子主導；在多變數校正下，治療前 SMI 之獨立邊際貢獻較小，且未呈現出清晰可獨立切出之非線性風險轉折點。

## 檔案說明 
本專案根目錄包含以下兩個核心檔案：

1. **`ovarian_cancer_survival_analysis.ipynb`**
   * **作用**：專案的核心程式碼與分析流程。包含了資料預處理、各項存活預測模型（Cox、RSF 等）之訓練與評估、模型效能比較（C-index、Time-dependent ROC、Calibration plot），以及使用 SHAP 進行特徵解釋與視覺化繪圖的完整 Jupyter Notebook。

2. **`Ovarian_Cancer_Survival_Prediction_Using_Explainable_AI .pdf`**
   * **作用**：研究成果報告。完整記錄了本研究之背景文獻回顧、研究設計與方法架構、實驗初步結果、模型評估圖表，以及針對現階段分析結果與限制所做出的總結討論。
