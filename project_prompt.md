# Project Prompt

## Project Goal

建立一個可直接部署到 GitHub Pages 的靜態教學網站，主題為 `Git`、`GitHub`、`VS Code` 入門。此網站同時具備：

- 教學網站的清楚結構與可讀性
- 練習導向的 Lab 體驗
- Apple 官網風格的乾淨、高級、克制視覺

這不是一般部落格，也不是純文件站，而是一個有品牌感的教學型電子書網站。

## Primary Audience

- Git / GitHub 初學者
- 想用 VS Code 學版本控制的學生
- 想完成第一個 GitHub 專案與 GitHub Pages 部署的入門者

## Product Positioning

產品定位為「可閱讀、可操作、可練習」的學習網站。

內容要做到：

- 讓初學者看得懂
- 讓使用者知道下一步要做什麼
- 讓每個章節都能搭配實際練習

視覺要做到：

- 像 Apple 官網一樣乾淨、精緻、可信賴
- 不要做成一般模板站
- 不要做成資訊過滿的傳統教材頁

## Design Direction

整體視覺以 Apple 官網風格為唯一主要參考。

只借鏡以下元素：

- Apple：留白、比例、層次、精緻感、產品感
- GitBook：文件導覽結構

不要同時混入過多 `Notion`、`Medium`、SaaS dashboard、部落格模板語言，避免風格失焦。

## Visual Style

關鍵字：

- Minimal
- Premium
- Calm
- Spacious
- Editorial
- Soft contrast
- Apple-inspired
- Subtle green accent

畫面特徵：

- 大面積留白
- 清楚而穩定的段落節奏
- 精簡卡片與低存在感邊框
- 柔和陰影與乾淨背景
- 高可讀性字級層次

## Color System

整體配色以黑、白、灰為核心，搭配少量低飽和淡綠色點綴。

### Design Tokens

```css
:root {
  --color-bg: #f5f7f4;
  --color-surface: #ffffff;
  --color-surface-soft: #eef3ee;
  --color-text: #161816;
  --color-text-muted: #5f675f;
  --color-border: #d8e0d8;
  --color-accent: #b8d3bf;
  --color-accent-strong: #8fb59a;
  --color-highlight: #e3efe6;
  --shadow-soft: 0 20px 60px rgba(22, 24, 22, 0.08);
  --radius-lg: 28px;
  --radius-md: 18px;
  --radius-sm: 12px;
  --content-max: 1200px;
}
```

### Color Rules

- 背景以 `--color-bg`、`--color-surface` 為主
- 文字以 `--color-text`、`--color-text-muted` 為主
- 淡綠色只用於 hover、標籤、重點區塊、icon、分隔強調
- `--color-accent-strong` 不可大面積鋪滿整頁
- 禁止使用高飽和綠、螢光綠、科技藍紫漸層

## Typography

字體方向需現代、乾淨、具設計感，避免預設系統字堆疊造成普通感。

建議：

- 英文與數字可用 `SF Pro Display` 風格或相近無襯線字體
- 中文可搭配乾淨、現代的黑體
- 標題字重明確，內文字重正常，避免全部過粗

字級層次建議：

- Hero Title: 48px 至 72px
- Section Title: 28px 至 40px
- Card Title: 20px 至 24px
- Body: 16px 至 18px
- Meta / Caption: 13px 至 14px

## Motion

動效必須克制且有目的，不可浮誇。

可使用：

- 區塊淡入
- 卡片輕微上浮
- 按鈕與連結的柔和 hover
- 目錄或導覽的平滑切換

避免：

- 過度彈跳
- 強烈縮放
- 花俏粒子效果
- 與學習內容無關的炫技動畫

## MVP Scope

第一版必做頁面：

- `index.html`
  首頁，展示專案定位、學習價值、章節入口、Lab 入口
- `toc.html`
  課程總目錄頁，列出所有章節與 Lab
- `chapters/ch01.html`
  第一章內容頁
- `chapters/ch02.html`
  第二章內容頁
- `labs/lab01-student-repo.html`
  第一個 Lab 練習頁
- `README.md`
  專案說明與部署方式

若時間足夠可延伸：

- `chapters/ch03.html`
- `labs/lab02-push-to-github.html`
- `labs/lab03-collaboration.html`

## Required Components

所有頁面需盡量共用一致元件與樣式系統。

第一版至少包含以下元件：

- 全站頂部導覽列
- Hero 區
- 章節卡片列表
- Lab 卡片列表
- 文章內容區
- 側邊或頁內目錄
- 上一頁 / 下一頁導覽
- 頁尾

建議元件：

- 重點提示框
- 指令區塊
- 步驟流程區
- 常見錯誤提醒框

## Information Architecture

網站內容結構建議如下：

```text
project-root/
├─ index.html
├─ toc.html
├─ style/
│  └─ main.css
├─ js/
│  └─ main.js
├─ chapters/
│  ├─ ch01.html
│  ├─ ch02.html
│  ├─ ch03.html
│  └─ ...
├─ labs/
│  ├─ lab01-student-repo.html
│  ├─ lab02-push-to-github.html
│  ├─ lab03-collaboration.html
│  └─ ...
├─ assets/
│  └─ images/
├─ README.md
└─ project_prompt.md
```

## Content Plan

建議章節：

- Chapter 1: Git 與 GitHub 是什麼
- Chapter 2: 安裝 Git 與設定環境
- Chapter 3: 用 VS Code 開始第一個版本控制專案
- Chapter 4: clone、add、commit、push 流程
- Chapter 5: GitHub repository 基本管理
- Chapter 6: branch 與 collaboration 入門
- Chapter 7: pull request 基礎
- Chapter 8: GitHub Pages 發布網站

## Lab Plan

每個 Lab 頁面都應包含：

- 練習目標
- 先備條件
- 操作步驟
- 指令範例
- VS Code 操作對照
- 預期結果
- 常見錯誤與排除

建議 Lab：

- Lab 1: 建立第一個 GitHub Repo
- Lab 2: 將本機專案推送到 GitHub
- Lab 3: 協作與 Pull Request 入門
- Lab 4: 排除 push fail 與常見 Git 錯誤
- Lab 5: 還原錯誤提交與 rollback 基礎
- Lab 6: 分支合併與衝突處理
- Lab 7: GitHub Pages 發布與更新網站

## Page-Level Guidance

### Homepage

首頁應包含：

- 清楚的主標題與副標
- 這個網站能學到什麼
- 章節入口
- Lab 練習入口
- GitHub Pages / 靜態網站特色說明
- 簡短但有質感的視覺區塊

首頁不應該一開始就塞滿長文教材。

### Chapter Page

章節頁應包含：

- 章節標題
- 章節摘要
- 內文段落
- 重點整理
- 範例指令或示意區塊
- 前後頁切換

### Lab Page

Lab 頁要比一般章節更重視操作感。

至少包含：

- 任務標題
- 難度或建議時間
- 操作步驟
- 指令區塊
- 成功條件
- 常見錯誤

## Writing Style

文字風格需：

- 清楚
- 直接
- 友善
- 初學者可理解

避免：

- 過度學術
- 過長段落
- 空泛品牌文案
- 太像 AI 自嗨式描述

## Frontend Rules

- 使用 HTML、CSS、JavaScript 製作
- 優先採用語意化 HTML
- CSS 需集中管理色彩、間距、圓角、陰影、字級
- JavaScript 只處理必要互動，不引入沉重框架
- 響應式設計需同時照顧桌機與手機
- 可先不做深色模式

## Responsive Rules

- 手機版仍需保留 Apple 式留白感，但不能過於空洞
- 卡片與段落在小螢幕需有清楚間距
- 導覽在手機上可折疊
- Hero 區文字不可因換行變得過度擁擠

## Accessibility Rules

- 文字與背景需有足夠對比
- 連結、按鈕、hover 狀態需可辨識
- 內容區塊標題層級要正確
- 不能只靠顏色傳達狀態

## Avoid

- 不要做成 SaaS 後台
- 不要做成普通部落格模板
- 不要大量使用厚重陰影
- 不要使用高飽和霓虹色
- 不要塞滿資訊導致首頁失去節奏
- 不要同時混太多設計風格

## Deliverable Expectation

交付結果需讓人一打開就感受到：

- 這是一個高品質教學網站
- 視覺乾淨成熟，有 Apple 風格影響
- 內容結構清楚，能直接開始學習
- 後續擴充章節與 Lab 時不需要重做整個系統

## Execution Priority

若由 AI 或前端直接開工，優先順序如下：

1. 先完成全站版型系統與首頁
2. 再完成 `toc.html` 與 2 個章節頁
3. 再完成至少 1 個 Lab 頁
4. 最後補互動細節與內容擴充
