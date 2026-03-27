# AIIU Lab Website (v2)

這是 **AIIU Lab** 的官方網站。本網站採用純 Gemini 開發，旨在提供一個輕量、專業且易於維護的學術展示平台。

## 🌐 網站網址
[https://aiiu-lab.github.io/](https://aiiu-lab.github.io/)

---

## 📂 分支管理策略 (Branching Strategy)

為了確保網站維護的安全性與歷史紀錄的完整性，我們採用以下分支結構：

* **`main` (預設分支)**：當前正式上線的網站程式碼。所有更新（論文、成員、新聞）請直接對此分支進行修改並推播 (Push)。
* **`legacy-v1` (封存分支)**：保留 2026 年改版前的舊版網站 (2019) 檔案。僅供歷史參考，除非需要找回舊資料，否則請勿更動。

---

## 🚀 如何更新網站內容

維護者只需要具備和 Gemini 溝通的能力，以及基礎的 HTML/CSS 知識即可進行更新。

### 1. 更新精選研究 (Latest Works) & 論文 (Publications)
* 檔案位置：`index.html`
* **近期消息**：找到 `<section id="news">`，複製 `news-item` 依序增加近期消息。
* **精選研究**：找到 `<section id="latest-works">`，複製一個 `.work-card` 區塊並填入新的研究標題、摘要與圖片路徑。
* **論文列表**：找到 `<section id="publications">`，在 `.pub-list` 中新增一個 `<li>` 項目。請確保使用 `.pub-title` 和 `.pub-venue` 標籤以維持格式統一。

### 2. 更新成員資訊 (Members & PI)
* 檔案位置：`members.html`
* **新增成員**：在 `.member-list` 下複製一個 `<li>` 項目。
    * 頭貼請放至 `images/` 資料夾（此處可未來自由新增定義）。
    * 在 `.member-links` 中可以更新個人網站、Email 或 LinkedIn 連結。

### 3. 更新校友名單 (Alumni)
* 檔案位置：`members.html`
* 找到 `<section class="alumni-section">`。
* 校友名單採用 `grid` 佈局，請依序填入：`姓名(職位)`、`待的時間`、`畢業去向`。

### 4. 更新生活相簿 (Album)
* 檔案位置：`index.html`
* 將新照片放入 `images/`，並在 `.album-grid` 中新增一個 `.album-item`。
* **重要**：請在 `data-description` 屬性中輸入該照片的文字描述，這會在滑鼠懸停時顯示。

---

## 🛠️ 技術規格
* **架構**：純 HTML5, CSS3 (Flexbox & Grid 佈局)。
* **字體**：使用 Google Fonts (Lora 用於標題，Noto Sans 用於正文)。
* **部署**：透過 GitHub Pages 自動部署。只要推播至 `main` 分支，網站會在 1 分鐘內自動更新。

---

## 📸 圖片規範
為了保持頁面加載速度，請在更新圖片前注意：
* **成員頭貼**：建議裁切為正方形，解析度不超過 400x400 px。
* **研究縮圖**：建議寬度 800px 左右，格式建議使用 `.jpg` 或 `.webp`。
* **檔案路徑**：所有圖片請統一存放於 `images/` 資料夾。

---

## ✍️ 維護者
本網站目前由 **[Pin-Yen Chiu](https://itsnickchiu.github.io/)** 維護。
如果有任何技術問題或需要大規模改版，請聯繫 `[nickchiu@citi.sinica.edu.tw]`。