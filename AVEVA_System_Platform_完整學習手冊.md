# AVEVA™ System Platform 完整學習手冊
### 入門教學｜90 天學習企劃案｜實作練習專案（整合版）

> 本文件整合三部分內容：① 原始入門教學筆記、② 90 天分階段學習企劃、③ 對應各階段的實作練習專案。學習者具備 PLC（Mitsubishi FX5U、Delta AS、Siemens S7）、SCADA/HMI（FUXA、Node-RED、ScadaBR）、Modbus TCP、OPC UA 等背景，練習專案以此為基礎並延伸至精準農業應用場景（RTK 灌溉站、馬達控制）。

---

# 第一部分｜AVEVA System Platform 入門教學

> 影片來源：[What is AVEVA™ System Platform?](https://www.youtube.com/watch?v=OVJmcTxKwgk)

## 課程簡介
AVEVA™ System Platform 是整合廠區控制與資訊管理系統的工業軟體平台，涵蓋：
- 即時資料擷取（Real-time Data Acquisition）
- 視覺化（Visualization）
- 警報管理（Alarm Management）
- 歷史資料記錄（Historization）
- 製程控制（Process Control）
- 報表（Reporting）

提供**多使用者、物件導向**平台開發、執行、監控與視覺化應用程式所需的框架與工具。

## 一、System Platform 組成與客戶端架構
三層架構：**資料來源層 → 平台核心層 → 監督式客戶端層**

**1. 底層：資料來源** — Controllers（PLC）、Software、Data Sources

**2. 中層：System Platform 核心**

| 元件 | 說明 |
|---|---|
| AVEVA Application Server | 物件導向架構，開發與部署應用程式 |
| AVEVA Historian | 歷史資料儲存與管理 |
| AVEVA Communication Drivers | 與控制器/設備通訊 |

**3. 上層：監督式客戶端** — Operations Management Interface、InTouch for System Platform、Historian Client、Historian Client Web

資料雙向流動：控制器 → 平台核心（收集、儲存）→ 監督式客戶端（視覺化、操作）

## 二、核心概念與術語

| 術語 | 定義 |
|---|---|
| Application Server | 物件導向框架與工具的統一開發／部署環境 |
| Bootstrap | 提供接收平台所需之基礎軟體的核心服務 |
| System Platform IDE | 設定與部署 Galaxy 的整合開發環境 |
| Galaxy | 應用程式、設定資訊與專案資料庫 |
| Galaxy Repository | 主機並管理 Galaxy 的單一電腦與軟體 |

**重點記憶：** Bootstrap 先啟動基礎服務 → 透過 IDE 開發 Galaxy → Galaxy 儲存在 Galaxy Repository 中集中管理。

## 三、System Platform 服務功能
圍繞 **Galaxy（中央資料庫）** 的完整服務鏈：

1. I/O → 2. Graphics → 3. Data → 4. Alarms → 5. History → 6. Process Control → 7. Scripts → 8. Reporting

體現「單一資料來源、多重應用」的設計理念。

## 課程總結
- 物件導向、多使用者的工業自動化整合平台
- 三層架構：資料來源 → 平台核心 → 監督式客戶端
- 核心流程：Bootstrap → IDE → Galaxy → Galaxy Repository
- 完整服務鏈：I/O 到報表，支援即時監控、警報、歷史記錄與製程控制

---

# 第二部分｜90 天學習企劃案

## 企劃目標

| 項目 | 內容 |
|---|---|
| 總時長 | 90 天（約 13 週） |
| 每日投入 | 平日 1.5–2.5 小時，週末 3–4 小時整合練習 |
| 先備知識 | PLC 邏輯、SCADA 基礎、Modbus/OPC UA |
| 最終產出 | 可運行的 Galaxy 專案：I/O、HMI、警報、歷史記錄、報表、腳本 |
| 建議環境 | AVEVA System Platform 試用版 + Application Server + InTouch + Historian |

## 課程總覽

| 階段 | 天數 | 主題 |
|---|---|---|
| Phase 1：基礎建置 | Day 1–20 | 架構認識、環境安裝、核心術語 |
| Phase 2：物件與圖形開發 | Day 21–45 | ArchestrA 物件導向、Galaxy 開發、InTouch 圖形 |
| Phase 3：服務鏈深化 | Day 46–70 | 警報、歷史記錄、製程控制、腳本、報表 |
| Phase 4：整合實戰與部署 | Day 71–90 | 通訊整合、效能優化、部署、期末專案 |

### Phase 1：基礎建置（Day 1–20）
- **Week 1**：架構筆記、申請試用版、安裝 Application Server + Bootstrap、建立 Galaxy Repository
- **Week 2**：IDE 入門、Template/Instance 概念、首個物件部署、WinPlatform/AppEngine、版本控制
- **Week 3**：DAServer/OI Server、Modbus TCP 驅動設定、串接既有 PLC、I/O Tags 驗證、OPC UA
- **檢核**：完成「PLC → AVEVA I/O Tag」端對端資料擷取小專案

### Phase 2：物件與圖形開發（Day 21–45）
- **Week 4**：Template 繼承、UDA、Extension、設備範本設計、批次實例化
- **Week 5**：InTouch WindowMaker/Viewer、Symbol/Wizard/ArchestrA Graphic、流程圖繪製、動畫連結
- **Week 6**：多視窗導覽、Style Library、參數化 Symbol、趨勢圖、警報視窗
- **Week 7**：以 RTK 灌溉站監控為題設計專案架構、自我審查
- **檢核**：展示可運行的 HMI 專案雛形

### Phase 3：服務鏈深化（Day 46–70）
- **Week 8**：警報等級/群組、類比與離散量警報、確認/抑制機制、通知策略
- **Week 9**：安裝 Historian、資料儲存架構、記錄頻率與壓縮、Historian Client/Web、SQL 查詢
- **Week 10**：PID/Sequencer 物件、狀態機、連鎖保護邏輯
- **Week 11**：QuickScript 語法、觸發時機、自訂邏輯、除錯
- **檢核**：完成整合警報、歷史記錄、製程控制、腳本的中型專案

### Phase 4：整合實戰與部署（Day 71–90）
- **Week 12**：Reporting、日報表設計、多 Galaxy/Platform 架構、系統整合、備份還原
- **Week 13**：掃描週期優化、負載平衡、健康監控、壓力測試、權限管理、部署流程
- **Day 85–90**：期末綜合專案 —「RTK 灌溉站 + 馬達控制 SCADA 系統」設計、開發、測試、驗收與總結報告

---

# 第三部分｜實作練習專案

> 統一主題：**「智慧灌溉站監控系統」**（貫穿全部 90 天，難度逐階段疊加），結合你熟悉的 RTK GNSS 精準農業場景與既有 PLC/馬達控制經驗，讓每個 Phase 的練習都累積成同一個最終系統的一部分，而非零散習題。

## 專案總覽

| 項目 | 內容 |
|---|---|
| 專案名稱 | 智慧灌溉站 SCADA 監控系統（Smart Irrigation SCADA） |
| 模擬場域 | Houli/Waipu 農地灌溉站：1 座抽水站（馬達 + 變頻器）、2 條灌溉支線（電磁閥控制）、1 組水位/流量感測、1 台既有 PLC（Mitsubishi FX5U 或 Delta AS 皆可） |
| 通訊方式 | PLC 端用 Modbus TCP（若練習 OPC UA 則另建一組 Server 模擬） |
| 最終交付 | 一個完整 Galaxy 專案，可獨立匯出/部署，含操作手冊 |

---

## 專案一（對應 Phase 1，Day 1–20）：I/O 擷取雛形
**目標：完成端對端資料擷取，驗證通訊鏈路**

**任務清單：**
1. 在既有 PLC（或模擬器，如 Modbus TCP Slave 模擬軟體）建立測試點位：
   - `PumpStatus`（BOOL，馬達運轉狀態）
   - `PumpRunHours`（INT，累計運轉時數）
   - `Valve1_Status` / `Valve2_Status`（BOOL，電磁閥開關）
   - `WaterLevel`（REAL，水位百分比 0–100）
   - `FlowRate`（REAL，流量 L/min）
2. 在 Application Server 建立 Modbus TCP DAServer 連線
3. 建立對應 I/O Tags，並在 IDE 中即時監看數值變化
4. 手動改變 PLC 端點位數值，驗證 AVEVA 端是否即時同步

**驗收標準：** 5 個點位皆能穩定即時更新，延遲 < 2 秒；撰寫一頁「通訊架構圖 + 點位對照表」

---

## 專案二（對應 Phase 2，Day 21–45）：物件模型與 HMI 畫面
**目標：以物件導向方式重新設計，並完成第一版視覺化畫面**

**任務清單：**
1. 設計三個 ArchestrA Template：
   - `Template_Motor`（馬達通用範本：運轉狀態、累計時數、啟停指令、故障旗標）
   - `Template_Valve`（電磁閥範本：開關狀態、開關指令）
   - `Template_Sensor`（感測器範本：數值、單位、量測範圍上下限 UDA）
2. 由範本實例化出：`Pump01`、`Valve01`、`Valve02`、`LevelSensor01`、`FlowSensor01`
3. 繪製 InTouch 主畫面：
   - 抽水站流程圖（管線、馬達圖示、動態顏色表示運轉/停止）
   - 兩條支線閥門圖示與開關按鈕
   - 水位/流量數值顯示 + 簡易趨勢圖
4. 建立導覽選單：「總覽頁」與「設備明細頁」兩個視窗切換

**驗收標準：** 操作人員可從 HMI 直接看懂全站運作狀態，並能手動開關閥門測試（若允許寫入）

---

## 專案三（對應 Phase 3，Day 46–70）：警報、歷史記錄、控制邏輯
**目標：加入智慧化邏輯，使系統具備真實產線水準**

**任務清單：**
1. **警報設計：**
   - 水位過低（LoLo）→ 高優先警報，自動觸發停止抽水馬達的連鎖邏輯
   - 流量異常偏低但馬達運轉中 → 判斷可能阻塞，中優先警報
   - 馬達累計運轉時數超過保養門檻 → 低優先提醒警報
2. **歷史記錄：**
   - 設定 `WaterLevel`、`FlowRate`、`PumpRunHours` 加入 Historian 記錄
   - 建立每日用水量趨勢查詢（用 Historian Client 或 SQL 查詢驗證資料）
3. **製程控制邏輯：**
   - 建立簡易「定時灌溉」Sequencer：依排程自動開啟 Valve1 → 延時 → 關閉 → 開啟 Valve2 → 延時 → 關閉
   - 建立連鎖保護：水位 LoLo 時強制停止馬達並鎖定，需人工確認才能重啟
4. **腳本：**
   - 撰寫 QuickScript：當 `FlowRate` 連續 30 秒為 0 且馬達運轉中，自動寫入「疑似空轉」診斷旗標

**驗收標準：** 模擬觸發水位過低情境，系統應自動停機、警報跳出、歷史記錄可查到事件前後數值變化

---

## 專案四（對應 Phase 4，Day 71–90）：整合部署與期末驗收
**目標：完成正式化部署與系統文件，作為 90 天學習總驗收**

**任務清單：**
1. **報表：** 建立「每日灌溉與用水量日報表」（自動彙總 Historian 資料，含馬達運轉時數統計）
2. **系統架構優化：**
   - 檢視掃描週期設定是否合理（水位/流量可 1 秒，馬達累計時數可 10 秒）
   - 若模擬多台設備，練習跨 WinPlatform 部署平衡
3. **權限管理：** 建立「操作員」（只能看、可開關閥門）與「工程師」（可修改設定）兩組 Security Group
4. **備份與還原：** 完整執行一次 Galaxy Backup，並在另一台（或同台不同路徑）還原測試
5. **期末文件：**
   - 系統架構圖（資料來源 → Galaxy → HMI）
   - 點位清單（I/O List）
   - 警報一覽表
   - 操作手冊（含常見異常排除步驟）
   - 90 天學習總結：記錄哪些概念與既有 PLC/SCADA 經驗最相似、哪些是全新學習

**驗收標準：** 系統可從 Backup 檔案完整還原並正常運作；能對外（如同事或線上社群）完整簡報這套系統 15 分鐘

---

## 練習專案時程對照表

| 天數 | 對應專案 | 主要交付物 |
|---|---|---|
| Day 1–20 | 專案一：I/O 擷取雛形 | 通訊架構圖 + 點位對照表 |
| Day 21–45 | 專案二：物件模型與 HMI 畫面 | 可操作的 HMI 主畫面 |
| Day 46–70 | 專案三：警報、歷史記錄、控制邏輯 | 具備自動保護邏輯的完整系統 |
| Day 71–90 | 專案四：整合部署與期末驗收 | 完整部署文件 + 期末簡報 |

---

## 延伸建議
- 若試用版授權到期較早，可將專案一、二優先完成並截圖/錄影存證，作為履歷或作品集素材
- 期末系統若運作良好，可評估是否延伸應用到實際農地灌溉站，銜接你既有的 RTK 自動導航與精準農業工作
- 後續深化方向：AVEVA Edge（邊緣運算 HMI）、AVEVA Unified Operations Center（多站整合管理）
