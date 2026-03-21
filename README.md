# PFMS 物業與設施及資產管理系統

> Property & Facility Management System — 基於 3D GIS 的綜合性物業設施資產管理平台

[![Deploy to Netlify](https://www.netlify.com/img/deploy/button.svg)](https://app.netlify.com/start)

---

## 🌟 系統功能

| 模組 | 說明 |
|------|------|
| 系統總覽 | 8 項 KPI 指標儀表板、工單列表、據點狀態監控 |
| 3D GIS | Three.js 即時 3D 場景、圖層樹管理、全域搜尋、三平台切換 |
| 資產管理 | Grid/List 雙視圖、搜尋篩選、掃描入庫、狀態統計 |
| 巡邏檢查 | QR Code 掃描、排程管理、進度追蹤 |
| 維護查修 | Kanban 看板、優先級標示、派工管理 |
| 報表分析 | 盤點報告、成本分析、能源效率、設備可靠性 |

## 🛠 技術棧

- **React 18** — UI 框架
- **Three.js r128** — 3D GIS 渲染引擎
- **Tailwind CSS 2.x** — 響應式設計
- **Babel Standalone** — JSX 即時編譯
- **Pure SVG Icons** — 零圖標庫依賴

---

## 🚀 部署方式

### 方式一：Netlify（推薦，最快上線）

#### 拖曳部署（30 秒完成）

1. 前往 [app.netlify.com](https://app.netlify.com)
2. 登入或註冊帳號（可用 GitHub/Email）
3. 在首頁找到 **"Sites"** → **"Add new site"** → **"Deploy manually"**
4. 將整個 `pfms-system` 資料夾**直接拖曳**到上傳區域
5. 等待 10 秒部署完成
6. 取得網址如：`https://xxxxx.netlify.app`

#### 修改網站名稱

1. 進入 Site settings → Site information → Change site name
2. 改為：`pfms-system` 
3. 網址變為：`https://pfms-system.netlify.app`

#### 綁定自訂域名（選用）

1. Site settings → Domain management → Add custom domain
2. 輸入您的域名（如 `pfms.yourcompany.com`）
3. 按照指示設定 DNS CNAME 記錄
4. Netlify 自動提供免費 SSL 憑證

---

### 方式二：GitHub Pages（免費 + 版本控制）

#### 步驟 1：建立 GitHub Repository

```bash
# 在本機開啟終端機，進入 pfms-system 資料夾
cd pfms-system

# 初始化 Git
git init
git add .
git commit -m "🚀 Initial release: PFMS v1.0"

# 連結到您的 GitHub Repository
# 請先在 GitHub 網站建立新的 Repository（名稱建議：pfms-system）
git remote add origin https://github.com/您的帳號/pfms-system.git
git branch -M main
git push -u origin main
```

#### 步驟 2：啟用 GitHub Pages

1. 前往 GitHub Repository 頁面
2. 點選 **Settings** → 左側選單 **Pages**
3. **Source** 選擇 **GitHub Actions**
4. 系統會自動偵測 `.github/workflows/deploy.yml` 並執行部署
5. 等待 1-2 分鐘，取得網址：`https://您的帳號.github.io/pfms-system`

#### 步驟 3：後續更新

```bash
# 修改檔案後
git add .
git commit -m "✨ 更新功能描述"
git push
# GitHub Actions 會自動重新部署
```

---

### 方式三：Docker 容器化（企業內網）

```bash
# 建立 Docker Image
docker build -t pfms-system .

# 啟動容器
docker run -d -p 80:80 --name pfms pfms-system

# 訪問 http://localhost
```

---

## 📁 檔案結構

```
pfms-system/
├── index.html              # 主程式（單一 HTML，包含所有功能）
├── 404.html                # SPA 路由支援（GitHub Pages）
├── netlify.toml            # Netlify 部署設定
├── _redirects              # Netlify 路由設定
├── .nojekyll               # 停用 GitHub Pages Jekyll
├── .github/
│   └── workflows/
│       └── deploy.yml      # GitHub Actions 自動部署
└── README.md               # 本文件
```

## 📱 瀏覽器支援

- ✅ Chrome 90+
- ✅ Firefox 88+
- ✅ Safari 14+
- ✅ Edge 90+
- ✅ iOS Safari / Android Chrome（行動裝置）

## 📄 License

© 2026 PFMS System. All rights reserved.
