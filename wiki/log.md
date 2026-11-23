# 紀錄

依時間由舊到新附加。ingest 依論文首次發表時間（arXiv 編號）由舊到新處理：
lewis2020（2005）→ liu2023（2307）→ es2023（2309）→ ovadia2023（2312.05934）→ gao2024（2312.10997）→ li2024（2407）→ singh2026（2501）。

## 2026-11-23｜ingest｜lewis2020
- 新增：sources/lewis2020、concepts/what-is-rag、concepts/hallucination、concepts/embedding-and-retrieval、concepts/knowledge-update、concepts/lost-in-the-middle（檢索文件數的段落）
- 修改：無（第一篇）
- 矛盾：無
- 自查：發現 1 處錯誤，已修正：來源頁「出處」寫了 NeurIPS 2020，但 PDF 本身沒有載明，改為註明「依 es2023 參考文獻所載」。其餘 17 個數字和章節核對無誤。

## 2026-11-23｜ingest｜liu2023
- 新增：sources/liu2023、concepts/lost-in-the-middle（主體）、concepts/rag-vs-long-context（「讀得長不代表讀得好」）
- 修改：concepts/advanced-techniques（重排序的依據）、concepts/rag-limitations（限制四）
- 矛盾：檢索文件數量是否越多越好：liu2023 §5（超過 20 份幾乎沒有進步）vs. lewis2020 §4.5（RAG-Sequence 持續上升）。已登記在 concepts/lost-in-the-middle。
- 自查：發現 1 處錯誤，已修正：「出處」TACL 改為註明依據原文致謝段落。其餘 8 個數字和章節核對無誤。

## 2026-11-23｜ingest｜es2023
- 新增：sources/es2023、concepts/rag-evaluation
- 修改：concepts/hallucination（冷門知識）、concepts/lost-in-the-middle（引用 liu2023 的段落）
- 矛盾：無
- 自查：發現 1 處錯誤，已修正：「出處」寫了 EACL 2024，原文沒有這項資訊，改為「arXiv 預印本（原文未載明發表會議）」。其餘 9 個數字和章節核對無誤。

## 2026-11-23｜ingest｜ovadia2023
- 新增：sources/ovadia2023、concepts/rag-vs-fine-tuning
- 修改：concepts/hallucination（模型答錯的五種原因）、concepts/knowledge-update、concepts/what-is-rag
- 矛盾：無（「微調＋RAG」的分歧要到 gao2024 才出現）
- 自查：發現 1 處原文內部不一致，已處理：§4.1 寫「四個任務」卻列出五個科目，來源頁以五個科目為準並加註。其餘 10 個數字和章節核對無誤。

## 2026-11-23｜ingest｜gao2024
- 新增：sources/gao2024、concepts/rag-evolution、concepts/advanced-techniques、concepts/rag-limitations
- 修改：concepts/what-is-rag（三步驟）、concepts/embedding-and-retrieval（切塊、稀疏與稠密檢索）、concepts/rag-vs-fine-tuning（課本比喻、適用場合）、concepts/rag-vs-long-context（RAG 仍不可取代）、concepts/rag-evaluation（三分數＋四能力）、concepts/lost-in-the-middle（「越多越好」是誤解）
- 矛盾：
  1. 「微調＋RAG」是否更好：gao2024 §II-D（可能最佳）vs. ovadia2023 §5（時事題反而變差）。已登記在 concepts/rag-vs-fine-tuning。
  2. 不相關文件是否有害：gao2024 §VII-B（轉述研究：準確率可提高超過 30%）vs. liu2023 §2.3（干擾文件讓表現變差）。已登記在 concepts/lost-in-the-middle。
- 自查：發現 1 處錯誤，已修正：concepts/rag-vs-long-context 寫成「2023 年底已能處理 20 萬 token」，但原文只說「目前」（本檔為 2024 年 3 月版），改為「gao2024 撰寫時（2024 年初）」。其餘 7 個數字和章節核對無誤。

## 2026-11-23｜ingest｜li2024
- 新增：sources/li2024
- 修改：concepts/rag-vs-long-context（主體：實驗結果、Self-Route）、concepts/rag-limitations（RAG 失敗的四種原因）、concepts/rag-evaluation（人工測試題的陷阱）、concepts/embedding-and-retrieval（300 字切塊）、concepts/lost-in-the-middle（k 越大越好）、concepts/advanced-techniques（多步推理的需求）
- 矛盾：
  1. 長上下文會取代 RAG 嗎：li2024 §3.3（LC 一致勝出）vs. liu2023 §2.3（長上下文模型不一定比較會用）、gao2024 §VII-A（RAG 不可取代）；li2024 §2 自己也提到 Xu et al. 2023 的相反結論。已登記在 concepts/rag-vs-long-context。
  2. 檢索文件數量的分歧，補上 li2024 §5.1 的說法。已更新 concepts/lost-in-the-middle。
- 自查：發現 1 處錯誤，已修正：「出處」寫了 EMNLP 2024，原文沒有這項資訊，改為「arXiv 預印本」。另外原文內部有數字不一致（Gemini 交給 RAG 的比例：§4.2 寫 82%、§4.3 寫 81.74%、Table 1 平均為 76.78%），Wiki 只引用「超過一半」(§4.3)，並在來源頁加註。其餘 18 個數字和章節核對無誤。

## 2026-11-23｜ingest｜singh2026
- 新增：sources/singh2026、concepts/agentic-rag
- 修改：concepts/rag-evolution（圖譜 RAG、代理式 RAG）、concepts/rag-limitations（檢索瓶頸、成本、安全）、concepts/rag-evaluation（過程導向的評估）、concepts/what-is-rag（三分法）
- 矛盾：「樸素 RAG」用什麼方法檢索：singh2026 §2.3.1（關鍵字 TF-IDF／BM25）vs. gao2024 §II-A（嵌入向量）；lewis2020 §2.2 早已使用向量檢索。已登記在 concepts/rag-evolution。
- 自查：無數字錯誤（本篇沒有實驗數字）。特別注意：§5 的「使用情境」範例回答中出現的數字（例如 20%、120 萬個工作、50% 相關性、15% 成長）都是示意用的虛構輸出，Wiki 一律不引用，並在來源頁加註。

## 2026-11-23｜lint｜全部頁面
檢查 9 項，共修正 15 處：
1. 斷鏈：0 處。
2. 未標記的類比：0 處需要修正。concepts/rag-vs-fine-tuning 的「三個學生」「課本 vs. 學生」比喻出自論文本身（ovadia2023 §1、gao2024 §II-D），屬於引用事實、已附出處，不加 💡 標記。
3. 太技術：修正 5 處。
   - concepts/what-is-rag：替 DPR、BART 加上白話說明。
   - concepts/lost-in-the-middle：替 RAG-Sequence、RAG-Token 加上白話說明。
   - concepts/rag-vs-fine-tuning：替「Mistral 7B」說明是 70 億參數的開源模型。
   - concepts/agentic-rag：替 API 加上白話說明。
   - concepts/rag-vs-long-context：刪去沒有解釋的「Transformer」。
4. 缺類比：0 處（12 個概念頁各有 2–3 個 💡類比）。
5. 類比失真：修正 1 處。concepts/knowledge-update 的「重印整本百科全書」誇大了重新訓練的成本，改為「重新改版，費時費工」。
6. 缺引用：修正 3 處。
   - concepts/agentic-rag：9 處只寫 `[§x]` 的引用，補上 `[[sources/singh2026]]`（算 1 處修正）。
   - concepts/rag-vs-long-context：「早期模型只能讀幾千字」沒有出處，改為引用 liu2023 §1 的「512 到 2,048 個 token」。
   - concepts/lost-in-the-middle：「畫成圖形就像字母 U」改為原文用語「U 型表現曲線」，避免像是沒標記的類比。
   - 其餘條列項目都在已附引用的引導句之下，視為已引用。
7. 數字核對：69 個數字已用文字比對逐一回到 raw/ 原文確認，全部找得到；章節也逐一核對。
8. 孤兒頁：0 處（index.md 是入口頁，不算孤兒）。
9. 索引完整：所有頁面都在 index.md。術語表補上 6 個缺漏的術語：建立索引（Indexing）、先找再讀（Retrieve-Read）、索引熱抽換（index hot-swapping）、BART、API、GPT Score。

## 2026-11-23｜review｜人工審查
- 抽查 6 處：6 處正確。ovadia2023 一處：經回查原文 §4.1 開頭的 'four distinct tasks'，原文確有不一致，註記保留；人工審查初判有誤，原因是只讀了段落後半。審查規則補充：判定錯誤時須附原文完整句子。
- 發現：「出處」錯誤在 4 篇重複出現 → 規則前移到 ingest 步驟（已寫入 CLAUDE.md 第 5 節）
- 決定：簡報要講的分歧為「長上下文會取代 RAG 嗎」「檢索文件越多越好嗎」，「微調＋RAG」簡單帶過，其餘兩項不講
- 引用檢查：混合多篇論文的條列清單都已逐點附引用；單一論文的清單維持在引導句引用，不需修改

## 2026-11-23｜slides｜slides/index.html
- 產出：slides/index.html，單一 HTML 檔，共 19 張。順序依人工審查調整：1–11 → 怎麼查得更好 → RAG 的演進 → 代理式 RAG → 評估 → 限制 → 長上下文 → 長上下文分歧 → 總結。
- 風格：依 CLAUDE.md 第 7 節。圓體從 Google Fonts 載入 Huninn（粉圓），失敗時退回微軟正黑體；封面和總結頁放書本吉祥物；鍵盤左右鍵換頁，右下角顯示來源和頁碼。
- 貫穿例子「學校圖書館這學期幾點關門？」用在第 2、5、8 張，標成 💡 示意，不附論文來源。
- 數字白話化：第 9 張改成 48% → 50%、RAG 88%；第 8 張說明 70%／4% 各代表什麼情況；第 17 張只保留「100 萬 token」一個主要數字。
- 版面檢查：在瀏覽器量測 19 張的內容範圍。第 8 張右欄太貼近頁尾，已縮小大數字。
- 逐張核對 wiki，修正 5 處：
  1. 第 10 張：「可能下降超過 20%」沒有說明是哪個模型，改為「有的模型下降超過 20%」（wiki：以 GPT-3.5-Turbo 為例）。
  2. 第 11 張：「2020 年的研究：成績會跟著上升」太絕對，改為「大多會」（wiki：RAG-Token 在 10 份時最好）。
  3. 第 11 張：「+1.5%」補上小字「以 GPT-3.5-Turbo 為例」（wiki：Claude-1.3 約 1%）。
  4. 第 15 張：「資料相關性」和 wiki 用語不一致，改為「上下文相關性」。
  5. 第 14 張：「專案經理」類比原本不在 wiki，已補進 concepts/agentic-rag 的 💡類比。
- 每張的圖示控制在 1–2 個（💡 標記也算在內），已刪去第 2、6、7、8 張標題的多餘 emoji。
- WIKI 缺口：無。
