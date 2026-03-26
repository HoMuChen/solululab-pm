# Solululab PM — Claude Code Plugin

客戶專案管理工作流 Plugin，適用於接案型軟體開發公司的客戶專案全生命週期管理。

## 包含的 Skills

| Skill | 觸發時機 | 功能 |
|-------|----------|------|
| `pm-project-init` | 「新專案」、「開新案子」 | 從模板建立標準專案資料夾 |
| `pm-meeting` | 「整理會議紀錄」、「處理逐字稿」 | 會議紀錄整理、逐字稿處理、會後追蹤 |
| `pm-requirement` | 「整理需求」、「更新 questions」 | 需求文件撰寫、問題追蹤、客戶資料管理 |
| `pm-proposal` | 「寫提案」、「報價」 | 提案書、報價單、合約管理 |
| `pm-spec` | 「寫規格書」、「排時程」 | 功能規格書、系統架構、時程規劃 |
| `pm-execution` | 「客戶要加功能」、「change request」 | 變更追蹤、問題管理、交付物管理 |
| `pm-closure` | 「結案」、「驗收」、「覆盤」 | 驗收紀錄、覆盤報告、結案流程 |

## 安裝

### 從 GitHub 安裝

```bash
claude plugin add solululab/solululab-pm
```

### 本地開發測試

```bash
claude --plugin-dir ./solululab-pm
```

安裝後執行 `/reload-plugins` 載入。

## 前置需求

此 plugin 預期你的專案根目錄有以下結構（可搭配 solululab 資料夾模板使用）：

```
solululab/
├── _templates/
│   └── _project-template/    # pm-project-init 會從這裡複製
├── _company/
├── _resources/
└── [客戶名-專案名]/           # 各專案資料夾
```

## 專案生命週期

```
新專案 → 會議溝通 → 需求釐清 → 提案報價 → 規格設計 → 執行開發 → 結案驗收
  │         │          │          │          │          │          │
  v         v          v          v          v          v          v
pm-init  pm-meeting  pm-req   pm-proposal  pm-spec  pm-exec   pm-closure
```

## 授權

MIT
