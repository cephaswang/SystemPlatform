# AVEVA™ System Platform 90 天學習企劃案

> 依據上傳教材《AVEVA™ System Platform 入門教學》延伸規劃，並考量學習者已具備 PLC（Mitsubishi FX5U、Delta AS、Siemens S7）、SCADA/HMI（FUXA、Node-RED、ScadaBR）、Modbus TCP、OPC UA 等工業自動化背景，規劃一套**從入門到實戰部署**的完整學習路徑。

---

## 企劃目標

| 項目 | 內容 |
|---|---|
| **總時長** | 90 天（約 13 週） |
| **每日投入** | 建議 1.5–2.5 小時（平日），週末可安排 3–4 小時整合練習 |
| **先備知識** | 已具備 PLC 邏輯、SCADA 基礎、Modbus/OPC UA 通訊概念 |
| **最終產出** | 一套可實際運行的 Galaxy 專案，涵蓋 I/O 擷取、圖形化 HMI、警報、歷史記錄、報表與腳本邏輯 |
| **建議環境** | AVEVA System Platform 試用版（Trial）+ Application Server + InTouch + Historian（單機安裝即可） |

---

## 課程總覽（四大階段）

| 階段 | 天數 | 主題 | 對應教材章節 |
|---|---|---|---|
| **Phase 1：基礎建置** | Day 1–20 | 架構認識、環境安裝、核心術語 | 一、二 |
| **Phase 2：物件與圖形開發** | Day 21–45 | ArchestrA 物件導向、Galaxy 開發、InTouch 圖形 | 二、三 |
| **Phase 3：服務鏈深化** | Day 46–70 | 警報、歷史記錄、製程控制、腳本、報表 | 三 |
| **Phase 4：整合實戰與部署** | Day 71–90 | 通訊驅動整合、效能優化、正式部署、期末專案 | 全部整合 |

---

## Phase 1：基礎建置（Day 1–20）
**目標：理解三層架構，完成安裝，熟悉 Galaxy 開發環境**

### Week 1（Day 1–7）：架構與環境
- Day 1–2：複習教材一、二章，繪製「資料來源 → 平台核心 → 監督式客戶端」架構圖，並對照自己熟悉的 FUXA/Node-RED 架構做比較筆記
- Day 3：了解 AVEVA Application Server、Historian、Communication Drivers 三大核心元件的分工
- Day 4：申請並下載 AVEVA System Platform 試用版
- Day 5–6：安裝 Application Server + Bootstrap，建立第一個 Galaxy Repository
- Day 7：週末整合 — 撰寫「Bootstrap → IDE → Galaxy → Galaxy Repository」流程筆記，並用自己的話錄一段口頭講解（測試理解程度）

### Week 2（Day 8–14）：System Platform IDE 入門
- Day 8：開啟 IDE，建立第一個 Galaxy 專案，認識 Model / Deployment / Graphic Toolbox 三個視圖
- Day 9：了解 Template 與 Instance 的物件導向概念（對比 PLC 中 Function Block 的思維）
- Day 10：建立第一個簡單物件（如 UserDefined 物件）並部署到本機 Platform
- Day 11：認識 WinPlatform、AppEngine 的角色與部署關係
- Day 12：了解 Galaxy 的版本控制、Check In/Check Out 機制
- Day 13：練習部署（Deploy）與復原（Undeploy）流程
- Day 14：週末整合 — 建立一份「IDE 操作速查表」

### Week 3（Day 15–20）：通訊與 I/O 基礎
- Day 15：認識 DAServer / OI Server 架構，理解與既有 Modbus TCP 知識的對應關係
- Day 16：安裝並設定 Modbus TCP 通訊驅動（因已熟悉 Modbus，可加速學習）
- Day 17：建立 DDESuiteLinkClient 或 OPC UA Client 物件，串接一台既有 PLC（可用 Mitsubishi FX5U 或 Delta AS 測試）
- Day 18：建立 I/O Tags，驗證資料是否正確擷取
- Day 19：練習 OPC UA 連線設定，比較與 Modbus TCP 的差異
- Day 20：**Phase 1 檢核** — 完成「PLC → AVEVA I/O Tag」端對端資料擷取小專案，撰寫檢核報告

---

## Phase 2：物件與圖形開發（Day 21–45）
**目標：熟練 ArchestrA 物件導向設計與 InTouch 圖形化界面**

### Week 4（Day 21–27）：ArchestrA 物件導向進階
- Day 21–22：深入理解 Template 繼承（Inheritance）與多層繼承設計
- Day 23：學習 UDA（User Defined Attribute）與屬性參考（Attribute Reference）
- Day 24：學習 Extension（擴充功能）的概念與應用
- Day 25：設計一組符合「單一資料來源、多重應用」理念的設備範本（如馬達範本、水閥範本）
- Day 26：練習範本批次實例化（Instance）多台相同設備
- Day 27：週末整合 — 建立一套可重複使用的設備物件庫

### Week 5（Day 28–34）：InTouch for System Platform 入門
- Day 28：認識 InTouch WindowMaker / WindowViewer 架構
- Day 29：建立第一個 InTouch Application 並與 Galaxy 整合
- Day 30：學習 Symbol、Wizard、ArchestrA Graphic 的差異與使用時機
- Day 31：繪製第一個製程流程圖（P&ID 風格）並綁定物件屬性
- Day 32：學習動畫連結（Animation Links）：顏色變化、數值顯示、可視性控制
- Day 33：學習觸控/按鈕互動設計（Touch Pushbuttons、Value Display）
- Day 34：週末整合 — 完成一頁完整的 HMI 監控畫面（含至少 5 個動態元件）

### Week 6（Day 35–40）：圖形進階與導覽設計
- Day 35：學習多視窗導覽（Window Navigation）與選單設計
- Day 36：學習全域樣式（Style Library）與命名規範，建立一致的視覺設計系統
- Day 37：學習 ArchestrA Symbol 的參數化設計（可重複使用元件）
- Day 38：練習趨勢圖（Trend）元件嵌入畫面
- Day 39：練習警報視窗（Alarm Viewer）嵌入畫面
- Day 40：週末整合 — 建立包含導覽選單、流程圖、趨勢、警報視窗的完整 HMI Demo

### Week 7（Day 41–45）：中期專案演練
- Day 41–43：以自己的農業自動化背景為題（如 RTK 灌溉站監控），設計一套簡易 Galaxy + InTouch 專案架構
- Day 44：邀請自我審查（Code/Design Review）：檢查物件命名、繼承結構、畫面一致性
- Day 45：**Phase 2 檢核** — 展示可運行的 HMI 專案雛形，撰寫檢核報告

---

## Phase 3：服務鏈深化（Day 46–70）
**目標：完整掌握警報、歷史記錄、製程控制、腳本、報表五大服務**

### Week 8（Day 46–52）：警報管理（Alarm Management）
- Day 46：學習警報等級（Priority）、警報群組（Alarm Group）設計
- Day 47：設定類比量警報（High/Low/HiHi/LoLo）與離散量警報
- Day 48：學習警報確認（Acknowledge）、抑制（Suppression）機制
- Day 49：設計警報通知策略（Email/簡訊整合概念）
- Day 50：練習警報歷史查詢與篩選
- Day 51：整合警報視窗到既有 HMI 專案
- Day 52：週末整合 — 撰寫一份「警報設計規範」文件（可作日後專案模板）

### Week 9（Day 53–59）：歷史記錄（AVEVA Historian）
- Day 53：安裝並設定 AVEVA Historian
- Day 54：學習歷史記錄的資料儲存架構（Tag、Retrieval Mode、Compression）
- Day 55：設定 Tag 的歷史記錄頻率與資料壓縮策略
- Day 56：學習 Historian Client 查詢介面操作
- Day 57：學習 Historian Client Web 的使用場景
- Day 58：練習用 SQL 查詢 Historian 資料庫（Historian 底層為 SQL Server）
- Day 59：週末整合 — 建立一份歷史趨勢報表雛形

### Week 10（Day 60–65）：製程控制（Process Control）
- Day 60：學習 System Platform 中內建的控制邏輯物件（如 PID、Sequencer）
- Day 61：比較 AVEVA 製程控制邏輯與既有 PLC 梯形圖邏輯思維的異同
- Day 62：練習設計簡易 PID 迴路物件並綁定 HMI 顯示
- Day 63：學習狀態機（State Machine）設計模式
- Day 64：練習連鎖保護邏輯（Interlock）設計
- Day 65：週末整合 — 完成一組含 PID 控制與連鎖保護的製程物件

### Week 11（Day 66–70）：腳本（Scripts）
- Day 66：學習 ArchestrA QuickScript 語法基礎
- Day 67：學習腳本觸發時機（On Startup、On Scan、Value Change 等）
- Day 68：練習撰寫自訂邏輯腳本（如條件式警報抑制）
- Day 69：學習腳本除錯（Debug）技巧
- Day 70：**Phase 3 檢核** — 完成整合警報、歷史記錄、製程控制、腳本的中型專案，撰寫檢核報告

---

## Phase 4：整合實戰與部署（Day 71–90）
**目標：完成通訊整合優化、系統部署與期末綜合專案**

### Week 12（Day 71–77）：報表與系統整合
- Day 71：學習 AVEVA Reporting（或整合 SQL Server Reporting Services）基礎
- Day 72：設計一份自動化日報表（產量、稼動率、警報統計）
- Day 73：學習多 Galaxy / 多 Platform 的分散式架構概念
- Day 74：學習與既有 OPC UA / Modbus TCP 系統的整合最佳實務
- Day 75：學習網路架構規劃（防火牆、VLAN 隔離的基本考量）
- Day 76：學習系統備份與還原策略（Galaxy Backup/Restore）
- Day 77：週末整合 — 撰寫一份「系統整合檢查清單」

### Week 13（Day 78–84）：效能優化與正式部署準備
- Day 78：學習掃描週期（Scan Rate）優化原則
- Day 79：學習物件部署負載平衡（跨 WinPlatform 分配 AppEngine）
- Day 80：學習系統健康監控（Diagnostics、Log Viewer）
- Day 81：進行壓力測試（模擬多 Tag、多用戶端連線）
- Day 82：學習使用者權限管理（Security Groups）設計
- Day 83：練習正式環境部署流程（區分開發/測試/正式環境）
- Day 84：週末整合 — 完成部署前檢核表並模擬正式上線

### Day 85–90：期末綜合專案
- Day 85–86：定案期末專案主題（建議：整合農業自動化背景，如「RTK 灌溉站 + 馬達控制 SCADA 系統」）
- Day 87：完成專案架構設計（Galaxy 物件模型、I/O 清單、HMI 畫面規劃）
- Day 88：完成開發（物件、圖形、警報、歷史記錄全部整合）
- Day 89：進行完整測試與除錯
- Day 90：**期末驗收** — 展示完整運行的專案，撰寫 90 天學習總結報告，列出後續深化方向（如 AVEVA Edge、AVEVA Unified Operations Center 等進階模組）

---

## 學習資源建議

| 類型 | 建議來源 |
|---|---|
| 官方文件 | AVEVA 官方 Knowledge & Support 網站（System Platform 使用手冊、Application Server 使用手冊） |
| 視訊教學 | AVEVA 官方 YouTube 頻道系列課程（含本教材來源影片） |
| 社群 | AVEVA Community Forum（實務問題討論） |
| 實作環境 | AVEVA System Platform 試用版授權（通常提供有限期限） |

---

## 檢核與追蹤建議

- 每個 Phase 結束設一次**檢核點**，以「能否獨立完成一個小專案」作為通過標準，而非單純閱讀進度
- 建議每週撰寫簡短學習日誌（3–5 行），記錄卡關處與解決方式，累積成個人 troubleshooting 筆記庫
- 善用既有 PLC/SCADA 背景做「概念映射」（如 Modbus TCP 對應 DAServer、Function Block 對應 ArchestrA Template），可大幅加速理解速度
