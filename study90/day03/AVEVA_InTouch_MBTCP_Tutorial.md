# AVEVA InTouch HMI
## OI Server 與 Modbus TCP 通訊及 Access Name 設定教學
### OI Server — Modbus TCP Communication & Access Name Configuration Tutorial

雙語教學文件（中文／English）｜ Bilingual Tutorial (Chinese / English)

參考影片 / Reference video: https://www.youtube.com/watch?v=GvCx6QsABxw

---

## Overview 概述

This tutorial demonstrates how to establish a Modbus TCP (MBTCP) communication link between AVEVA's Operations Integration (OI) Server and a PLC/controller, and how to expose the live PLC value to an AVEVA InTouch HMI application through an Access Name and a tag. By the end of this tutorial, a graphic object on an InTouch screen will display a live value read directly from the PLC over Modbus TCP.

本教學說明如何在 AVEVA 的作業整合伺服器（OI Server）與 PLC／控制器之間建立 Modbus TCP（MBTCP）通訊連線，並透過 Access Name 與標籤（Tag），將 PLC 的即時數值帶入 AVEVA InTouch HMI 應用程式中顯示。完成本教學後，InTouch 畫面上的圖形物件將能直接透過 Modbus TCP 顯示從 PLC 讀取的即時數值。

### Required Software 所需軟體

- AVEVA InTouch HMI (development environment / WindowMaker & runtime / WindowViewer)
  AVEVA InTouch HMI（開發環境 WindowMaker／執行環境 WindowViewer）
- AVEVA Operations Integration (OI) Server / System Platform, including the Operations Control Management Console
  AVEVA 作業整合伺服器（OI Server／System Platform），含 Operations Control Management Console
- MBTCP (Modbus TCP) OI Server driver — installed as part of the OI Server setup
  MBTCP（Modbus TCP）OI Server 驅動程式 — 於安裝 OI Server 時一併安裝
- A Modbus TCP–capable PLC, or a Modbus TCP PLC simulator, reachable on the network
  支援 Modbus TCP 的 PLC，或可透過網路連線之 Modbus TCP PLC 模擬器

> **Note / 備註:** This tutorial does not include installers for AVEVA software. AVEVA InTouch HMI and OI Server / System Platform are commercial, licensed products — obtain them from an authorized AVEVA source.
> 本教學不含 AVEVA 軟體安裝檔。AVEVA InTouch HMI 及 OI Server／System Platform 為商業授權軟體，請透過 AVEVA 授權管道取得。

---

## Step 1: Open the Operations Integration Server Manager Console
### 步驟 1：開啟作業整合伺服器管理主控台

From the Windows Start menu, expand the AVEVA program group and select "Operations Control Management Console" (the OI Server Manager). This is the central console where all PC-to-PLC communication drivers are configured.

從 Windows 開始功能表展開 AVEVA 程式集，選擇「Operations Control Management Console」（作業整合管理主控台，即 OI Server Manager）。所有 PC 與 PLC 之間的通訊驅動程式，皆在此主控台中設定。

![AVEVA program group with Operations Control Management Console highlighted](images/3n_01.jpg)

*AVEVA program group with Operations Control Management Console highlighted / AVEVA 程式集，標示出作業整合管理主控台*

---

## Step 2: Review the Server Manager Tree
### 步驟 2：檢視伺服器管理員樹狀結構

In the Operations Integration Server Manager tree, under Default Group > Local, you can see the communication drivers that were installed. In this example only the Modbus TCP (MBTCP) driver appears, because it was the only protocol selected during installation. If other drivers had also been installed, they would be listed here as well.

在「Operations Integration Server Manager」樹狀結構中，於 Default Group > Local 底下，可看到已安裝的通訊驅動程式。本範例僅顯示 Modbus TCP（MBTCP）驅動程式，因為安裝時只選取了此通訊協定；若安裝了其他驅動程式，也會一併列於此處。

![Server Manager tree showing the Modbus - MBTCP driver node](images/3n_02.jpg)

*Server Manager tree showing the Modbus - MBTCP driver node / 伺服器管理員樹狀結構，顯示 Modbus - MBTCP 驅動節點*

---

## Step 3: Configure the PLC Connection Parameters
### 步驟 3：設定 PLC 連線參數

Expand Modicon - MBTCP > OI.MBTCP.1 > Configuration > PORT > PLC to open the "PLC Parameters" tab. Enter the target PLC/PC's network address (IP address) and the Modbus TCP port number (default 502) — these must match the actual device's network settings. In this example, IP 192.168.1.109 is used to reach a PC-based PLC simulator.

展開 Modicon - MBTCP > OI.MBTCP.1 > Configuration > PORT > PLC，開啟「PLC Parameters」頁籤。輸入目標 PLC／PC 的網路位址（IP）與 Modbus TCP 連接埠（預設為 502），此設定須與實際設備的網路配置一致。本範例使用 IP 192.168.1.109 連接以 PC 模擬的 PLC。

![PLC Parameters tab: network address and port number](images/3n_03.jpg)

*PLC Parameters tab: network address and port number / PLC Parameters 頁籤：網路位址與連接埠設定*

---

## Step 4: Create a Device Group (Topic)
### 步驟 4：建立裝置群組（Topic）

Switch to the "Device Groups" tab. In addition to the default groups (PLC_Fast, PLC_Normal, PLC_Slow), right-click to create a new group — this is commonly called a "Topic" and defines a tag update (scan) interval. It can be named freely; in this example it is named "topic1".

切換至「Device Groups」頁籤。除了預設群組（PLC_Fast、PLC_Normal、PLC_Slow）外，可按右鍵新增一個群組，此群組通常稱為「Topic」，用來定義標籤的更新（掃描）週期。名稱可自由命名，本範例命名為「topic1」。

![Device Groups tab with the new "topic1" group](images/3n_04.jpg)

*Device Groups tab with the new "topic1" group / Device Groups 頁籤，新增的「topic1」群組*

---

## Step 5: Activate the Communication Instance
### 步驟 5：啟用通訊實例

Right-click the driver instance (OI.MBTCP.1) and choose "Activate" for it to start automatically on reboot, or "Activate until reboot" for a temporary test. A green checkmark on the instance icon confirms the communication link is active.

在驅動程式實例（OI.MBTCP.1）上按右鍵，選擇「Activate」使其於重開機後自動啟動，或選擇「Activate until reboot」做暫時性測試。實例圖示出現綠色勾勾，即代表通訊連線已成功啟用。

![Right-click menu to activate the OI.MBTCP.1 instance](images/3n_05.jpg)

*Right-click menu to activate the OI.MBTCP.1 instance / 右鍵選單啟用 OI.MBTCP.1 實例*

---

## Step 6: Create an Access Name in InTouch
### 步驟 6：在 InTouch 中建立 Access Name

Open InTouch WindowMaker and go to Tools > Configure > Access Names. Click "Add" to create a new Access Name — this links InTouch tags to the OI Server. Give it a name, for example "ModbusTCP", and select "SuiteLink" as the protocol.

開啟 InTouch WindowMaker，進入 Tools > Configure > Access Names，點選「Add」新增一個 Access Name，用來連結 InTouch 標籤與 OI Server。輸入名稱，例如「ModbusTCP」，並選擇「SuiteLink」作為通訊協定。

![Access Names list with the Add Access Name dialog open](images/3n_08.jpg)

*Access Names list with the Add Access Name dialog open / Access Names 清單與「Add Access Name」對話框*

---

## Step 7: Set the Application Name
### 步驟 7：設定 Application Name

In the Add Access Name dialog, leave "Node Name" blank if the OI Server runs on the same computer as InTouch (otherwise enter that server's computer name). In "Application Name", enter the OI Server application name configured earlier — in this example, "MBTCP".

在「Add Access Name」對話框中，若 OI Server 與 InTouch 位於同一台電腦，「Node Name」可留空（否則需輸入該伺服器的電腦名稱）。在「Application Name」欄位輸入先前設定的 OI Server 應用程式名稱，本範例為「MBTCP」。

![Application Name set to "MBTCP"](images/3n_07.jpg)

*Application Name set to "MBTCP" / Application Name 設為「MBTCP」*

---

## Step 8: Set the Topic Name and Save
### 步驟 8：設定 Topic Name 並儲存

In the "Topic Name" field, enter the same Topic created in Step 4 (in this example, "topic1"). Click OK and save. Together, the Access Name, Application Name and Topic Name define the complete communication path from InTouch to the PLC.

在「Topic Name」欄位輸入與步驟 4 相同的 Topic 名稱（本範例為「topic1」）。按下 OK 並儲存。Access Name、Application Name 與 Topic Name 三者共同定義了 InTouch 到 PLC 的完整通訊路徑。

![Topic Name field completed with "topic1"](images/3n_09.jpg)

*Topic Name field completed with "topic1" / Topic Name 欄位填入「topic1」*

---

## Step 9: Create a New Tag and Select Its Type
### 步驟 9：新增標籤並選擇標籤類型

Open the Tagname Dictionary and click "New" to create a tag. In the Tag Types dialog, select "I/O Integer" — this means the tag reads/writes directly to the connected PLC/controller, rather than being an internal memory-only tag.

開啟「Tagname Dictionary」（標籤字典），點選「New」新增一個標籤。在「Tag Types」對話框中選擇「I/O Integer」，代表此標籤將直接與連接的 PLC／控制器讀寫資料，而非僅為內部記憶體標籤。

![Tag Types dialog with "I/O Integer" selected](images/3n_06.jpg)

*Tag Types dialog with "I/O Integer" selected / Tag Types 對話框，選取「I/O Integer」*

---

## Step 10: Configure the Tag Details
### 步驟 10：設定標籤詳細內容

Enter the tag name (in this example, "Mixer100_Level_PV"), set access to Read/Write, and select the Access Name created earlier ("ModbusTCP"). In the "Item" field, enter the PLC register address — here, register 300002 (a Modbus holding register). Set the engineering range: Min EU 0, Max EU 1000, Max Raw 4095, with Linear conversion, and set the engineering units (e.g. "Litre"). This scales the raw PLC value into the value that will be displayed.

輸入標籤名稱（本範例為「Mixer100_Level_PV」），存取方式設為 Read/Write，並選取先前建立的 Access Name（「ModbusTCP」）。在「Item」欄位輸入 PLC 暫存器位址，此處為 300002（Modbus 保持暫存器）。設定工程量範圍：Min EU 為 0、Max EU 為 1000、Max Raw 為 4095，轉換方式選擇 Linear（線性），並設定工程單位（例如「Litre」，公升）。此設定會將 PLC 的原始數值換算為要顯示的數值。

![Tagname Dictionary: tag details, Access Name and Item address](images/3n_10.jpg)

*Tagname Dictionary: tag details, Access Name and Item address / Tagname Dictionary：標籤詳細內容、Access Name 與 Item 位址*

---

## Step 11: Link the Tag to a Graphic Symbol
### 步驟 11：將標籤連結至圖形符號

On the InTouch drawing canvas, double-click the target graphic symbol (e.g., the tank cylinder) to open its "Edit Symbol Properties" dialog. Under Custom Properties, select the "Value" property and enter the tag name created above ("Mixer100_Level_PV") as its Default Value, then click OK to apply.

在 InTouch 繪圖畫面上，雙擊目標圖形符號（例如水槽圖形），開啟「Edit Symbol Properties」對話框。在 Custom Properties 中選取「Value」屬性，於 Default Value 欄位輸入前面建立的標籤名稱（「Mixer100_Level_PV」），再按下 OK 套用設定。

![Edit Symbol Properties: Value bound to Mixer100_Level_PV](images/3n_11.jpg)

*Edit Symbol Properties: Value bound to Mixer100_Level_PV / Edit Symbol Properties：Value 屬性綁定 Mixer100_Level_PV*

---

## Step 12: Verify the Result in Runtime
### 步驟 12：在執行模式中驗證結果

Switch to Runtime / WindowViewer mode. The graphic objects (tank level, gauge, digital display) should now update in real time, reflecting the live value received from the PLC through the "Mixer100_Level_PV" tag — confirming that the Modbus TCP communication and tag configuration were completed successfully.

切換至執行模式（Runtime／WindowViewer）。此時圖形物件（水槽液位、指針錶、數值顯示）應會即時更新，反映透過「Mixer100_Level_PV」標籤從 PLC 收到的即時數值，確認 Modbus TCP 通訊與標籤設定皆已正確完成。

![Runtime view: graphics updating live from the PLC via Mixer100_Level_PV](images/3n_12.jpg)

*Runtime view: graphics updating live from the PLC via Mixer100_Level_PV / 執行模式畫面：圖形透過 Mixer100_Level_PV 即時更新*

---

## Summary 總結

With the driver configured and activated on the OI Server side, and the Access Name, Topic, and I/O tag configured on the InTouch side, any InTouch graphic bound to that tag will show live data from the PLC. The same pattern — configure the driver connection, create a topic, create an Access Name pointing to it, then create I/O tags referencing PLC register addresses — applies to any OI Server driver, not just Modbus TCP.

完成 OI Server 端的驅動程式設定與啟用，以及 InTouch 端的 Access Name、Topic 與 I/O 標籤設定後，任何綁定該標籤的 InTouch 圖形都能顯示來自 PLC 的即時資料。此設定模式（設定驅動程式連線 → 建立 Topic → 建立指向該 Topic 的 Access Name → 建立參照 PLC 暫存器位址的 I/O 標籤）不僅適用於 Modbus TCP，亦可套用於其他 OI Server 驅動程式。
