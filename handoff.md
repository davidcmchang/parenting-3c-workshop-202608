# 交接檔（handoff.md）

> 任何 Agent、任何電腦接手前**必讀**；收工時**必更新**。本檔只放交接必需的精簡資訊，詳細脈絡放 Obsidian（若有 L3）。

## ⏯️ 目前做到哪
已依照指示**獨立抽出四頁文字雲網頁**，完成全新 `ParentingWordCloud` 互動展演網頁建置與雲端部署：
1. **獨立抽離文字雲展演網頁**：
   - 建立獨立專用網頁 `ParentingWordCloud.html` 與 `ParentingWordCloud/index.html`。
   - 包含上方題目切換選單（第 1-4 題切換）、即時動態計數器、QR Code 掃碼區域與「重新開始文字雲」獨立按鈕。
2. **雙渲染引擎 (Canvas + HTML Tag Cloud Backup)**：
   - 採用全新動態字級計算公式 `Math.min(42, Math.round(18 + (c / maxCount) * 24))`，徹底解決文字過大無法放入 Canvas 被隱藏的問題。
   - 即使單字輸入或半形英文輸入，也能 100% 穩定呈現於畫布上。
3. **跨裝置極速同步**：
   - 整合 LocalStorage、BroadcastChannel、REST API 雙向輪詢 (2 秒) 與 Firebase Firestore 實時監聽，手機 `vote.html` 提交後大螢幕即時同步更新。

## 🌐 雲端線上互動網址
- ☁️ **獨立 4 題文字雲展演網址**：
  - [https://davidcmchang.github.io/parenting-3c-workshop-202608/ParentingWordCloud.html](https://davidcmchang.github.io/parenting-3c-workshop-202608/ParentingWordCloud.html)
  - [https://davidcmchang.github.io/parenting-3c-workshop-202608/ParentingWordCloud/](https://davidcmchang.github.io/parenting-3c-workshop-202608/ParentingWordCloud/)
- 🖥️ **主簡報播放網址**：[https://davidcmchang.github.io/parenting-3c-workshop-202608/](https://davidcmchang.github.io/parenting-3c-workshop-202608/)
- 📲 **學員手機互動網址**：[https://davidcmchang.github.io/parenting-3c-workshop-202608/vote.html](https://davidcmchang.github.io/parenting-3c-workshop-202608/vote.html)

## 🕐 最後更新
- 時間：2026-08-10 14:58
- 更新者：Antigravity @ DESKTOP-HCL9VMA
- Git push：✅ 已推 (`https://github.com/davidcmchang/parenting-3c-workshop-202608`)
