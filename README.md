# 個人行銷／品牌網頁｜開工指令與製作經驗

原頁（TAVA v2，2026-10-15 更新）：https://www.tava-ai.com/chat/eo63j7e7tu/personal-brand-playbook-v2.html
舊版原頁（v1）：https://www.tava-ai.com/chat/zzphp46s9b/tava-brand-web-playbook.html

`index.html` 為 v2 原頁 1:1 拷貝（v2 原頁頁尾的「大樹教練」連結本來就是 https://www.bymyway.com/，沒有再做任何修改）。

v2 比 v1 新增：公益足跡區塊、每個區塊都要配圖、不要用「捲動才出現」的效果。

2026-10-16 教練要求：公益足跡的足跡時間軸改成上下時間線（不左右滑動）。`index.html` 的規格文字已照此改，與 TAVA 原頁文字不同。

網址：https://coach1973.github.io/tava-brand-web-playbook/

2026-10-29 教練指定：出圖指令併進開工指令。完整版加「配圖規則」、精簡版加一行、交付前檢查加一項：AI 不得自己出圖，需要圖的位置只寫出圖清單，由小龍蝦用 LK888 出（原因：有 AI 把「做出來」當成自己畫，一次扣很多點）。獨立的「出圖指令表一鍵注入」頁（ai-go/biz-web-inject.html）保留，給不走這份開工指令的單獨情境使用。

2026-10-25 教練指定：固定頁尾由三個連結增加為四個（新增「顧問師天團・人才軍火庫」→ https://event.bymyway.com/curated/skyteam/），因此 index.html 的製作指令、第 10 項固定頁尾、驗收清單、頁面自己的頁尾四處已同步修改，與 v2 原頁不再逐字相同。

2026-10-30 教練指定：出圖位置標編號、圖出好後直接換進已上架網頁。開工指令（完整版、精簡版）、製作經驗、交付前檢查四處加規則：要等出圖的位置一律寫成 `<img data-slot="IMG-001" src="暫時圖" alt="…">`，編號同出圖清單 ID，不加「待換圖」字卡，AI 不用等圖傳回來。流程：TAVA 做網頁＋出圖清單 → 教練把 ZIP 上傳策展中心 → 小龍蝦用 LK888 出圖 → 教練對 Claude Code 說「<短網址> 已上架，換圖」→ 工具 `workspace/scripts/swap_slot_images.py <短網址>` 照編號把圖壓成 webp 內嵌、commit、push（線上即時生效）。獨立的「生圖一鍵注入」頁（ai-go/lk888-inject.html）保留給單純要 AI 出圖的情境，做個人品牌網頁一律走這份開工指令。
