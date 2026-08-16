# camadalobster-source.github.io — 作品集首頁

對外網址：<https://camadalobster-source.github.io/>（GitHub Pages，來源 main/root）。單一 `index.html` ＋ inline CSS，深淺色自適應。

> 這份維護說明原本住在 auto-memory `wip_web_tool_portfolio`，2026-08-16 記憶架構搬移時落檔到 repo 自己身上。

## 兩個門面，每加一個工具要更新兩個地方

GitHub 的 repo 是平鋪的（無法巢狀），所以作品集靠兩個入口撐起來：

1. **對外作品集首頁**＝本 repo 的 `index.html`（就是你現在看到的這個網站）→ 新增工具＝複製一個 `.card` 區塊。
2. **GitHub 個人頁索引**＝Profile README repo `camadalobster-source/camadalobster-source`（本機 `~/dev/projects/camadalobster-source/`）→ 加一行：名稱／demo 連結／一句描述。

每個工具自己的 repo 也要 `gh repo edit <repo> --homepage <pages url>`，把 GitHub 側邊欄的首頁連到 demo。

## 分類法（Henry 定的）

判準＝「**能不能點開用** ＋ **是否從頭開發**」兩者綜合：

- 🛠 **自行開發的 AI 工具**——從頭開發 ＋ 能實際操作。卡片按鈕寫「開啟」，連 demo。
- 💡 **AI 應用案例**——展示用 AI 達成的成果／過程，可以用現成服務、不一定能互動。卡片按鈕寫「查看」，連簡報或說明頁，**用紫色調與工具區區隔**。新案例＝複製 `.cases .card` 區塊。

案例頁放在本 repo 的 `cases/` 底下，用作品集層級的寫法（問題 → 做法 → AI 角色 → 成果），**刻意不含個人資料、實際內容與敏感路徑**（例如 auto-digest 與 second-brain 兩個系統本身是私密的，案例頁只寫方法）。

## 首頁風格（2026-06-23 定稿）

極簡；**不放方法論說明**；**不放原始碼連結**（Henry 覺得對外無價值——repo 仍是 public，只是不從首頁連過去）。漸層底、卡片格線，字標只放「Henry Chen」。

## 排除在作品集外

`tvbs-*`（公司 spec／wireframe）、`test`、`retro`（網站改版討論頁）。

## 開發流程

工具走 OpenSpec spec-driven：`new → proposal/tasks → 審核 → 實作 → archive`。一個工具一個獨立 git repo，推到 `camadalobster-source`；本機才用 `~/dev/projects/web-tools/<工具名>/` 分類。
