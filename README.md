# 貓家日子住宿金額計算機

這是一個可直接部署至 GitHub Pages 的單頁住宿金額計算機，不需要安裝任何套件。

## 已包含的計價規則

- 小貓房：每晚 NT$850
- 探險家庭房：每晚 NT$1,300
- 第 2 隻貓起：每隻每晚加收 NT$200
- 超過 15:00 退宿：加收當次單晚房價的 50%
- 15:00 準時或以前退宿：不加收安親費
- 住宿晚數以入住日與退宿日的日期差計算

## 上傳到 GitHub Pages

1. 在 GitHub 建立一個新的 repository。
2. 將 `index.html` 上傳到 repository 的根目錄。
3. 進入 repository 的 **Settings → Pages**。
4. 在 **Build and deployment** 選擇 **Deploy from a branch**。
5. Branch 選擇 `main`，資料夾選擇 `/ (root)`，再按 **Save**。
6. 等待 GitHub 完成部署，Pages 頁面會顯示可公開瀏覽的網址。

## 修改價格

用文字編輯器打開 `index.html`，搜尋以下設定即可調整：

```js
small: { name: "小貓房", baseRate: 850 },
family: { name: "探險家庭房", baseRate: 1300 },
const EXTRA_CAT_RATE = 200;
const DAYCARE_RATE = 0.5;
```

價格調整後，重新把 `index.html` 上傳並覆蓋原檔案即可。
