---
name: pm-project-init
description: |
  建立新的客戶專案資料夾。Use when 使用者說「新專案」、「開新案子」、「建立專案」、「新增客戶」、
  「init project」、「create project」。從 _templates/_project-template/ 複製標準結構，
  包含 01-meetings 到 06-closure 六個階段資料夾、README.md、CLAUDE.md、questions.md。
---

# 新建專案

## 執行步驟

1. 確認專案命名：格式為 `客戶名-專案名`（全小寫英文，用 `-` 連接）
   - 範例：`acme-ai-monitoring`、`betacorp-data-platform`
   - 如果使用者沒提供英文名，協助轉換

2. 複製模板：
   ```bash
   cp -r _templates/_project-template/ ./客戶名-專案名/
   ```

3. 更新 README.md：引導使用者填入以下資訊
   - 客戶名稱
   - 專案名稱
   - 主要聯絡人與聯絡方式
   - 專案概述（2-3 句話）
   - 預計開始日期

4. 更新狀態為「洽談中」

5. 確認建立完成，提醒使用者：
   - 下一步通常是安排第一次會議
   - 會議前可以先在 `02-requirements/questions.md` 列出想了解的問題

## 專案資料夾結構

建立後的結構應為：

```
客戶名-專案名/
├── CLAUDE.md
├── README.md
├── 01-meetings/
├── 02-requirements/
│   ├── client-inputs/
│   └── questions.md
├── 03-proposal/
│   └── contract/
├── 04-spec/
├── 05-execution/
│   └── deliverables/
└── 06-closure/
```

## 注意事項

- 同一客戶的多個專案，客戶名部分要保持一致
- 如果 `_templates/_project-template/` 不存在，提醒使用者先建立模板資料夾
