# TripRadar 車趟輔助 — 官方網站

職業司機的 AI 接單助手 **TripRadar(車趟輔助)** 的官方一頁式行銷網站。純靜態、無建置流程,直接以 GitHub Pages 部署。

> App 原始碼在 private repo `s878787-code/line-trip`,本 repo 只放公開網站。

## 內容

| 檔案 | 說明 |
|---|---|
| `index.html` | 完整一頁式網站(深色雷達青主題、創始會員定價、FAQ、購買/聯絡) |
| `assets/QRCODE.png` | 官方 LINE 加好友 QR |
| `assets/og.png` | 社群分享縮圖(Open Graph,1200×630) |
| `assets/og.html` | OG 圖的原始碼(改完用 Chrome headless 重截即可) |
| `assets/logo.svg` | 品牌 Logo(橫式) |
| `assets/favicon.svg`・`favicon-32.png`・`apple-touch-icon.png`・`icon-512.png` | 網站圖示 |

## 部署(GitHub Pages)

1. **Settings → Pages**
2. **Source**:`Deploy from a branch`
3. **Branch**:`main` `/ (root)` → **Save**
4. 網址:**https://s878787-code.github.io/line-trip_web/**

推新 commit 後 Pages 會自動重新部署(約 1–2 分鐘)。

## 本機預覽

```bash
python -m http.server 8080
# 開 http://localhost:8080
```

## 重新產生 OG 分享圖

改 `assets/og.html` 後:

```bash
chrome --headless=new --window-size=1200,630 --virtual-time-budget=6000 \
  --screenshot=assets/og.png "file:///<絕對路徑>/assets/og.html"
```

## 待補

- App 真實操作影片(10–20 秒)與 4 張截圖(目前為佔位)
- 隱私權政策 / 服務條款 / 退款政策等連結頁

---

聯絡 / 購買:LINE **@493watvi**
獨立開發之輔助工具,與 LINE 官方無隸屬、合作或背書關係。
