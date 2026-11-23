# Dog Signals 101 — 讀懂狗狗的身體語言 🐶

**LLM Wiki × 教學型 HTML 簡報**

本專案以第一次養狗的新手飼主為主要讀者，透過 LLM Wiki 整理狗狗身體語言的相關知識，並製作成可以實際瀏覽的互動式 HTML 教學簡報。

## 1. 專案介紹

狗狗會透過尾巴、耳朵、眼神、身體姿勢與聲音傳達訊息，但單一動作不一定代表固定的情緒。

本專案希望讓新手飼主學習如何綜合觀察狗狗的行為與環境，避免過度解讀。

## 2. LLM Wiki 知識庫

本專案參考 Karpathy 的 LLM Wiki 設計概念，採用「先討論、後生成」的方式建立知識庫。

Wiki 主要包含：

- **Raw Sources：** 保存原始資料與來源紀錄。
- **Wiki：** 使用 Markdown 整理知識，建立索引與交叉連結。
- **Schema：** 透過 `AGENTS.md` 定義 AI 的工作規範。

本次共完成 5 篇有效資料 Ingest，來源包括 AKC、ASPCA、VCA Animal Hospitals 與 Dogs Trust。

[查看 Wiki 知識庫](./wiki/)

[查看 AGENTS.md](./AGENTS.md)

[查看 Ingest 操作紀錄](./log.md)

## 3. HTML 教學簡報

**[點此開啟 Dog Signals 101 互動式 HTML 簡報](https://nadia-bit-dot.github.io/dog-signals-101/)**

簡報共 9 頁，內容包含：

1. Dog Signals 101 封面
2. 狗狗如何透過身體語言溝通
3. 搖尾巴一定代表開心嗎？
4. 耳朵與眼神的觀察
5. 緊張與壓力訊號
6. 吠叫與聲音溝通
7. 常見情境判讀
8. 互動測驗
9. 重點整理與參考來源

簡報採用 Editorial 雜誌式排版，使用真實狗狗攝影照片，並支援翻頁與互動測驗。

## 4. Loop / Graph 工作流程

本專案的主要流程為：

**需求確認 → 來源蒐集 → 來源檢查 → Ingest → Wiki 更新 → Lint → Query Wiki → 整理教學內容 → 圖片檢查 → HTML 生成 → 最終檢查**

當資料來源、Wiki 內容或 HTML 顯示未通過檢查時，流程會返回對應階段進行修正。

[查看 Workflow / Graph](./workflow.md)

## 5. 實際執行與檢查

本次執行的主要結果：

| 檢查項目 | 結果 |
|---|---|
| 有效資料 Ingest | 5 篇 |
| Markdown 相對連結 | 0 個失效連結 |
| HTML 簡報 | 9 頁 |
| 內嵌真實照片 | 8 張 |
| JavaScript 語法檢查 | 通過 |

實作過程中曾遇到資料使用限制、圖片裁切、尺寸不一致與圖片重複等問題，後續透過提前檢查來源與圖片原檔進行改善。

[查看最終檢查報告](./final-check-report.md)

[查看 Wiki Lint 報告](./lint-report.md)

## 6. Workflow 反思

本次最常遇到問題的是 HTML 圖片整合與版面檢查階段。

因此，我將圖片來源、解析度、尺寸比例與重複檢查提前至 HTML 生成之前，並將資料使用限制檢查提前至 Ingest 之前。

這次作業讓我理解，AI Workflow 不只是產生內容，也需要在適當節點進行驗證與修正。

[查看完整反思報告](./reflection.md)

---

**Project:** Dog Signals 101

**Topic:** LLM Wiki × Interactive HTML Tutorial
