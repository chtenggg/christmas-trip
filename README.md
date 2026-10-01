# 我們的聖誕旅程｜GitHub Pages 網頁

本版以「華沙_伊斯坦堡_2026聖誕行程_餐廳更新.xlsx」（2026-10-01）生成。

## 打開網頁

先把 ZIP 解壓縮，再打開 `index.html`。HTML、JavaScript、字型和照片必須放在同一套資料夾裡。

包含每日行程、73 篇景點導覽、餐飲詳情、特色菜、訂位與旅費，以及 TRY／CZK 換成 HKD 的換算頁。新增餐廳名稱保留「（待定）」；營業待確認不代表已訂位。新增店家未有核實照片，沒有拿其他餐廳照片代替。

## 放上 GitHub Pages：建議用 GitHub Desktop

檔案和照片超過 100 個，使用 GitHub Desktop 可以一次加入所有檔案，不需分批在瀏覽器上傳。

1. 從 https://desktop.github.com/ 安裝 GitHub Desktop，登入 GitHub。
2. 選 **File → New Repository**，名稱例如 `christmas-trip`，選好電腦存放位置，按 **Create Repository**。
3. 選 **Repository → Show in Finder**（Windows 為 Show in Explorer）。把 ZIP 解壓後的全部檔案及 `assets` 資料夾，複製到這個 repository 資料夾。`index.html` 必須直接放在根目錄，不要多包一層資料夾。
4. 回 GitHub Desktop，在 Summary 填 `更新旅行網頁`，按 **Commit to main**。
5. 按 **Publish repository**；使用 GitHub Free 時，取消勾選 **Keep this code private**，發布為 Public repository。
6. 在 GitHub 網站打開該 repository，進入 **Settings → Pages**。
7. 在 **Build and deployment → Source** 選 **Deploy from a branch**。
8. Branch 選 **main**，Folder 選 **/ (root)**，按 **Save**。
9. 等部署完成，返回 Pages 頁面按 **Visit site**。通常網址為 `https://你的帳號.github.io/christmas-trip/`，以 GitHub 顯示的實際網址為準。

GitHub Free 的 Public repository 可使用 GitHub Pages；不是 30 天試用。

如果你已經有 repository，先用 GitHub Desktop **Clone repository**，在本機替換網頁檔案，Commit 後按 **Push origin**。原本 Pages 設定可以沿用。

## 網頁檔案

- `index.html`：網頁入口。
- `style.css`、`journey.css`：畫面樣式。
- `app.js`：導覽和匯率換算功能。
- `data.js`、`data.json`：由最新 Excel 擷取的內容。
- `assets/`：實拍照片及繁體中文字型。
- `旅行行程.xlsx`：最新 Excel，網頁內也可下載。
- `.nojekyll`：供 GitHub Pages 直接提供靜態檔案，不必修改。

所有連結採相對路徑與 `#` 導覽，可以放在 GitHub Pages 的 repository 子路徑。不需要執行 npm 或額外建置。

## 港幣換算

土耳其里拉為 TRY，捷克克朗為 CZK；此頁不會因此增加捷克行程。

首次顯示 2026-09-30 ECB 參考值：EUR/HKD 8.9095、EUR/TRY 55.6596、EUR/CZK 24.440。交叉計算為 `外幣金額 ×（HKD 每 EUR ÷ 外幣每 EUR）`。

按「更新參考匯率」會向 Frankfurter 的 ECB 端點取得最新可用日期。這是每日參考匯率，並非即時銀行或信用卡成交價。連線失敗會清楚提示，保留原數值；也可自行輸入實際換到的匯率。沒有計算信用卡或換匯手續費。

來源：

- https://www.ecb.europa.eu/stats/policy_and_exchange_rates/euro_reference_exchange_rates/html/index.en.html
- https://frankfurter.dev/
- https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site
- https://docs.github.com/en/desktop/adding-and-cloning-repositories/adding-a-repository-from-your-local-computer-to-github-desktop

## 下一次改行程

網頁已固定採本次最新 Excel 內容，瀏覽器不會自動讀取後來修改的 Excel。修改行程後，請重新產生 `data.js`／`data.json` 和相關照片，與更新後的 Excel 一起替換，再 Commit 和 Push。
