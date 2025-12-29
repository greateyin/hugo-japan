# hugo-japan

Tech Insights 科技洞察 - 一個使用 Hugo 建立的多語言科技部落格。

## 🚀 快速開始

### 前置需求

- [Git](https://git-scm.com/downloads)
- [Hugo Extended](https://gohugo.io/installation/) (建議版本 v0.112.0 或更新)

### 解壓縮後立即啟用

1. **下載並解壓縮專案**

   將壓縮檔解壓縮到您想要的目錄：
   ```bash
   unzip hugo-japan.zip -d hugo-japan
   cd hugo-japan
   ```

2. **初始化 Git 子模組 (主題)**

   由於本專案使用 Git Submodule 管理主題，解壓縮後需要初始化：
   ```bash
   git init
   git submodule add https://github.com/themefisher/parsa-hugo.git themes/parsa
   ```

   或者，如果您是從 Git clone 下來的：
   ```bash
   git submodule update --init --recursive
   ```

3. **啟動本地開發伺服器**

   ```bash
   hugo server -D
   ```

   成功啟動後，開啟瀏覽器訪問：http://localhost:1313/

### Windows 使用者快速指令

如果您使用 PowerShell：
```powershell
# 解壓縮
Expand-Archive -Path hugo-japan.zip -DestinationPath .\hugo-japan
cd hugo-japan

# 初始化主題
git init
git submodule add https://github.com/themefisher/parsa-hugo.git themes/parsa

# 啟動伺服器
hugo server -D
```

## 📁 專案結構

```
hugo-japan/
├── archetypes/        # 內容模板
├── assets/            # SCSS、JS 等資源檔
├── content/           # 多語言內容
│   ├── en/           # 英文內容
│   ├── zh-TW/        # 繁體中文內容
│   └── zh-CN/        # 簡體中文內容
├── i18n/              # 多語言翻譯檔
├── layouts/           # 自訂版面配置
├── static/            # 靜態檔案（圖片等）
├── themes/            # Hugo 主題
└── hugo.toml          # Hugo 配置檔
```

## 🌐 支援語言

- English (en)
- 繁體中文 (zh-TW)
- 简体中文 (zh-CN)

## 📝 常用指令

| 指令 | 說明 |
|------|------|
| `hugo server -D` | 啟動開發伺服器（包含草稿） |
| `hugo server` | 啟動開發伺服器（不包含草稿） |
| `hugo` | 建構靜態網站到 `public/` 目錄 |
| `hugo new posts/my-post.md` | 建立新文章 |

## 🔧 疑難排解

### 主題載入失敗

如果看到主題相關錯誤，請確認：
```bash
# 檢查主題目錄是否存在
ls themes/parsa

# 若不存在，重新初始化 submodule
git submodule update --init --recursive
```

### Hugo 版本問題

請使用 **Hugo Extended** 版本（支援 SCSS 編譯）：
```bash
hugo version
# 應顯示 "extended" 字樣，例如：hugo v0.120.0+extended
```

## 📄 授權

本專案使用 [MIT License](LICENSE)。
