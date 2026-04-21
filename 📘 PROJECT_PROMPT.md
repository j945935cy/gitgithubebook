📘 PROJECT_PROMPT.md（強化版：含實例演習）
# 專案名稱
Git & GitHub 實戰教學書（搭配 VS Code）

# 專案目標
建立一套完整的「Git + GitHub + VS Code 教學教材」，同時輸出：
1. 網頁版電子書（HTML / CSS / JS）
2. EPUB 電子書
3. GitHub Pages 可部署網站

並加入：
👉「常用情境實例演習單元（Scenario-based Practice）」

---

# 目標使用者
- 高中生 / 大學生
- 初學程式設計者
- 教師教學使用

---

# 教學定位
- 重實作（操作導向）
- 每章都能「做出東西」
- 強調 VS Code 操作流程

---

# 專案結構（請自動建立）

project-root/
│
├── index.html
├── toc.html
│
├── style/
│   └── main.css
│
├── js/
│   └── main.js
│
├── chapters/
│   ├── ch01.html
│   ├── ch02.html
│   └── ...
│
├── labs/                     # ⭐新增：實例演習
│   ├── lab01-student-repo.html
│   ├── lab02-push-to-github.html
│   ├── lab03-collaboration.html
│   └── ...
│
├── assets/
│   └── images/
│
├── README.md
└── PROJECT_PROMPT.md

---

# UI 設計要求

風格：
- 類似 GitBook / Notion / Medium
- 左側目錄 + 右側內容
- 行動裝置可閱讀

---

# 教學章節規劃

（略，維持原 10 章）

---

# ⭐ 新增：常用情境實例演習單元（非常重要）

每個 lab 必須是：

- 真實情境
- 有完整步驟
- 可直接操作
- 有成果
- 加入合適相關說明圖形

---

## Lab 1：建立學生專題 Repo

### 情境說明
你是一名學生，要交一個「網頁專題」，需要：

- 建立 GitHub repo
- 用 VS Code 管理
- 上傳作品

---

### 操作步驟（必須條列）

1. 到 GitHub 建立新 repo
2. 設定 repo 名稱（例如：my-first-project）
3. 開啟 VS Code
4. 使用 Git: Clone
5. 開啟資料夾

---

### 本機操作

```bash
git clone https://github.com/你的帳號/my-first-project.git
建立專案內容
新增 index.html
新增 style.css
提交與上傳
git add .
git commit -m "初始專題上傳"
git push
VS Code 操作
Source Control → Commit
點擊 Push
成果
GitHub 上看到檔案
可以分享 repo 連結
常見錯誤
沒登入 GitHub
repo 設 private 無法分享
push 失敗（權限問題）
延伸練習
加 README.md
加圖片
Lab 2：推資料到 GitHub（Push）
情境說明

你已經有專案，現在修改內容，需要更新到 GitHub

操作流程
修改檔案
存檔
commit
push
指令
git add .
git commit -m "更新首頁內容"
git push
VS Code 操作
開啟 Source Control
查看變更
Commit
Push
成果
GitHub 出現最新版本
常見錯誤
忘記 commit
push 前沒 pull（衝突）
延伸練習
修改多個檔案
查看 commit 歷史
Lab 3：多人協作（選做）
fork 專案
pull request
每章格式（維持）

每章必須包含：

概念
指令
VS Code 操作
常見錯誤
小練習
⭐ Lab 格式（統一）

每個 lab 必須包含：

情境說明
操作步驟（條列）
指令
VS Code 操作
成果
常見錯誤
延伸練習
README.md 要求

需包含：

專案介紹
使用方式
GitHub Pages 部署方式
章節 + Lab 列表
額外限制
使用純 HTML / CSS / JS
不使用框架
每個 Lab 為獨立 HTML 頁
Codex 任務流程
建立專案結構
建立首頁
建立 3 個章節
建立 2 個 Lab
建立 CSS
建立 README.md
確保可 GitHub Pages 部署
最終成果

一個可：

教學
實作
練習

的完整 Git 教學電子書網站


---

## 補充建議（教學價值會大幅提升）

你可以再加這幾個 Lab（很實用）：

- Lab 4：修正 Git 錯誤（push fail）
- Lab 5：回到上一版本（rollback）
- Lab 6：建立分支做實驗
- Lab 7：GitHub Pages 發佈網站

---

## 一句話總結

這次升級的重點是：

- ❌ 只是「講 Git」
- ✅ 變成「學生真的會用 Git」

---

如果你要，我可以幫你再做一版：

- 「高中生講義版（更白話）」
- 或「A4 可列印實作單」