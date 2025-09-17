# 🚀 ArXiv 每日論文推薦器 🛰️

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/vvchung/daily_arxiv_recommender/blob/main/daily_arxiv_recommender.ipynb)

每天追 ArXiv 最新論文追到心累嗎？😫 擔心錯過自己領域的重磅新研究？

別怕！這個小工具就是你的研究助理！🦸‍♀️ 它會自動幫你：
1.  **掃描** ArXiv 上最新的論文。
2.  用 AI **智慧分析**與你設定的關鍵字的相關度。
3.  **篩選**出最值得你關注的 Top K 篇論文清單！

從此告別大海撈針，每天只看精華中的精華！👇

## ✨ 主要功能

*   **每日自動捕捉** 🎣｜自動抓取 ArXiv 過去 24 小時內發表的最新論文。
*   **你的主題你做主** 📝｜完全客製化！打造你專屬的關鍵字與研究領域清單。
*   **AI 智慧排序** 🧠｜利用 TF-IDF 和餘弦相似度，精準計算論文與你的興趣匹配度，分數越高越相關！
*   **一鍵輕鬆執行** 💨｜點擊上方 "Open in Colab" 按鈕，直接在 Google Colab 中運行，完全不用煩惱環境設定。
*   **100% 絕對安全** 🔒｜純粹的論文推薦器，**完全不需**提供 Email 或任何密碼，安心使用！

## 📈 成果長這樣

執行完畢後，你會得到一個像這樣的超清晰推薦列表：

| title                                                        | score    | published  | url                                                |
| ------------------------------------------------------------ | -------- | ---------- | -------------------------------------------------- |
| A New Transformer Architecture for Large Language Models     | 0.8912   | 2025-09-16 | [https://arxiv.org/pdf/2509.12345.pdf](https://arxiv.org/pdf/2509.12345.pdf) |
| Rethinking Object Detection with Vision Transformers         | 0.8567   | 2025-09-16 | [https://arxiv.org/pdf/2509.54321.pdf](https://arxiv.org/pdf/2509.54321.pdf) |
| ...                                                          | ...      | ...        | ...                                                |

## 🚀 快速開始 (3 個步驟搞定！)

### 1. 在 Colab 中開啟 🚀

點擊 README 最上方的 [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/vvchung/daily_arxiv_recommender/blob/main/daily_arxiv_recommender.ipynb) 按鈕，筆記本就會在你的 Google Colab 環境中打開。

### 2. 客製化你的興趣 🎨

找到筆記本中的**步驟 2：參數配置**儲存格，然後修改這兩個地方：

```python
# --- 論文相關設定 ---
# 把你感興趣的魔法咒語 (關鍵字) 加進去！🧙‍♂️
KEYWORDS = [
    'Object Detection', 'Computer Vision', 'Image Classification',
    'Natural Language Processing', 'Large Language Models', 'Transformer',
    # ... 在這裡加入更多你喜歡的關鍵字！
]

# 選擇你想探索的學術領域 🗺️
ARXIV_TOPIC = {
    'Computer Vision': 'cs.CV',
    'Computation and Language': 'cs.CL',
    # ... 你可以新增或修改這裡的領域
}
```

### 3. 執行！▶️

點擊 Colab 上方的選單：「**執行階段**」➡️「**全部執行**」。

然後就去泡杯咖啡 ☕，稍等一下，推薦結果就會神奇地出現在頁面下方啦！

## 🤖 它是怎麼運作的？

這個推薦器背後的魔法其實很簡單：

1.  **每日掃描 📡**：透過 [arxiv API](https://pypi.org/project/arxiv/) 抓取指定領域的最新論文摘要。
2.  **TF-IDF 魔法 ✨**：將你的關鍵字和每篇論文的摘要，轉換成電腦看得懂的數字向量 (Vector)。
3.  **餘弦相似度配對 💘**：計算你的「關鍵字向量」和每一篇「論文摘要向量」之間的夾角。夾角越小，代表方向越接近，也就是內容越相關！分數（1 表示最相關，0 表示不相關）就這樣誕生了。

## 🛠️ 技術棧

*   **Python** 🐍
*   **Pandas** 🐼
*   **Scikit-learn** 🧪
*   **Arxiv API** 📜
*   **Google Colab** ☁️

## 🤝 歡迎貢獻

發現 Bug？有超棒的新點子？或是想讓推薦演算法更厲害？

都非常歡迎發 `Issue` 或 `Pull Request`！讓我們一起打造更棒的學術工具吧！🎉
