# security-tools — 保安科工具總專案

## 對話開始時請先讀
進度與最近更動都在 Obsidian：`secondbrain/security-tools/工作筆記.md`

## 工作模式
- **加新工具**：對 Claude 說「我想做一個 XXX 工具」→ Claude 會建 `tools/<工具名>/` 子資料夾並開始製作
- **結束工作**：對 Claude 說「**收工**」→ 自動 commit + push + 更新 Obsidian 工作筆記
- **接續工作**：對 Claude 說「讀工作筆記、告訴我上次做到哪」

## 工作桌 + 三個家
- 📋 GDrive 工作桌：`G:\我的雲端硬碟\security-tools\`（自動跨電腦同步）
- 🐙 GitHub repo：`a0933997949-eng/security-tools`（公開，網頁的家）
- 📘 Obsidian 駕駛艙：`secondbrain/security-tools/工作筆記.md`（想法的家）
- 🔥 Firebase 專案：`kucing-f2781`（資料的家）
- 🗄️ Supabase 專案：`xluqvelnpkxntbftcmwm`（SQL 資料的家）

## 工具清單
（之後加新工具時會自動更新）
- （尚無）

## 工作注意事項
- 涉及個資的工具一律去識別化（只用編號、代號）
- commit 訊息要寫清楚做了什麼 + 為什麼
- 收工前說「收工」讓 Claude 同步三方
- 敏感業務工具請啟用隱私模式（Frontmatter 加 sensitive: true）
