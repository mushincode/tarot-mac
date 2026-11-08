# 塔羅素材與原專案授權補查

核查日期：2026-11-08。下文區分原始權利聲明、實際檔案檢查及仍未核實的地方；不是對任何司法管轄區著作權狀態的保證。

## 原參考專案：實際塔羅路徑

核查基準：[原專案 commit 44d185187d1babafff5ba4bf722e60640492ab81](https://github.com/dreamhunter2333/chatgpt-tarot-divination/tree/44d185187d1babafff5ba4bf722e60640492ab81)。

- [根目錄 LICENSE](https://github.com/dreamhunter2333/chatgpt-tarot-divination/blob/44d185187d1babafff5ba4bf722e60640492ab81/LICENSE) 是 MIT，版權聲明為 dreamhunter2333；使用其中受該授權涵蓋的內容須保留授權與版權聲明。不能僅依此推論所有第三方資產、字型及依賴均由原作者授權。
- [塔羅頁](https://github.com/dreamhunter2333/chatgpt-tarot-divination/blob/44d185187d1babafff5ba4bf722e60640492ab81/frontend/src/pages/divination/TarotPage.tsx) 收集問題並呼叫塔羅解讀；[塔羅提示詞](https://github.com/dreamhunter2333/chatgpt-tarot-divination/blob/44d185187d1babafff5ba4bf722e60640492ab81/src/divination/tarot.py) 要求 AI 虛擬洗牌、抽三張及解讀。這條已檢查路徑沒有直接載入 78 張塔羅牌圖或固定牌義資料庫；不能由此斷言儲存庫其他位置完全沒有相關素材。AI 生成回覆並非該 repo 提供一套已審核的固定牌義。
- [前端 CSS](https://github.com/dreamhunter2333/chatgpt-tarot-divination/blob/44d185187d1babafff5ba4bf722e60640492ab81/frontend/src/index.css) 宣告 `Inter, sans-serif`；已查看的 [入口 HTML](https://github.com/dreamhunter2333/chatgpt-tarot-divination/blob/44d185187d1babafff5ba4bf722e60640492ab81/frontend/index.html) 沒有字型載入標籤，程式碼搜尋沒有找到 `@font-face` 或 Google Fonts 引入。這不證明所有部署環境不存在其他字型載入方式；若日後要打包 Inter，須獨立核實所用具體字型版本及授權，不把 repo MIT 等同字型授權。
- repo 尚有應用圖示、示範截圖和依賴套件；這次未逐項追溯它們各自的權利。新產品先前已決定 Flutter 重新實作、原專案作參考，不應自動匯入這些檔案。

## 完整 78 張影像候選：Soimoi

- [Soimoi 牌圖目錄](https://github.com/mixvlad/TarotCards/tree/840b84d012c6b74dc1634fa2d00d1b21f5b28093/tarot/soimoi/full) 的目錄清單顯示 22 張編號大牌（00–21）、Cups、Pents、Swords、Wands 各 01–14 共 56 張，另有 Cover，合計 78 張牌圖加封面。此為檔名與數量核查，未逐張檢視圖像內容、牌義一致性、牌背或解析度是否符合應用。
- [牌組專屬 LICENSE](https://github.com/mixvlad/TarotCards/blob/840b84d012c6b74dc1634fa2d00d1b21f5b28093/tarot/soimoi/LICENSE) 聲明 Mike Koz 2025，目錄牌圖（含縮圖及 GIF）以 CC BY 4.0 授權，並說明生成式影像模型參與製作及其權利因司法管轄區而異。[SOURCES](https://github.com/mixvlad/TarotCards/blob/840b84d012c6b74dc1634fa2d00d1b21f5b28093/SOURCES.md) 記載 78 張及作者資料。CC BY 條款允許商業再散布及改作，但要求適當署名、連結授權與標示修改，亦有限制附加限制等條件；以[授權條款](https://creativecommons.org/licenses/by/4.0/legalcode)為準。
- 限制：授權聲明是發布者對其權利的聲明，不是對所有素材來源或每個地區可主張權利的獨立認證。未核對模型來源、生成素材權利鏈、具體地區法律、每張圖品質或是否符合使用者選定的紫金美術風格；這是候選而不是已獲使用者選用的正式牌組。

## 候選牌義資料集：Oraclume

- [index.json 固定版本](https://github.com/smallcat419/tarot-card-data/blob/b40718b33ea9de3a89dc65fc0e2c9a9a605e409e/index.json)（blob SHA `758ef90ee8a4c39bdb1b0a1172d2d8444aeb72e8`）經 JSON 統計實際有 78 個獨立 ID、78 個不同名稱、22 個 `arcana: Major` 與四花色各 14 張，每張皆有正位及逆位 `meaning`。維護者 [README](https://github.com/smallcat419/tarot-card-data/blob/b40718b33ea9de3a89dc65fc0e2c9a9a605e409e/README.md) 宣稱 CC0 1.0；[CC0 說明](https://creativecommons.org/publicdomain/zero/1.0/) 提供授權／放棄權利的條件。未獨立核實資料創作者對全部內容的權利。
- **實際資料與 README 不一致**：56 張小阿爾克那沒有 `arcana` 欄位，而且財務解釋 `upright.finance` / `reversed.finance` 只有 22 張大阿爾克那有，56 張小阿爾克那均缺少，與 README 的小阿爾克那含 finance 欄位的描述相反。不能直接依 README 的篩選程式和欄位保證建立產品資料。資料為英文；繁體中文翻譯、語義品質及與娛樂定位的適配仍需人工審核。

## 應排除作為傳統牌組的候選

[False Dichotomy 作者 README](https://github.com/ChaoteCruithne/FalseDichotomyTarot/blob/923032442ec6070ad8d8a353cc5debc87e1070dd/README.md) 聲稱 78 張及 CC BY 4.0，但作者明確表示小牌不採傳統數字階序、牌組不使用傳統正逆位，與本應用已定的傳統 78 張及正逆位需求不一致。其 README 另提到第三方 Chaos Times 字型；不能假設該字型隨牌組授權自動可單獨使用。

## 尚未決定

- 使用者已認可原創「星星」牌的視覺方向；未決定首版採自製整套、採用上述第三方牌組或混合素材。原創概念圖只有一張，並非完成的 78 張。
- 無法憑這次研究確認所有原專案二進位圖片／字型及其權利鏈，也無法保證候選資料的原創性、準確性或適合各司法管轄區；採用前固定版本，保存授權、來源、署名與修改紀錄，並由負責人逐項審核。
