# 📈 股票月線 / 季線走勢與乖離追蹤器 (Stock MA & Bias Tracker)

一個輕量、極速、響應式的網頁應用程式，專為台股與美股投資人設計。透過多通道競速 API，自動抓取現價與歷史 K 線數據，計算月線 (20MA) 與季線 (60MA) 乖離率，並支援 iPhone Bark / LINE / Discord 觸價推播通知與 Google 雲端跨裝置同步功能。

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white)
![TailwindCSS](https://img.shields.io/badge/TailwindCSS-38B2AC?style=flat-square&logo=tailwind-css&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![Chart.js](https://img.shields.io/badge/Chart.js-FF6384?style=flat-square&logo=chartdotjs&logoColor=white)

---

## ✨ 核心功能特色

### ⚡ 1. 極速多通道報價與走勢圖
* **多通道併發引擎**：同時透過 FinMind 官方 API 與 Yahoo Finance 代理通道競速，幾秒內即可同時更新所有自選股的最新價格與均線資料。
* **K 線與均線圖表**：內建 Chart.js 畫布，可自由切換看 **月線 (20MA)**、**季線 (60MA)** 或 **雙線同看**。
* **歷史乖離率波動圖**：直觀顯示紅柱（正乖離）與綠柱（負乖離）走勢，方便捕捉高低點拉回或反彈時機。
* **時間區間切換**：支援切換「近 60 日」與「近半年 (完整)」走勢。

### ✏️ 2. 獨立自選股清單管理
* **獨立編輯分頁**：專屬清單管理介面，輕鬆新增、手動修改或刪除股票。
* **支援台股與海外標的**：直接輸入台股代號（例 `2330`、`00631L`），上櫃股票加上 `.TWO`（例 `8299.TWO`）。

### 🎯 3. 乖離率追蹤階梯
* **目標價自動換算**：自訂乖離階梯（如 $\pm5\%, \pm10\%, \pm15\%$），自動計算當前均線對應的加碼與減碼目標價位。
* **狀態警示燈號**：當現價突破或跌破階梯時，呈現閃爍高亮卡片。

### 🔔 4. 彈性觸價推播通知
* **多條件門檻設定**：支援多選「大於等於 ($\ge$)」或「小於等於 ($\le$)」，並可輸入多個數字（例：`5, 10, 20`）。
* **iPhone Bark 推播**：無縫支援免費的 iOS Bark App，自動發送通知至 iPhone 鎖定畫面。
* **Discord / LINE Webhook**：支援自訂 Webhook 網址，輕鬆整合通訊軟體。

### ☁️ 5. Google 帳號與跨裝置同步
* **一鍵 Google 登入**：無需複雜後端，輸入 Email 即可為您建立專屬備份檔。
* **跨裝置同步碼**：一鍵產生 Base64 同步字串，手機與電腦間複製貼上即可瞬間還原設定。

---

## 🚀 快速上手 (Quick Start)

### 本地直接執行
1. 將本專案下載或 Clone 至本地電腦：
   ```bash
   git clone https://github.com/您的帳號/stock-tracker.git
   ```
2. 直接使用瀏覽器打開 `index.html` 即可使用，無需安裝任何 Node.js 套件或啟動伺服器！

---

## 🌐 部署至 GitHub Pages

您可以免費將此專案發布為線上網頁：

1. 將程式碼 Push 至您的 GitHub 儲存庫。
2. 進入儲存庫頁面，點選 **Settings** $\rightarrow$ **Pages**。
3. 在 **Build and deployment** 下方的 **Branch** 選擇 `main` (或 `master`)，目錄選擇 `/root`。
4. 按下 **Save**，等待約 1~2 分鐘即可獲得專屬網址：
   `https://<YOUR-USERNAME>.github.io/<REPOSITORY-NAME>/`

---

## 🛠️ 技術棧 (Tech Stack)

* **Frontend**: HTML5, Vanilla JavaScript (ES6+)
* **Styling**: [Tailwind CSS CDN](https://tailwindcss.com/)
* **Charts**: [Chart.js](https://www.chartjs.org/)
* **Data Sources**: FinMind API / Yahoo Finance API
* **Storage**: Browser LocalStorage & Portable Base64 Codes

---

## 📄 授權條款 (License)

本專案採用 [MIT License](LICENSE) 授權開源，歡迎自由修改與分享。
