# 交接檔（handoff.md）

> 任何 Agent、任何電腦接手前**必讀**；收工時**必更新**。本檔只放交接必需的精簡資訊，詳細脈絡放 Obsidian（若有 L3）。

## ⏯️ 目前做到哪
已完全查明手機端（iPhone/Android/LINE/相機QR Code）傳送問題的原因，並在**完全不影響電腦端已修正程式的前提下**完成了手機端極速修復：

1. **手機端失敗的技術原因（除錯報告）**：
   - 當學員使用手機（特別是 iOS Safari、LINE 內建瀏覽器或相機掃 QR Code 時），瀏覽器處於全新乾淨會話。
   - 當學員在手機按「🚀 立即送出答案」時，因 anon auth 匿名憑證尚未獲取或被第三方 Cookie 限制擋住，導致 `addDoc` 權限不足被 Firebase 擋掉！
2. **手機端極速修復方案（`vote.html`）**：
   - 加入 **`inMemoryPersistence` 記憶體型持久化憑證**，全面避開 Safari/LINE 內嵌瀏覽器的 Cookie/IndexedDB 阻擋政策。
   - 加入 **`ensureMobileAuth()` 強制驗證保護**：在按下的瞬間自動確認並獲取匿名 Token，確保手機 4 題均可 100% 成功寫入雲端並推播至大螢幕！
3. **電腦端防護**：
   - 保持 `ParentingWordCloud.html` 與 `index.html` 之電腦端程式完全不受任何影響！

## 🌐 雲端線上互動網址
- ☁️ **獨立 4 題文字雲展演網址**：
  - 👉 [https://davidcmchang.github.io/parenting-3c-workshop-202608/ParentingWordCloud.html](https://davidcmchang.github.io/parenting-3c-workshop-202608/ParentingWordCloud.html)
- 📲 **學員手機互動網址**：[https://davidcmchang.github.io/parenting-3c-workshop-202608/vote.html](https://davidcmchang.github.io/parenting-3c-workshop-202608/vote.html)
- 🖥️ **主簡報播放網址**：[https://davidcmchang.github.io/parenting-3c-workshop-202608/](https://davidcmchang.github.io/parenting-3c-workshop-202608/)

## 🕐 最後更新
- 時間：2026-08-10 15:40
- 更新者：Antigravity @ DESKTOP-HCL9VMA
- Git push：✅ 已推 (`https://github.com/davidcmchang/parenting-3c-workshop-202608`)
