# 網站維護筆記(內部用)

README 留給對司機的更新公告;部署與維護資訊放這裡。

## 部署(GitHub Pages)

- Settings → Pages → Source: `Deploy from a branch`,Branch: `main` `/ (root)`
- 網址:https://s878787-code.github.io/line-trip_web/
- push 到 main 後 Pages 自動重新部署(約 1–2 分鐘);若 deploy 偶發 `try again later`,推個空 commit 重跑即可

## 檔案

| 檔案 | 說明 |
|---|---|
| `index.html` | 一頁式官網(深色琥珀、實心編輯式設計) |
| `assets/app-icon.png` | App 正式 icon(favicon 各尺寸由它縮出) |
| `assets/QRCODE.png` | 官方 LINE 加好友 QR |
| `assets/og.png` / `og.html` | 社群分享縮圖(1200×630)與其原始碼 |
| `assets/logo.svg`・`favicon*.png`・`icon-*.png`・`apple-touch-icon.png` | 品牌與圖示 |

## 重產 OG 分享圖

改 `assets/og.html` 後:

```powershell
& "C:\Program Files\Google\Chrome\Application\chrome.exe" --headless=new --window-size=1200,630 --virtual-time-budget=6000 --screenshot="assets\og.png" "file:///C:/Github/line-trip_web/assets/og.html"
```

## 本機預覽

```powershell
python -m http.server 8080
# http://localhost:8080
```

## ⚠️ 個資紅線(曾出過事)

- 這是 **public repo**:任何截圖/影片/檔案 push 前先確認**沒有**授權金鑰、住家地址、真實客戶派單地址、LINE 群組畫面(群名/暱稱/電話)。
- 操作影片一律用 **open 測試機版的「模擬派單」**錄製,不用正式機真實資料。
- 已發生過一次外洩並以 force push 清史;當時截圖中的授權金鑰應視為已曝光,須重新產生。

## 待補素材

- App 實機操作影片(10–20 秒,直式,模擬派單錄製)→ 丟 `assets/` 後嵌回「操作流程」區
