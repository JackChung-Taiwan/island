# 翊華兒童程式｜創意冒險群島

這是一個可直接部署的互動展示網站，包含 12 座 3D 透視浮空島、課程介紹、實作問答、任務護照、島嶼切換及行動版介面。

## 開啟方式

- 直接用瀏覽器開啟 `index.html`；**不需要 npm、Vite 或其他安裝**。
- 為了避免部分瀏覽器限制，建議使用本機伺服器測試：在本資料夾執行 `python -m http.server 8000`，再開啟 `http://localhost:8000`。
- `index.html`、`style.css`、`app.js` 必須放在相同資料夾。

## 部署至 GitHub Pages

1. 建立新 GitHub repository，例如 `yihwa-islands`。
2. 將三個檔案 `index.html`、`style.css`、`app.js` 上傳到儲存庫根目錄。
3. 在 Settings → Pages → Build and deployment，選擇 Deploy from a branch、`main`、`/(root)`。
4. 存檔後可透過 `https://<帳號>.github.io/yihwa-islands/` 瀏覽。

## 操作

- 拖曳 3D 場景旋轉；滑鼠滾輪或 ＋/－ 縮放；⌂ 返回全景。
- 點擊島嶼或下方導覽列切換介紹；按「實作挑戰」答題。
- 每座島答對即可取得徽章，瀏覽器會使用 localStorage 記住進度。
- 按「任務護照」查看全部徽章；可清除本機進度。
- 「自動導覽」每 4.5 秒切換一座島。
- 支援觸控拖曳與手機版介面。

## 內容維護

島嶼資訊與題庫位於 `app.js` 開頭的 `courses` 陣列；可修改島名、課程說明、學習目標、成品靈感及選擇題。`correct` 為正確選項的索引（0 代表第一個）。

`buildings` 為不同課程島的自繪 3D 物件；使用純 Canvas 2D 的透視投影與低多邊形幾何渲染，**未使用 Three.js、外部圖片或外部 JS 函式庫**，因此可離線開啟、適合 GitHub Pages 靜態部署。

## 內容與權限

- 此為**課程介紹與互動示範作品**。十二座主題島不代表目前均有正式開班，請以翊華官網公告為準。
- 本專案的 3D 場景、程式與版面為本次獨立製作，沒有複製石門國小原始碼、人物、素材或音樂。
- 聯絡方式與師資名稱參考 [翊華兒童程式官網](https://sites.google.com/view/yihwa-coding/index)。
- 目前只有本機進度，沒有帳號系統、線上成績同步或正式證書發放功能。
