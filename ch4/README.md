# Chapter 4: 文本分類的全景圖 (Text Classification)

![TwinkleAI Reading Club Banner](../images/TwinkleAI_Reading_Club_00800_x_320_px.png)

- **日期：** 2026-05-03
- **內容：** 從傳統表示型模型到最新生成式模型，全面探索 LLM 如何精準判斷文字背後的意圖與情緒。
- **實作：** （待更新）

## 本章重點

### 表示型模型的分類雙重奏

- **任務特定模型（Task-specific Models）**：以 BERT 家族等 Encoder-only 模型為基礎，針對特定分類任務進行微調（Fine-tuning），在分類頭（Classification Head）上輸出最終預測
- **嵌入模型（Embedding Models）**：將文字轉為向量表示，再搭配傳統機器學習分類器（如邏輯迴歸 Logistic Regression）進行分類，適合資源有限或標記資料較少的情境

### 零樣本分類（Zero-shot Classification）

- 面對標記資料匱乏的實務困境，透過比較文字嵌入向量與標籤描述向量之間的**餘弦相似度（Cosine Similarity）**，在完全不訓練模型的情況下完成分類
- 核心概念：語意相近的文字在向量空間中距離也相近，標籤的語意描述即可作為分類依據

### 生成式模型的分類新思維

| 模型類型 | 代表模型 | 特點 |
| --- | --- | --- |
| **Sequence-to-Sequence** | Flan-T5 | 以生成方式輸出分類標籤，透過指令微調（Instruction Tuning）強化任務理解 |
| **閉源生成模型** | ChatGPT / GPT-4 | 透過提示工程（Prompt Engineering）指引模型輸出結構化分類結果 |

- **提示工程（Prompt Engineering）**：設計有效的提示詞以引導模型產出期望的分類格式，包含 Few-shot 範例注入與輸出格式約束
- **偏好對齊（Preference Tuning）**：透過 RLHF / DPO 等技術使模型行為更符合人類期望，間接提升分類任務的準確性

### 專業的評估指標

- **混淆矩陣（Confusion Matrix）**：全面呈現預測結果與真實標籤之間的分布，揭示模型在各類別上的表現差異
- **準確率（Accuracy）**：正確預測佔全體樣本的比例，適合類別分布均衡的情境
- **精確率（Precision）**：預測為正例中實際為正例的比例，強調「預測的可靠性」
- **召回率（Recall）**：實際正例中被正確預測出來的比例，強調「找出所有正例的能力」
- **F1 分數（F1 Score）**：Precision 與 Recall 的調和平均，在兩者之間取得平衡

## 資源

- [官方 Notebook](Chapter%204%20-%20Text%20Classification.ipynb)
- 簡報：（待更新）
- TwinkleAI 版 Notebook：（待更新）