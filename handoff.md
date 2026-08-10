# 交接檔（handoff.md）

> 任何 Agent、任何電腦接手前**必讀**；收工時**必更新**。本檔只放交接必需的精簡資訊，詳細脈絡放 Obsidian（若有 L3）。

## ⏯️ 目前做到哪
已依照您的指導精確對照修復全數 10 頁：
1. **Slide 1 純淨照片（去邊框與文字殘影）**：使用 Python PIL 裁切出最純淨的母子沙發照片 (`slide_1_pure_photo.jpg`)，徹底去除了導出的綠線與底部文字。
2. **Slide 2 講員頭像與 Logo 徹底對調**：
   - 校正檔名對應關係，將**張志銘執事大頭像** (`slide_2_speaker.png`) 放置於**左側投影大白框**內。
   - 將 **Towarding Logo** (`slide_2_logo.png`) 放置於**右上角**。
3. **Slide 3 「重新開始文字雲」按鈕更名與真正歸零**：
   - 按鈕名稱修正為 **`🔄 重新開始文字雲`**。
   - 修正歸零邏輯：按下後將現場 Session 計時點更新，畫面**立即歸零顯示 0 筆回應**且**畫布完全空白**；Firebase Firestore 資料則**100% 完整留存**供未來分析使用。
4. **Slide 3-6 題目字體放大比例**：
   - 縮小「開場破冰：文字雲活動」為小副標，將「1. 你的孩子目前多大？ (幾歲／幾年級？)」等主要題目字體**大幅放大至 1.35em (32pt+) 粗體**，確保現場後排家長清晰可見。
5. **Slide 4-6 移除按鈕**：僅保留 Slide 3 之「重新開始文字雲」按鈕。
6. **Slide 7-11 分步 Reveal 動態展演**：完全按照 PPT 格式設定，支援方向鍵逐字/逐區塊動態顯現。

## 🌐 雲端線上互動網址
- 🖥️ **主簡報播放網址**：[https://davidcmchang.github.io/parenting-3c-workshop-202608/](https://davidcmchang.github.io/parenting-3c-workshop-202608/)
- 📲 **學員手機互動網址**：[https://davidcmchang.github.io/parenting-3c-workshop-202608/vote.html](https://davidcmchang.github.io/parenting-3c-workshop-202608/vote.html)

## 🕐 最後更新
- 時間：2026-08-10 14:20
- 更新者：Antigravity @ DESKTOP-HCL9VMA
- Git push：✅ 已推 (`https://github.com/davidcmchang/parenting-3c-workshop-202608`)
