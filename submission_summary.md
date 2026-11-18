# 作業繳交摘要（發布後請填入網址）

**主題**：Financial Statement Analysis 101 — 財務報表分析入門

**LLM Wiki 介紹**：蒐集 SEC、SBA、CFI、Wikipedia 等八篇公開財務資料，整理成涵蓋三大財報、獲利、流動性、營運效率與財務警訊的 Wiki；原始與 Wiki Chunk 共 211 筆，使用 SQLite FTS5 在本機檢索。網頁版為 Wiki 靜態展示，非即時 LLM 檢索服務。

**LLM Wiki 成果連結**：［發布 GitHub Pages 後填入 index.html URL］

**教學 HTML 簡報連結**：［發布後填入 slides.html URL］

**Loop / Graph**：蒐集 → Ingest → 品質檢查 → Wiki / 索引 → 檢索 → 證據充分性與來源檢查 → 草稿 → 財務檢查 → HTML 生成與測試。正文缺漏、證據不足、計算錯誤會回到對應節點；檢索最多重試三次後停止該段生成。詳細流程圖及輸入輸出參見 `workflow_report.md`。

**一次執行及檢查**：上傳的 SQLite 確認含 211 筆 Chunk；HTML 具八個主投影片；來源審核發現 `raw_quote` 部分是 Wiki 摘要而非原文，因此改用正確標籤。修正版 Safari 人工測試確認來源矩陣開關、鍵盤切頁與三題互動測驗正常。完整原始日誌另存於本機專案 logs 資料夾。

**反思**：來源引用一致性為重要風險；將來源證據檢查從 HTML 產生後前移至檢索與草稿之間。尚未取得完整 Error Log，無法量化認定哪個節點最常出錯。
