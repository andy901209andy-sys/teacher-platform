# 史迪克教學資源網

一個使用 HTML、CSS、JavaScript 製作的響應式教師教學資源網站，可免費部署到 GitHub Pages。

## 網站頁面

- `index.html`：首頁與隨機分組器
- `resources/index.html`：教學資源分類與 Google Drive 連結指引
- `tools/index.html`：隨機抽選器、離堂小反思工具
- `table-tennis/index.html`：桌球教學專區
- `about.html`：關於本站
- `assets/css/style.css`：全站共用樣式
- `assets/js/main.js`：導覽列、分組器與互動工具程式

## 部署到 GitHub Pages

1. 登入 https://github.com/ ，建立新的 **Public** repository，例如 `stick-teaching-site`。
2. 將本資料夾內的所有檔案與資料夾上傳到 repository 根目錄。請確認 `index.html` 位於根目錄，而不是再多一層資料夾。
3. 在 repository 開啟 **Settings → Pages**。
4. 在 **Build and deployment** 選擇 **Deploy from a branch**。
5. Branch 選 `main`，資料夾選 `/(root)`，按 **Save**。
6. 等待 GitHub Pages 完成部署。網址通常會是 `https://你的GitHub帳號.github.io/儲存庫名稱/`。
7. 開啟網址，測試首頁、導覽、分組器與其他頁面。若尚未出現，稍等幾分鐘並檢查 Actions 頁面的部署狀態。

## 如何上傳檔案

### 用 GitHub 網頁上傳（不需要安裝程式）

1. 進入 repository。
2. 點 **Add file → Upload files**。
3. 將 ZIP 解壓縮後的檔案與資料夾拖曳上傳（不要只上傳 ZIP）。
4. 在 Commit changes 區輸入訊息，例如 `Add first version of teaching website`，然後提交。

### 用 Git 指令（選用）

```bash
git clone https://github.com/你的帳號/你的儲存庫.git
# 將本網站檔案複製進該資料夾
git add .
git commit -m "Add teaching resource website"
git push
```

## 加入 Google Drive 教學資源

1. 在 Google Drive 選取檔案並點「共用」。
2. 依檔案性質設定分享權限。
3. 複製分享網址。
4. 編輯 `resources/index.html`，找到「新增資源連結」，將其改為實際的 `<a href="你的Google Drive網址">檔案名稱 →</a>`。

公開網站上的網址可能被任何人看到。請勿將學生姓名、成績、個人聯絡資訊或未經同意的照片與影片設為公開。

## 自訂網站

- 網站名稱與導覽：搜尋 HTML 裡的「史迪克教學資源網」。
- 色彩、字體、卡片：修改 `assets/css/style.css` 最上方的 CSS 變數。
- 新增工具：在 `tools/` 建立新資料夾，新增 HTML 頁面，引用 `../assets/css/style.css`；需要共用互動程式時可新增 JS 檔案。
- 所有內部連結目前使用相對路徑，適合 GitHub Pages 的「專案網站」網址格式。

## 重要限制

- GitHub Pages 是靜態網站託管；這一版不含登入、資料庫或雲端儲存。
- 本版互動工具只在瀏覽器中運作，不會將輸入資料傳送到伺服器。
- 若未來要儲存學生資料，請先設計權限、隱私與資料保護機制，再考慮串接 Apps Script。
