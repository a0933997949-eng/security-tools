# Memory — security-tools 專案

## 📝 開工記錄（最新）

#### 2026-05-25 — 開工指令
- 啟動時間：2026-05-25
- 用戶指令：「開工」→ 合併 CLAUDE.md 並統一所有檔案至 security-tools/
- 規則版本：統一版 CLAUDE.md（2026-05-25）
- 執行狀態：✅ 已完成，所有檔案統一在 security-tools/

---

## 🔴 最高優先規則

**執行任何操作前，第一步必須讀取**：
- `G:\我的雲端硬碟\security-tools\CLAUDE.md`（包含所有工作規則與行為準則）

**Why:** CLAUDE.md 包含所有工作規則、六大指令流程、強制規範、隱私模式規則。未讀取直接操作可能違反強制規範，導致工作混亂或洩露敏感信息。

---

## 🔒 隱私模式永久規則（強制優先級最高）

### 快速定義
**隱私模式**保護警察系統敏感信息：不訓練 ✅ | 不記錄位置 ✅ | 可存檔但保護 ✅ | 不記憶細節 ✅ | 不分享 ✅

### 自動啟用場景（主動偵測詢問）
- 涉及員警個人姓名或身份號
- 提及案件編號、受害人信息
- 討論人事評估、紀律調查
- 涉及首長行動或安全措施

### 隱私模式下的操作規則
```
✅ 允許：/練化、/轉存 等指令（自動添加 sensitive: true）
✅ 必須：Frontmatter 添加 sensitive: true 標籤
✅ 必須：在 log.md 標註「【敏感檔案】」
❌ 禁止：在 MEMORY.md 記錄敏感細節（僅記錄位置）
❌ 禁止：分享敏感檔案至 security-tools/ 以外的公開位置
```

---

## 👤 用戶身份

用戶是**警察局保安科長**，工作對象：基層員警（教導）、長官（開會報告）。

**回答偏好**：繁體中文、詳細重點式、每個回答含 ✅ 優點 / ⚠️ 風險 / 💡 建議。

---

## 📁 專案結構

**security-tools 路徑**：`G:\我的雲端硬碟\security-tools\`

```
security-tools/
├── CLAUDE.md        ← 統一行為規則（本機完整版）
├── MEMORY.md        ← 跨會話記憶（本檔）
├── tools/           ← 各工具子資料夾
├── .gitignore
└── README.md（待建）
```

**三個家 + 兩個資料庫**：
- 📋 GDrive：`G:\我的雲端硬碟\security-tools\`
- 🐙 GitHub：`a0933997949-eng/security-tools`
- 📘 Obsidian：`secondbrain/security-tools/工作筆記.md`
- 🔥 Firebase：`kucing-f2781`
- 🗄️ Supabase：`xluqvelnpkxntbftcmwm`

---

## 🛠️ 六大核心指令

| 指令 | 功能 | 時機 |
|------|------|------|
| `/練化` | 精煉+晉升+自動歸檔（五階段） | 隨時 |
| `/轉存` | 法令轉化+存檔至8層資料夾 | 收到法令時 |
| `/wiki-ingest` | 知識攝取 | 每週末 |
| `/wiki-query` | 知識查詢（決策支援） | 頻繁 |
| `/wiki-lint` | 知識庫巡檢 | 每月底 |
| `/簡報大綱製作` | 智能生成簡報大綱（五步驟） | 需要簡報時 |
| **開工** | 接續上次工作 | 每次對話開始 |
| **收工** | 三方同步（GDrive + GitHub + Obsidian） | 每次結束 |

---

## ⚠️ 強制規範

- 所有新檔案自動歸檔至正確位置，不等待用戶指示
- `.claude/` 永遠不要 commit（.gitignore 已排除）
- commit 訊息要清楚說明做了什麼 + 為什麼
- 涉及個資的工具一律去識別化（只用編號、代號）

---

## 📌 五大核心工作流指令（詳細版）

### 1️⃣ `/練化[文件名]` — 精煉 + 晉升 + 自動歸檔

**完整七階段流程**（自動執行，無中斷）：
- Step_0：全路徑搜尋檔案 + 用戶確認位置
- **Step_0.5：代碼層預檢（Frontmatter、iframe、Mermaid、YouTube Video ID 補充）**
- Step_1-3：修正三項缺陷
- Step_4.5：代碼層驗證
- Step_4.9：建立雙向 Wiki 連結
- Step_5：強制歸檔（移動至 raw/archive/、更新統計、記錄日誌）
- Step_6：輸出精煉報告

**Step_0.5 YouTube Video ID 補充流程**：
- 若 video_url 或 video_id 含 [video_id] 佔位符 → 詢問用戶取得實際 YouTube 連結
- 自動更新四個位置：Frontmatter video_url、video_id、Callout 連結、iframe src
- 同步更新 archive 版本

**關鍵規則**：
- ✅ Step_4.9 + Step_5 強制執行，不可跳過
- ❌ 禁止留下 [video_id] 佔位符進入 Phase 1

### 2️⃣ `/轉存 [法令名稱]` — 法令轉化 + 自動存檔

**8 層資料夾對應**：01通用法規 / 02民防防空 / 03槍械刀械 / 04維安反恐 / 05選舉治安 / 06監視個資 / 07精神衛生 / 08跨域法規

### 3️⃣ `/wiki-ingest` — 每週末知識攝取

### 4️⃣ `/wiki-query [主題]` — 決策支援查詢（頻繁使用）

### 5️⃣ `/wiki-lint` — 每月底知識庫巡檢

---

## 🎥 影片筆記 iframe 強制規則（永久）

IF `type: 影片筆記` THEN Step_0.5 必須強制檢查：
1. ✅ video_url 欄位有效
2. ✅ video_id 欄位有效（非佔位符）
3. ✅ 正文有完整 iframe 嵌入

缺一不可，否則返回修正，不得輸出完成報告。

---

## 🔗 Claude.ai 隱私設定確認
- ✅ Location metadata：**已關閉**
- ✅ Help Improve Claude：**已關閉**
- ✅ 帳號層級：**Claude for Work**
