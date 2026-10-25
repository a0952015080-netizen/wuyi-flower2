# 🌸 WUYI 梧藝花藝｜線上花束預訂與 LINE 自動代入系統

專為客人手機瀏覽體驗打造的花束線上預訂頁面。客人填寫與選取款式後，點擊一鍵按鈕將**自動喚醒 LINE App**，並把整理好的訂單文字自動填入聊天室輸入框，由客人直接發送給官方客服！

---

## 🌟 核心特色

1. **同步櫃檯結帳規格邏輯**：
   - 9 款精選花束：精緻款、透包、造型甜筒（S/M/L）、時髦條紋（S/M/L）、復古點點。
   - 專用紙材：甜筒支援加購立挺硬紙（+$50）。
   - 色系混搭：最多可複選 3 種色系，並支援自訂填寫（如：奶茶色、香檳色）。
   - 內襯紙升級（+$100）：選「網格」支援複選 1 色底襯，或自訂襯紙名稱。
   - 配件與蛋糕加購：花束提袋（$40）、保冰袋（$100）、漢堡盒蛋糕（$680/$700/$720）、質感餐具、蠟燭與派對道具（$45/$55/$89/$99 複選累加）。
2. **手機響應式設計 (Mobile Friendly)**：
   - 採用純 HTML5 + CSS3 + 原生 JavaScript，無需安裝 npm 套件或後端伺服器。
   - 浮動底部快速結帳欄，清楚顯示即時試算總額。
3. **LINE 深度整合機制**：
   - 使用 LINE 官方 URI Scheme：`https://line.me/R/oaMessage/{LINE_ID}/?{ENCODED_MESSAGE}`
   - 自動將整理好的品項、規格、加購、總額、取貨時間、訂購人電話複製到剪貼簿，並喚起 LINE 自動填入。
   - 設有完成彈窗與手動複製備援，確保在任何手機瀏覽器（Safari、Chrome、FB/IG 內建瀏覽器）皆可 100% 順暢送單。

---

## 🚀 如何上傳到 GitHub 並開啟網頁連結（GitHub Pages）

### 方法一：使用 GitHub 網頁直接上傳（最簡單）

1. 登入 [GitHub](https://github.com/)，點選右上角 **「+」** ➔ **「New repository」**。
2. Repository name 輸入例如：`wuyi-flower`，設定為 **Public**，點擊 **Create repository**。
3. 在新建立的專案頁面中，點擊 **「uploading an existing file」**。
4. 將本專案資料夾 `WUYI_花束LINE訂購` 內的所有檔案：
   - `index.html`
   - `README.md`
   - `images/` 資料夾（包含花束照片）
   直接拖曳到 GitHub 視窗中，點擊下方 **Commit changes**。
5. 點擊專案上方的 **Settings** ➔ 左側選單選擇 **Pages**。
6. 在 **Branch** 處選擇 `main`（或 `master`），資料夾保持 `/ (root)`，點擊 **Save**。
7. 等待約 1~2 分鐘，上方會出現專屬網址：
   `https://<你的GitHub帳號>.github.io/wuyi-flower/`
   👉 這就是可以直接傳給客人點擊的訂購連結！

---

### 方法二：使用 Git 指令終端機推送

```bash
cd "/Users/Leon/Desktop/WUYI_花束LINE訂購"
git init
git add .
git commit -m "feat: WUYI 線上花束預訂系統"
git branch -M main
git remote add origin https://github.com/<你的帳號>/wuyi-flower.git
git push -u origin main
```
推送完成後，同樣至 Repository Settings ➔ Pages 開啟即可。

---

## ⚙️ 客製化設定

若日後需更換官方 LINE 帳號，直接開啟 `index.html`：
```javascript
const LINE_OA_ID = "@230fpemy"; // 修改為您的官方 LINE ID
```
門市取貨地址與公休日亦可在 HTML 頂部資訊區塊調整。
