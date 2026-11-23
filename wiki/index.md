# RAG LLM Wiki 索引

本 Wiki 整理 7 篇 RAG（檢索增強生成）論文，供製作給一般大眾看的中文教學簡報使用。

## 教學故事線

簡報依照以下順序展開，每一段對應一個概念頁：

| # | 段落 | 核心問題 | 概念頁 |
|---|---|---|---|
| 1 | AI 會亂講 | 為什麼聰明的 AI 還會說錯、會過時？ | [[concepts/hallucination]] |
| 2 | 先查再答 | RAG 是什麼？怎麼運作？ | [[concepts/what-is-rag]] |
| 3 | 怎麼查 | 電腦怎麼找到「意思相近」的資料？ | [[concepts/embedding-and-retrieval]] |
| 4 | 換資料就更新 | 不用重新訓練，怎麼讓 AI 知道新的事？ | [[concepts/knowledge-update]] |
| 5 | 開書考 vs. 考前苦讀 | 為什麼不直接把知識教進 AI 腦中？ | [[concepts/rag-vs-fine-tuning]] |
| 6 | 資料給越多越好嗎 | AI 會不會漏讀中間的資料？ | [[concepts/lost-in-the-middle]] |
| 7 | AI 能讀整本書了 | 長上下文模型會取代 RAG 嗎？ | [[concepts/rag-vs-long-context]] |
| 8 | RAG 的演進 | RAG 怎麼從簡單版變成積木版？ | [[concepts/rag-evolution]] |
| 9 | 怎麼查得更好 | 改寫問題、重新排序、反覆查找 | [[concepts/advanced-techniques]] |
| 10 | 讓 AI 自己決定怎麼查 | 什麼是代理式 RAG？ | [[concepts/agentic-rag]] |
| 11 | 怎麼打分數 | 怎麼知道 RAG 做得好不好？ | [[concepts/rag-evaluation]] |
| 12 | 限制與未來 | RAG 在哪些地方會失敗？ | [[concepts/rag-limitations]] |

## 概念頁

- [[concepts/hallucination]]：大型語言模型會產生幻覺、知識過時、記不住冷門知識。
- [[concepts/what-is-rag]]：RAG 的定義、三個步驟、兩個角色，以及帶來的好處。
- [[concepts/embedding-and-retrieval]]：切塊、向量、相似度，以及關鍵字比對和語意比對兩種找法。
- [[concepts/knowledge-update]]：換掉資料庫就能更新知識，附世界領袖實驗。
- [[concepts/rag-vs-fine-tuning]]：RAG 和微調的比較，RAG 在新知識上明顯勝出。
- [[concepts/lost-in-the-middle]]：模型容易忽略中間的資訊，資料給越多不一定越好。
- [[concepts/rag-vs-long-context]]：長上下文模型成績較好，但 RAG 便宜很多；介紹 Self-Route 混合方法。
- [[concepts/rag-evolution]]：從樸素、進階、模組化，到圖譜和代理式 RAG。
- [[concepts/advanced-techniques]]：查詢改寫、重排序、壓縮，以及迭代、遞迴、自適應檢索。
- [[concepts/agentic-rag]]：AI 代理的組成、四種工作模式、常見架構與使用注意事項。
- [[concepts/rag-evaluation]]：Ragas 的三個評分面向，以及三分數加四能力的評估架構。
- [[concepts/rag-limitations]]：資料錯誤、檢索失敗、不擅長的問題類型、成本與安全。

## 來源頁（依發表時間由舊到新）

- [[sources/lewis2020]]：提出 RAG 的原始論文（2020），證明先查再答更準確，而且能換資料更新知識。
- [[sources/liu2023]]：發現模型會「迷失在中間」，資料放中間最容易被忽略（2023 年 7 月）。
- [[sources/es2023]]：提出 Ragas，不需要標準答案的 RAG 自動評估方法（2023 年 9 月）。
- [[sources/ovadia2023]]：比較微調和 RAG，RAG 在注入新知識上全面勝出（2023 年 12 月）。
- [[sources/gao2024]]：RAG 綜述，整理樸素、進階、模組化三階段與各種技術（2023 年 12 月首發，2024 年版）。
- [[sources/li2024]]：比較 RAG 和長上下文模型，提出 Self-Route（2024 年 7 月）。
- [[sources/singh2026]]：代理式 RAG 綜述，整理代理設計模式、架構分類與實務教訓（2025 年 1 月首發，2026 年版）。

## 其他頁面

- [[glossary]]：術語表，英文原文對照白話中文解釋。
- [[log]]：ingest、lint、矛盾的處理紀錄。
