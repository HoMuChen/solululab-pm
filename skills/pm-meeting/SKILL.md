---
name: pm-meeting
description: |
  整理會議紀錄、處理逐字稿、管理會議相關文件。Use when 使用者說「整理會議紀錄」、「會議筆記」、
  「處理逐字稿」、「今天跟客戶開會」、「meeting notes」、「幫我整理這次討論」、
  「transcript」、或提供了錄音轉出的逐字稿要求整理。
---

# 會議紀錄管理

## 檔案命名規則

所有會議相關檔案放在 `01-meetings/`，命名格式：

```
YYYY-MM-DD_主題.md                  # 整理後的會議筆記
YYYY-MM-DD_主題.mp3                 # 錄音原檔
YYYY-MM-DD_主題_transcript.md       # AI 轉出的逐字稿（原始）
YYYY-MM-DD_主題_attachments/        # 該次會議的附件
```

主題用簡短英文：`kickoff`、`requirement-review`、`demo-v1`、`scope-change`、`weekly-sync`。

## 整理會議紀錄的標準格式

```markdown
# YYYY-MM-DD 會議主題

## 基本資訊
- **日期**：YYYY-MM-DD
- **參與者**：
- **會議形式**：（線上/現場/電話）

## 討論摘要

（依討論主題分段整理，用自己的語言重述重點，不是逐字記錄）

### 主題一：XXX
- 重點內容
- 客戶的立場/需求
- 我方的回應/建議

### 主題二：XXX
- ...

## 決議事項

（明確列出已達成共識的決定）

1. [決議內容] — 負責人：XXX

## 待辦事項

（會後需要跟進的事項）

- [ ] [事項] — 負責人：XXX — 預計完成：YYYY-MM-DD
- [ ] [事項] — 負責人：XXX — 預計完成：YYYY-MM-DD

## 下次會議

- **預計日期**：
- **預計討論**：
```

## 從逐字稿整理的流程

當使用者提供逐字稿（transcript）要求整理時：

1. 先將原始逐字稿保存為 `YYYY-MM-DD_主題_transcript.md`
2. 閱讀逐字稿，提取關鍵資訊
3. 按上述標準格式產出整理後的會議筆記 `YYYY-MM-DD_主題.md`
4. 特別注意提取：
   - 客戶明確表達的需求或偏好
   - 已達成的決議
   - 尚未解決的問題（更新到 `questions.md`）
   - 客戶承諾要提供的資料

## 會後必做事項

每次整理完會議紀錄後，提醒使用者：

1. **更新 questions.md**：`02-requirements/questions.md`
   - 標記本次會議已解決的問題為 ✅
   - 新增本次會議中浮現的新問題為 ⬜
2. **更新 README.md**：在「最近活動」區塊新增本次會議記錄
3. **收到的客戶資料**：如果客戶在會議中提供或承諾提供資料，提醒放入 `02-requirements/client-inputs/`
