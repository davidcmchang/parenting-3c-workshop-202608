# 交接檔（handoff.md）

> 任何 Agent、任何電腦接手前**必讀**；收工時**必更新**。本檔只放交接必需的精簡資訊，詳細脈絡放 Obsidian（若有 L3）。

## ⏯️ 目前做到哪
已完全查明並徹底修正「電腦需 Refresh 才呈現，手機無動態」的技術原因：
1. **問題原因（除錯報告）**：
   - 舊程式在 Firestore 查詢時使用了 `limit(120)`，但資料庫先前測試已累積超過 120 筆歷史文檔。當新資料送出時，因預設非時間倒序排列，導致新文檔直接被 `limit(120)` 截斷在外面，`onSnapshot` 根本收不到最新數據！
   - 此前的 localStore 僅存在本機，故電腦刷新頁面時手動讀取本機數據才顯現，而手機與遠端完全收不到。
2. **徹底修正方案**：
   - 移除所有限制截斷障礙，直連 Firestore 即時連線流。
   - 加入 **1.5 秒自動繪圖與 UI 刷新計時器** (`setInterval(renderCurrentCloud, 1500)`)，無論手機或電腦，**完全無需手動按 Refresh，0.5 ~ 1.5 秒內會自動在文字雲大螢幕即時浮現最新回應**！

## 🌐 雲端線上互動網址
- ☁️ **獨立 4 題文字雲展演網址**：
  - 👉 [https://davidcmchang.github.io/parenting-3c-workshop-202608/ParentingWordCloud.html](https://davidcmchang.github.io/parenting-3c-workshop-202608/ParentingWordCloud.html)
- 📲 **學員手機互動網址**：[https://davidcmchang.github.io/parenting-3c-workshop-202608/vote.html](https://davidcmchang.github.io/parenting-3c-workshop-202608/vote.html)
- 🖥️ **主簡報播放網址**：[https://davidcmchang.github.io/parenting-3c-workshop-202608/](https://davidcmchang.github.io/parenting-3c-workshop-202608/)

## 🕐 最後更新
- 時間：2026-08-10 15:27
- 更新者：Antigravity @ DESKTOP-HCL9VMA
- Git push：✅ 已推 (`https://github.com/davidcmchang/parenting-3c-workshop-202608`)
