# 待辦清單 Web App

這是一個在 GitHub Copilot 實戰工作坊中完成的待辦清單 Web App。專案以純前端技術實作，讓使用者可以新增、完成、刪除與篩選待辦事項，並在瀏覽器中保存資料與主題偏好。

## 線上展示

[前往線上展示](https://<你的帳號>.github.io/<你的repo名稱>/)

> 請將上方網址中的 `<你的帳號>` 與 `<你的repo名稱>` 替換成實際的 GitHub Pages 資訊。

## 功能

- 新增待辦事項，空白內容不會被加入清單。
- 勾選待辦事項後標記為已完成，文字會顯示刪除線並淡化。
- 刪除單筆待辦事項。
- 清除所有已完成的待辦事項。
- 顯示整體未完成待辦事項數量，數字不受目前篩選條件影響。
- 清單為空時顯示提示文字。
- 支援「全部」、「未完成」、「已完成」三種篩選模式。
- 篩選結果為空時顯示對應提示，讓使用者知道項目是被篩選掉而不是被刪除。
- 支援淺色與深色模式手動切換。
- 深色模式按鈕會顯示對應的圖示與文字。
- 記住使用者的深色模式選擇，重新整理後仍會維持。
- 使用者尚未手動選擇時，會跟隨作業系統的深淺色設定。
- 待辦資料保存於 `localStorage`，重新整理頁面後仍會保留。
- 版面支援手機螢幕，並採用置中卡片式設計。

## 技術

- 使用純 HTML、CSS 與原生 JavaScript。
- 不使用任何前端框架或第三方套件。
- 不引用外部 CDN，可直接離線開啟。
- 使用 CSS 變數管理介面顏色，並支援淺色與深色主題。
- 使用瀏覽器 `localStorage` 保存待辦資料與主題偏好。
- 主要檔案為根目錄的 `index.html`、`styles.css` 與 `app.js`。

## 開發方式

- 使用 GitHub Copilot Agent Mode，透過自然語言需求建立待辦清單的頁面結構、樣式與互動功能。
- 使用 MCP 連接 Microsoft Learn 文件工具，查詢 `prefers-color-scheme` 與深色模式色彩對比等官方建議。
- 使用 MCP 連接 GitHub 工具，讀取 repository issue、整理 issue 資訊，並建立修復用的分支與 Pull Request。
- 使用 `.github/prompts` 中的 `fix-issue.prompt.md` 定義 agentic workflow，依序執行讀取 issue、等待確認、建立分支、修改、驗證、提交推送與建立 PR。
- 透過瀏覽器開啟 `index.html`，實際驗證待辦操作、主題切換、篩選與資料保存行為。

## 我學到什麼

- 如何用原生 JavaScript 管理 DOM、事件與待辦事項狀態。
- 如何使用 `localStorage` 保存瀏覽器端資料，讓頁面重新整理後仍能恢復狀態。
- 如何使用 CSS 變數與 `prefers-color-scheme` 實作可切換且能跟隨系統設定的主題。
- 如何使用 GitHub Copilot Agent Mode、MCP 與提示檔，將需求拆成可驗證的開發流程。
- 如何從 GitHub issue 理解使用者體驗問題，提出最小修改並透過 Pull Request 完成修復。
