# 零基礎個人投資與理財入門

給沒有股市、基金或財經先備知識的大學生與社會新鮮人。從生活中的錢開始，透過生活比喻、假設試算與基礎題建立理解；不提供個人化投資建議或商品推薦。

## 從哪裡開始

- [公開入口首頁](index.html)
- [八頁教學 HTML 簡報](slides/index.html)
- [完整 Wiki 目錄](wiki/index.md)
- [七份來源登錄](sources/catalog.md)
- [五題練習與可展開解析](exercises/index.html)
- [專案規則](AGENTS.md)
- [內容檢查報告](reports/2026-11-19-content-check.md)
- [發布檢查報告](reports/2026-11-19-release-check.md)

## 五個學習單元

1. [先管好生活中的錢](wiki/01-budget-and-emergency-fund.md)：收支、結餘與備用金。
2. [錢為什麼會變多，也可能變少](wiki/02-inflation-and-compound-interest.md)：購買力、單利與複利。
3. [股票、債券、基金與 ETF 是什麼](wiki/03-stocks-bonds-funds-etfs.md)：所有權、出借及基金包含關係。
4. [如何避免把風險集中在一起](wiki/04-diversification-and-allocation.md)：分散與配置仍可能損失。
5. [建立自己的第一份理財計畫](wiki/05-first-financial-plan.md)：生活、目標、執行與付款前查核。

## 專案架構

```text
zero-basics-finance/
  AGENTS.md
  README.md
  .gitignore
  .nojekyll
  index.html
  sources/catalog.md
  notes/                     七份來源閱讀筆記
  wiki/                      五篇知識條目、目錄與執行日誌
  exercises/                 五份練習 Markdown 與 index.html
  slides/
    outline.md
    source-map.md
    drafts/                  八份核准逐頁稿
    index.html               八頁 HTML，內嵌 CSS、JavaScript 與 SVG
  reports/
    2026-11-19-content-check.md
    2026-11-19-release-check.md
    browser-check.json
    screenshots/             本機驗收畫面
```

## 來源查證原則

來源 ID 固定為 S001–S007，優先使用臺灣官方與公信力機構。每份登錄有網址、機構、日期、可定位段落、適用範圍與使用限制；不知道的發布日不補猜。可讀性與資料缺口另存 notes/。

重要主張先進 Wiki 才能進簡報，不能直接從外部資料加進簡報。用【來源內容】、【教學轉譯】、【假設例子】、【自編練習】及【待確認】辨識不同性質。假設數字不當歷史績效或收益保證。

S004 p25 未附出處的數據停用；S006 p12 百分比算式誤植已隔離，計息定義採 pp11、13，教學數字另行驗算。原始 PDF 與未授權教材不放入公開專案。

## 工作流

1. 先討論受眾、單元與規則。
2. 來源登錄、可讀性與缺口檢查，取得使用者確認。
3. 匯入五篇 Wiki 與練習，同步目錄與日誌。
4. 先做固定八頁大綱及逐頁來源對照，再由使用者明確確認。
5. 撰寫逐頁稿，分開執行字數、詞義、數字及來源檢查；保留問題與修正紀錄。
6. 使用者確認內容報告後，才製作 HTML 與 SVG。
7. 本機檢查通過後交付；上傳 GitHub Pages 之後另作公開網址實測。

新增知識時先更新來源與 Wiki，再重新檢查受影響的大綱、來源表、逐頁稿與 HTML。不能只改成品，使核准稿和網站內容分岔。

## 本機瀏覽

解壓縮後直接開啟根目錄 index.html，再進入簡報；或直接開啟 slides/index.html。簡報的樣式、互動與圖表均內嵌，不需安裝套件、API 金鑰或網路字型。

若電腦有 Python，也可在本專案根目錄執行：

```powershell
python -m http.server 8000 --bind 127.0.0.1
```

再以瀏覽器開啟 `http://127.0.0.1:8000/`。這是僅限本機的預覽，不是公開網址；關閉預覽服務即可停止。

操作：方向鍵左右切頁，空白鍵前進；也可使用下方按鈕。首頁與末頁按鈕有邊界，不會多出第九頁。手機直向採上下排列，依可用高度縮放；短螢幕或高倍率縮放可能使字變小，必要時改橫向或在較大螢幕閱讀。

Markdown 文件保留 `.md` 連結。GitHub Repository 會排版顯示；直接用本機瀏覽器或靜態網站開啟，可能顯示原始 Markdown 或下載，依瀏覽器處理。練習另有 HTML 入口，不依賴 Markdown 渲染。

## GitHub Pages 線上使用

本次**沒有上傳 GitHub，也沒有產生已驗證公開網址**。

將這個資料夾內的完整內容放入預定作為網站根目錄的 GitHub Repository，保留相對目錄及 `.nojekyll`。網站的發布來源必須包含根目錄 index.html；若多包一層資料夾，入口路徑也會多一層。

由使用者設定 GitHub Pages 發布來源後，使用 GitHub 顯示的實際網站網址開啟驗證。不要把 Repository 網址當成 Pages 網址，也不要猜測網址當作已部署成功。靜態網站的服務方式見 [GitHub Pages 官方說明](https://docs.github.com/en/pages/getting-started-with-github-pages/what-is-github-pages)；發布來源見[官方設定文件](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site)。

上傳後須親自檢查：首頁、八頁切換、圖表、來源／Wiki 路徑、練習解析、手機閱讀與公開無需登入；並把實際時間、網址及結果追加發布報告。`.nojekyll` 用來保留純靜態目錄與原始 Markdown 路徑，本專案不依賴 Jekyll 建置。

## 公開與私人資料

`.gitignore` 排除 .env、憑證、私人筆記、上傳原檔及未授權 PDF／Office 教材。公開的 notes/ 是來源閱讀摘要，並非私人學習筆記。reports/screenshots/ 只有本專案教學畫面。

忽略規則不能自動撤回以前已加入版本控制的秘密；上傳前仍要核對實際檔案。此專案沒有模型金鑰、帳號登入、分析追蹤或收集使用者財務資料的功能。

## 驗收界線

本機結構與指定尺寸的 Chrome 檢查已記錄於發布報告；不等於所有裝置、瀏覽器或公開主機皆已驗收。GitHub Pages 公開網址實測保持待辦，等使用者上傳後親自驗證。
