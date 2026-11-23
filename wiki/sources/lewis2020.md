# 用於知識密集任務的檢索增強生成

- **英文標題**：Retrieval-Augmented Generation for Knowledge-Intensive NLP Tasks
- **作者**：Patrick Lewis 等（Facebook AI Research、倫敦大學學院、紐約大學）
- **年份**：2020（arXiv 2005.11401；本檔為 2021 年 v4）
- **出處**：NeurIPS 2020（依 es2023 參考文獻所載）
- **原文**：`raw/lewis2020.pdf`

## 白話摘要
這篇論文正式提出「檢索增強生成（Retrieval-Augmented Generation，RAG）」這個名稱。作者讓語言模型在回答前，先到維基百科裡找出相關段落，再根據這些段落產生答案。這樣模型就同時擁有「腦中記住的知識」和「可以翻閱的外部資料」。結果在多個問答任務上表現超越當時的最佳方法，產生的內容也更符合事實、更具體。

## 核心想法
- 語言模型把知識存在自己的參數裡（**參數記憶，parametric memory**），但這種記憶很難修改、無法說明答案從哪來，還可能產生「幻覺（hallucination）」[§1]。
- RAG 加上一份**外部記憶（non-parametric memory）**：一個可搜尋的維基百科索引 [§1]。
- 系統由兩部分組成：**檢索器（retriever）**負責找出相關文件，**生成器（generator）**負責根據文件寫出答案 [§2]。
- 檢索器使用 DPR（Dense Passage Retriever），生成器使用 BART [§2.2, §2.3]。
- 提出兩種版本：RAG-Sequence（整個答案參考同一批文件）和 RAG-Token（每個字都可以參考不同文件）[§2.1]。

## 重要發現與數字
- 外部資料庫：2018 年 12 月的維基百科，切成每段 100 字的區塊，共 2,100 萬（21M）段 [§3]。
- 生成器 BART-large 有 4 億（400M）個參數 [§2.3]。
- 開放領域問答 Natural Questions：RAG-Sequence 得分 44.5，純靠記憶的 T5-11B 是 34.5 [§4.1, Table 1]。
- 即使正確答案不在任何檢索到的文件裡，RAG 仍有 11.8% 答對；只會從文件「摘抄」的模型在這種情況是 0% [§4.1]。
- 人工評估 Jeopardy 出題：評審認為 RAG 更符合事實的比例是 42.7%，認為 BART 更符合事實的只有 7.1% [§4.3, Table 4]。
- 事實查核 FEVER（三分類）：RAG 與當時最佳系統只差 4.3% 以內，而且不需要額外標註「哪段是證據」[§4.4]。
- **換資料就能更新知識（index hot-swapping）**：用 82 位在 2016–2018 年間換人的世界領袖測試。用 2016 年索引答 2016 年領袖，正確率 70%；用 2018 年索引答 2018 年領袖，正確率 68%。索引和年份不對時，只剩 12% 和 4% [§4.5]。
- 增加檢索文件數：RAG-Sequence 的問答成績隨文件數增加而持續上升；RAG-Token 在 10 份文件時達到最高 [§4.5]。
- 對 FEVER 來說，關鍵字比對的 BM25 檢索效果最好；其他任務則是學習式檢索較好 [§4.5]。

## 限制
- 外部知識來源（例如維基百科）本身不可能完全正確、毫無偏見 [Broader Impact]。
- 文件編碼器和索引在訓練時固定不更新，只微調查詢編碼器和生成器 [§2.4]。
- 部分 MS-MARCO 問題光靠維基百科無法回答 [§3.2]。

## 相關概念頁
- [[concepts/what-is-rag]]
- [[concepts/hallucination]]
- [[concepts/embedding-and-retrieval]]
- [[concepts/knowledge-update]]
- [[concepts/lost-in-the-middle]]
