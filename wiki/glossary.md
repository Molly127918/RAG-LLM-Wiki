# 術語表

專有名詞依主題分類，格式為：`中文（English）`：白話解釋 → 相關概念頁。

## 基本概念
- **大型語言模型（Large Language Model，LLM）**：像 ChatGPT 這樣，讀過大量文字、能理解和產生語言的 AI。→ [[concepts/hallucination]]
- **幻覺（hallucination）**：AI 說出聽起來合理、其實是錯的內容。→ [[concepts/hallucination]]
- **檢索增強生成（Retrieval-Augmented Generation，RAG）**：AI 回答前先查資料，再根據資料作答。→ [[concepts/what-is-rag]]
- **參數記憶（parametric memory）**：模型訓練時記在自己內部的知識。→ [[concepts/what-is-rag]]
- **非參數記憶（non-parametric memory）**：放在模型外面、可以查閱的資料庫。→ [[concepts/what-is-rag]]
- **閉卷（closed-book）**：不給任何參考資料，只靠模型自己的記憶回答。→ [[concepts/lost-in-the-middle]]
- **知識密集任務（knowledge-intensive task）**：沒有參考資料，連人也很難完成的任務，例如回答冷門的事實問題。→ [[concepts/what-is-rag]]
- **token**：模型計算文字長度的單位，大約是一個中文字或半個英文單字。→ [[concepts/embedding-and-retrieval]]
- **提示（prompt）**：交給模型的輸入文字，包含問題和參考資料。→ [[concepts/what-is-rag]]

## 查資料相關
- **檢索器（retriever）**：RAG 中負責找資料的部分，像圖書館員。→ [[concepts/what-is-rag]]
- **生成器（generator）**：RAG 中負責讀資料、寫答案的部分。→ [[concepts/what-is-rag]]
- **索引（index）**：事先整理好、方便快速查找的資料目錄。→ [[concepts/what-is-rag]]
- **建立索引（Indexing）**：RAG 的第一步，事先把文件切塊、轉成向量、存進資料庫。→ [[concepts/what-is-rag]]
- **先找再讀（Retrieve-Read）**：最基本 RAG 的流程，先檢索、再讓模型閱讀並回答。→ [[concepts/rag-evolution]]
- **索引熱抽換（index hot-swapping）**：直接換掉外部資料庫，讓模型知識跟著更新，不用重新訓練。→ [[concepts/knowledge-update]]
- **BART**：一種會讀文字、也會寫文字的語言模型，最早的 RAG 用它來產生答案。→ [[concepts/what-is-rag]]
- **API（應用程式介面，Application Programming Interface）**：讓程式彼此溝通的窗口，例如讓 AI 查詢天氣、物流狀態等外部服務。→ [[concepts/agentic-rag]]
- **區塊（chunk）／切塊（chunking）**：把長文件切成小段，方便查找。→ [[concepts/embedding-and-retrieval]]
- **嵌入（embedding）**：把一段文字轉成一串數字，意思相近的文字，數字也相近。→ [[concepts/embedding-and-retrieval]]
- **向量（vector）**：嵌入轉出來的那串數字。→ [[concepts/embedding-and-retrieval]]
- **向量資料庫（vector database）**：專門存放向量、可以快速找出「最相近」資料的資料庫。→ [[concepts/embedding-and-retrieval]]
- **前 k 名（top-k）**：檢索時取出最相關的前 k 份資料。→ [[concepts/embedding-and-retrieval]]
- **稀疏檢索（sparse retrieval）／BM25**：依「有沒有相同字詞」來找資料的方法。→ [[concepts/embedding-and-retrieval]]
- **稠密檢索（dense retrieval）**：依「意思是否相近」來找資料的方法。→ [[concepts/embedding-and-retrieval]]
- **DPR（Dense Passage Retriever）**：一種稠密檢索器，最早的 RAG 就是用它。→ [[concepts/what-is-rag]]
- **混合檢索（hybrid retrieval）**：同時使用關鍵字比對和語意比對。→ [[concepts/embedding-and-retrieval]]
- **知識圖譜（knowledge graph）**：用「誰和誰有什麼關係」連成網狀的資料。→ [[concepts/rag-evolution]]
- **多跳（multi-hop）**：需要串連好幾份資料、分好幾步才能找到答案的問題。→ [[concepts/rag-limitations]]

## 改良技巧
- **查詢改寫（query rewriting）**：把使用者的問題改寫得更清楚，再拿去搜尋。→ [[concepts/advanced-techniques]]
- **重排序（reranking）**：把找到的資料重新排序，最相關的排到前面。→ [[concepts/advanced-techniques]]
- **迭代檢索（iterative retrieval）**：一邊寫答案、一邊重複查資料。→ [[concepts/advanced-techniques]]
- **遞迴檢索（recursive retrieval）**：把問題逐步拆小，一層一層往下查。→ [[concepts/advanced-techniques]]
- **自適應檢索（adaptive retrieval）**：由模型自己決定要不要查、何時停止。→ [[concepts/advanced-techniques]]
- **樸素 RAG（Naive RAG）**：最基本的「建索引、檢索、生成」三步驟 RAG。→ [[concepts/rag-evolution]]
- **進階 RAG（Advanced RAG）**：在檢索前後加上優化的 RAG。→ [[concepts/rag-evolution]]
- **模組化 RAG（Modular RAG）**：可以像積木一樣替換、組合模組的 RAG。→ [[concepts/rag-evolution]]
- **圖譜 RAG（Graph RAG）**：使用知識圖譜來查資料的 RAG。→ [[concepts/rag-evolution]]

## 代理式 RAG
- **AI 代理（agent）**：能自己規劃、使用工具、檢查成果的 AI。→ [[concepts/agentic-rag]]
- **代理式 RAG（Agentic RAG）**：由 AI 代理主導查資料流程的 RAG。→ [[concepts/agentic-rag]]
- **反思（reflection）**：AI 自己檢查並修正答案。→ [[concepts/agentic-rag]]
- **規劃（planning）**：AI 把大任務拆成小步驟。→ [[concepts/agentic-rag]]
- **工具使用（tool use）**：AI 呼叫搜尋、資料庫等外部工具。→ [[concepts/agentic-rag]]
- **多代理協作（multi-agent collaboration）**：多個 AI 代理分工合作。→ [[concepts/agentic-rag]]
- **修正式 RAG（Corrective RAG）**：會檢查找到的資料，不好就重找的 RAG。→ [[concepts/agentic-rag]]
- **自適應 RAG（Adaptive RAG）**：依問題難度決定查幾次的 RAG。→ [[concepts/agentic-rag]]

## 其他做法與比較
- **微調（fine-tuning）**：拿新資料繼續訓練模型，讓它把知識記進內部。→ [[concepts/rag-vs-fine-tuning]]
- **知識注入（knowledge injection）**：讓模型學會新知識的過程。→ [[concepts/rag-vs-fine-tuning]]
- **災難性遺忘（catastrophic forgetting）**：模型學了新東西，卻忘掉原本會的。→ [[concepts/rag-vs-fine-tuning]]
- **改寫版本（paraphrase）**：意思相同、說法不同的句子。→ [[concepts/rag-vs-fine-tuning]]
- **上下文視窗（context window）**：模型一次能讀進的內容上限。→ [[concepts/rag-vs-long-context]]
- **長上下文（Long-Context，LC）**：把整份長文件直接交給模型讀。→ [[concepts/rag-vs-long-context]]
- **Self-Route（自我路由）**：先用 RAG 試答，答不出來才改讀全文的混合方法。→ [[concepts/rag-vs-long-context]]
- **首因偏差（primacy bias）／近因偏差（recency bias）**：比較注意開頭／結尾資訊的傾向。→ [[concepts/lost-in-the-middle]]
- **序列位置效應（serial-position effect）**：心理學現象，人最記得清單的第一個和最後一個。→ [[concepts/lost-in-the-middle]]
- **干擾文件（distractor）**：看起來相關、其實不含答案的文件。→ [[concepts/lost-in-the-middle]]

## 評估
- **Ragas**：一套用 AI 當評審、不需要標準答案的 RAG 評估工具。→ [[concepts/rag-evaluation]]
- **GPT Score**：Ragas 論文中的比較方法，直接請 ChatGPT 替答案打 0 到 10 分。→ [[concepts/rag-evaluation]]
- **忠實度（faithfulness）**：答案的內容在參考資料裡有沒有根據。→ [[concepts/rag-evaluation]]
- **答案相關性（answer relevance）**：答案有沒有切題。→ [[concepts/rag-evaluation]]
- **上下文相關性（context relevance）**：找到的資料是否精簡、聚焦。→ [[concepts/rag-evaluation]]
- **拒答（negative rejection）**：資料裡沒有答案時，能老實說不知道。→ [[concepts/rag-evaluation]]
- **抗雜訊（noise robustness）**：不被相關但沒用的資料干擾。→ [[concepts/rag-evaluation]]
- **多模態（multi-modal）**：同時處理文字、圖片、聲音、影片等多種資料。→ [[concepts/rag-limitations]]
