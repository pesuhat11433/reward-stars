# 集點寶貝 · assets 圖檔說明

把你生成的 PNG 圖檔放進對應的資料夾，再在 `manifest.json` 列出檔名，App 啟動時會自動載入。

## 資料夾分類

- `stickers/` — 集點章貼紙（每完成一次表現要蓋的小圖案）
- `avatars/` — 小朋友頭像
- `trophies/` — 沒拍寶物照時用的預設 icon
- `illustrations/` — 招牌角色、歡迎插畫、空狀態插畫、LOGO

## 規格建議

| 用途 | 尺寸 | 格式 | 背景 |
|---|---|---|---|
| stickers / avatars / trophies | 256 × 256 | PNG | 透明 |
| illustrations/character (揮手角色) | 512 × 512 | PNG | 透明 |
| illustrations/welcome、empty | 400 × 400 | PNG | 透明 |
| illustrations/logo | 256 × 256 | PNG | 透明 |
| 每張壓縮後 | < 200KB | | |

## 加新圖步驟

1. 把圖檔丟進對應的子資料夾，檔名可任意（建議 `01.png`、`02.png` 連續編號）
2. 編輯 `manifest.json`，把檔名加進對應的陣列裡
3. 重新整理 App 就會看到新圖

## 範例

```json
{
  "stickers": [
    "stickers/star.png",
    "stickers/heart.png",
    "stickers/unicorn.png"
  ],
  "illustrations": {
    "character": "illustrations/my-mascot.png"
  }
}
```

## 不想用部署資料夾也可以

打開 App 右上角「🖼️ 我的圖庫」按鈕，可以直接在 App 裡上傳圖檔（存在瀏覽器本地）。
這兩種方式可以混用：部署資料夾是大家共用的預設圖，App 內上傳的是個人裝置專屬的圖。
