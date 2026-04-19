# Twinkle AI 熬夜書坊 - LLM 讀書會資源庫

![TwinkleAI Reading Club Banner](images/TwinkleAI%20Reading%20Club%20v2%29.png)

歡迎來到 **Twinkle AI 熬夜書坊 (Late-Night Study Session)** 的專屬 GitHub Repository！

本專案旨在存放我們線上讀書會的所有開源資源，包含簡報、討論筆記以及可執行的 Jupyter Notebooks。目前我們正在共讀由 Jay Alammar 與 Maarten Grootendorst 共同撰寫的重量級大作——**《LLM 語意理解與生成技術 完全開發》 (Hands-On Large Language Models)**。

無論你是剛踏入 LLM 領域的新手，還是想穩固底層知識、掌握實作細節的開發者，都歡迎跟著石虎的腳步，一起輕鬆交流、共同成長！☕️📚

## 📖 讀書會時程與大綱

活動固定於 **每週日晚間 20:00** 於線上進行。以下是各章節的資源與實作進度：

- [x] **Chapter 1: 基礎 (Introduction to Language Models)**
  - 日期：2026-04-05
  - 內容：LLM OS 概念、生成式 AI 歷史時間軸、Text input 與 Embeddings 基礎。
  - 實作：使用 Twinkle AI 專屬模型 `gemma-3-4B-T1-it` 進行 Formosa Vision 專案問答實作。
  - 資源：[簡報](ch1/Twinkle-llm-book-ch1.pdf) | [Notebook](ch1/Chapter_1_Introduction_to_Language_Models.ipynb) | [TwinkleAI 版 Notebook](ch1/Chapter_1_Introduction_to_Language_Models_twinkleai_version.ipynb)

- [x] **Chapter 2: Tokens 與 Embeddings (Tokens and Embeddings)**
  - 日期：2026-04-12
  - 內容：Tokenization 解析、Vocabulary 與 Special Tokens、Embeddings 向量魔法。
  - 實作：深入拆解 Tokenizer 的編碼與解碼過程，含八種模型 Tokenizer 視覺化比較、Word2Vec 音樂推薦實作。
  - 資源：[簡報](ch2/Twinkle-llm-book-ch2-slide.pdf) | [Notebook](ch2/Chapter_2_Tokens_and_Token_Embeddings.ipynb) | [TwinkleAI 版 Notebook](ch2/Chapter_2_Tokens_and_Token_Embeddings-twinkleai.ipynb) | [NotebookLM 筆記](ch2/NotebookLM-Language_Blueprints.pdf)

- [ ] **Chapter 3: 看進語言模型的黑盒子 (Looking Inside Large Language Models)**
  - 日期：2026-04-19
  - 內容：打開語言模型的黑盒子，透視 Transformer 架構的內部運作機制。
    - **生成機制的秘密**：LLM 如何以自迴歸（autoregressive）方式逐 Token 生成，以及 KV Cache 最佳化技術如何大幅加速生成過程。
    - **Transformer 內部解密**：拆解 Transformer 區塊的兩大核心組件——負責記憶與推論的「前饋神經網路 (Feedforward Neural Network)」，以及整合上下文資訊的「注意力機制 (Attention Layer)」。
    - **注意力機制的進化**：深入認識 Queries、Keys、Values (QKV) 投影矩陣的產生與互動計算，以及近年架構改良——Grouped-Query Attention (GQA)、Flash Attention 與旋轉位置編碼 (RoPE)。
  - 實作：（待更新）
  - 資源：[簡報](ch3/Twinkle-llm-book-ch3.pdf)

> 後續章節將每週持續更新...

## 🚀 Getting Started (如何開始實作)

如果你想跟著讀書會一起動手跑程式碼，請參考以下步驟：

1. **環境準備**：強烈建議使用具備 GPU 資源的環境（例如 Google Colab 的 T4 GPU）以獲得順暢的推論體驗。或者你也可以使用自己習慣的 Jupyter / marimo 環境。
2. **安裝套件**：確保已安裝最新版的 `transformers` 與 `accelerate`。

   ```bash
   pip install transformers>=4.50.0 accelerate>=0.31.0
   ```

3. **模型存取**：部分模型可能需要 Hugging Face 帳號授權，請確保你在環境中設定了 `HF_TOKEN`。

## 🌟 About Twinkle AI

**Twinkle AI** 是一個以繁體中文為核心的開源 AI 社群，專注於打造在地語言模型與資料集。我們致力於推動可公開使用的模型權重、訓練資料與實務經驗分享，串聯研究者、工程師與創作者，促進台灣在地 AI 生態的交流與共創。

Twinkle AI is a research community founded in late 2024, dedicated to enhancing Traditional Chinese language models with local cultural context. Starting with open-source LLaMA models, we are developing practical technologies tailored to the linguistic nuances of Taiwan. Our mission is to promote knowledge of large language model training through real-world practices. By embracing openness and collaboration, we aim to advance the local ecosystem in the field of generative AI.

## 🤝 貢獻與參與

這個讀書會與資源庫是社群共創的心血。如果你在閱讀或執行程式碼時發現任何問題，或是想補充更棒的繁體中文/在地化 LLM 範例，非常歡迎發起 **Pull Request** 或建立 **Issue** 一起討論！

## 參考資源

### Twinkle AI

- [Twinkle AI 官網](https://twinkleai.tw/)
- [Hugging Face](https://huggingface.co/twinkle-ai)
- [GitHub](https://github.com/ai-twinkle)
- [Discord](https://discord.com/servers/twinkle-ai-1310544431983759450)

### 書籍相關

- [Hands-On Large Language Models 官網](https://www.llm-book.com/)
- [Hands-On Large Language Models (Official Repo)](https://github.com/HandsOnLLM/Hands-On-Large-Language-Models)
- [Jay Alammar's Blog](https://jalammar.github.io/)
- [Maarten Grootendorst's Newsletter](https://newsletter.maartengrootendorst.com/)

### 本讀書會

- [GitHub Repo](https://github.com/thliang01/TwinkleAI-LLM-Book-Club)
- [Maintainer: thliang01](https://github.com/thliang01)
