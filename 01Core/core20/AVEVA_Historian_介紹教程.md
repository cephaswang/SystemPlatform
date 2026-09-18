# AVEVA Historian 簡介教程

> 影片來源：[Introduction to AVEVA Historian](https://www.youtube.com/watch?v=cEtMtlNvpSA&list=PLJq4rR8tWINyOrvwxbIjRvgTtoyuuEfSz&index=20)
> 延伸資源：
> - [AVEVA Historian 產品頁面](https://www.aveva.com/en/products/historian/)
> - [AVEVA System Platform 產品頁面](https://www.aveva.com/en/products/system-platform/)

---

## 一、什麼是 AVEVA Historian

AVEVA Historian 是一套專為工業製程設計的高速資料庫，主要用途是持續擷取並儲存製程數據，讓工程師與操作人員能對製程異常進行完整的診斷與故障排除。它強調「即時、安全、可信賴」的資料基礎，讓企業能以第一手的工業數據做出決策。

其核心優勢包括：
- 專為工業場景打造，具備高速資料擷取與資料完整性保護
- 能與 Operations Control（如 OMI）等應用程式簡單整合，讓製程團隊在源頭就能萃取更多價值
- 內建趨勢圖（Trend）、查詢（Query）、報表等資料分析工具，方便進行製程異常的診斷與排查
- 內建資料轉發機制，可將數據送往雲端或其他資訊管理系統，供 AI/ML 等企業級應用使用

一些代表性的效能指標：40 倍的資料壓縮率、僅需 2% 的儲存空間、每秒可處理 150,000 個標籤（tag），並支援超過 200 萬個標籤。

![AVEVA Historian 總覽](images/image01.jpg)

### 支援的資料型態

AVEVA Historian 可以管理多種不同型態的資料，例如：
- **類比（Analog）**：如流量、溫度等連續數值
- **離散（Discrete）**：如開關狀態
- **字串（String）**
- **事件（Event）**
- **狀態摘要（State Summary）**

在設定畫面中，使用者可以針對每個標籤（Tag）指定其工程單位（Engineering Unit）、最大／最小值、內插方式（Interpolation Type）等屬性。

![新增類比標籤與資料型態設定](images/image02.jpg)

透過 Operations Control Management Console（OCMC），使用者也可以直接建立或管理各種類型的手動標籤（Manual Tags），彈性地涵蓋各種工業資料。

![OCMC 中管理各類資料標籤](images/image03.jpg)

---

## 二、與 AVEVA System Platform 的整合

AVEVA Historian 可與 AVEVA System Platform 深度整合，讓使用者依照資產階層（Asset Hierarchy）進行組態設定，大幅簡化建置與維護的流程。

在 System Platform IDE 中，物件之間的關聯（Associations）與內容（Content）可以直接對應到 Historian 的標籤，讓資料模型與實際設備結構保持一致。

![System Platform IDE 中的物件與屬性關聯](images/image04.jpg)

只要在物件的「History」頁籤中勾選需要歷史化（Historize）的屬性（例如 PV、SP 等），並設定儲存週期、死區（Deadband）、內插方式等參數，系統就能利用既有的物件關聯，自動完成歷史化的組態，不需要另外重複設定。

![透過物件關聯簡化歷史化設定](images/image05.jpg)

---

## 三、AVEVA Historian Client 資料分析工具

AVEVA Historian Client 提供了一整套桌面與網頁端的資料分析工具，協助使用者快速排查問題、找出節省成本的機會，並提升生產效率。主要包含四個工具：**Trend（趨勢圖）**、**Query（查詢）**、**Web（網頁版）** 以及 **Excel Add-in（Excel 增益集）**。

![AVEVA Historian Client 四大分析工具](images/image06.jpg)

### 1. Trend 趨勢圖工具

Trend 是一套桌面應用程式，讓使用者可以透過豐富的繪圖與格式設定功能，以視覺化的方式回顧一段時間內的製程資料變化。

在畫面左側的 Tag Picker 中，可以搜尋並勾選想要檢視的標籤；下方的表格則會列出每個標籤的顏色、最大最小值、來源伺服器與 IO 位址等詳細資訊。

![Trend 工具介面與歷史資料檢視](images/image07.jpg)

當同時勾選多個標籤時，Trend 會以不同顏色的曲線疊加顯示，方便使用者比較不同標籤隨時間變化的趨勢，並可透過拖曳游標線來查看特定時間點的數值。

![多筆標籤資料的趨勢曲線比較](images/image08.jpg)

### 2. Query 查詢工具

Query 工具讓使用者可以自行建立 SQL 查詢，並將結果以表格化的資料呈現，方便後續匯出到外部報表工具進行加工。

使用者可以在「Columns」頁籤中勾選想要查詢的欄位（例如 Quality、State Time、Resolution 等），系統會自動產生對應的 SQL 敘述，並顯示查詢結果，協助工程師與操作人員檢視異常事件與其他資料不一致的情況。

![Query 工具產生 SQL 並查詢資料異常](images/image09.jpg)

除了歷史數值查詢外，Query 工具也能查詢標籤本身的詳細組態資訊（Tag Details），例如儲存速率（Storage Rate）、工程單位範圍（Engineering Units Range）、建立日期等，讓使用者能快速掌握每個標籤的設定內容。

![使用 Query 工具查詢標籤詳細資訊](images/image10.jpg)

### 3. Excel Add-in

Excel Add-in 可以直接將 Historian 的資料擷取到 Microsoft Excel 試算表中，讓使用者運用 Excel 熟悉的複雜公式、格式設定選項與圖表功能，產出客製化的報表。

在 Excel 的「Historian」功能區中，使用者可以透過「Live Values」精靈選擇伺服器與標籤來源儲存格，將即時或歷史資料匯入至工作表。

![Excel Add-in 匯入 Historian 資料並製作報表](images/image11.jpg)

### 4. Historian Client Web

Historian Client Web 是一套以瀏覽器為基礎的工具，讓一般（casual）使用者也能輕鬆存取生產數據，並依需求檢視趨勢圖或表格化的資料。

使用者只需在搜尋欄輸入關鍵字，即可搜尋資產、已儲存內容、標籤或其他關鍵字，快速取得對應的生產與績效資料。

![透過瀏覽器存取生產與績效資料](images/image12.jpg)

這些以網頁呈現的儀表板，也可以進一步組合成更豐富的視覺化畫面，例如各種比較圖表、組成圖、時間序列分析等，讓 Historian 的數據能被直覺地存取與應用。

![以視覺化儀表板直覺存取 Historian 資料](images/image13.jpg)

---

## 四、OMI 中的歷史回放（Historical Playback）

AVEVA Operations Management Interface（OMI）提供「Historical Playback」功能，讓操作人員可以直接在 HMI 畫面上，對歷史製程資料進行暫停、倒轉與快轉，藉此回頭調查過去發生的異常事件。

例如在 SCADA Playback 的地圖式儀表板中，使用者可以切換到歷史時間點，觀察當時各地區（如歐洲、美洲、非洲）的即時數值與趨勢曲線。

![OMI 中的歷史回放功能](images/image14.jpg)

在 OMI 的畫面編輯環境中，使用者也可以從 Assets／Attributes 面板搜尋並拖曳資產或屬性到畫面上，快速建立包含歷史資料檢視能力、並可整合第三方軟體的操作介面。

![在 OMI 畫面中加入資產屬性與第三方整合](images/image15.jpg)

---

## 五、資料轉發與數位線程（Digital Thread）整合

AVEVA Historian 所儲存的資料，可以進一步轉發（Forward）並複寫（Replicate）到其他系統，包括：
- **AVEVA PI System**
- **AVEVA Insight**
- **AVEVA Data Hub**（雲端）

這樣的機制建立起橫跨整個企業的「數位線程（Digital Thread）」，確保各部門、各團隊都能以一致、即時的製程資料作為決策依據。

在 AVEVA Data Hub 中，使用者可以透過 Assets／Streams 搜尋特定設備（如 M21）的相關資料流，並選擇不同的時間區間（如最近 8 小時、最近 7 天等）來檢視數位線程延伸到雲端後的資料樣貌。

![AVEVA Data Hub 中檢視延伸自製程的數位線程資料](images/image16.jpg)

要設定資料複寫，可在 System Management Console（SMC）的「Replication Servers」頁面中新增複寫伺服器，並選擇目標複寫環境（例如 AVEVA Historian、AVEVA Insight、AVEVA Data Hub 或 AVEVA PI Server），設定連線資訊與儲存轉發（Store & Forward）路徑等參數，決定資料在複寫失敗時應如何暫存與後續處理。

![設定複寫伺服器與目標複寫環境](images/image17.jpg)

最後，在 Operations Control Management Console 的 Runtime Database 報表頁面中，使用者可以檢視系統參數、標籤數量統計、資料擷取來源、事件標籤與摘要作業等資訊，這些報表同樣有助於製程異常的診斷與故障排除。

![Runtime Database 報表協助製程異常診斷](images/image18.jpg)

---

## 六、小結

AVEVA Historian 作為一套高速工業資料庫，其價值不僅在於資料的擷取與儲存，更在於：

1. 與 AVEVA System Platform 深度整合，簡化以資產階層為基礎的組態設定
2. 透過 Trend、Query、Web、Excel Add-in 等多元分析工具，滿足不同使用情境的資料檢視需求
3. 結合 OMI 的歷史回放功能，讓操作人員能直接在既有 HMI 畫面上回顧歷史事件
4. 透過資料轉發機制串連 PI System、Insight、Data Hub 等系統，建立涵蓋全企業的數位線程

透過以上功能的組合，AVEVA Historian 協助企業建立一致、可信賴的即時工業數據基礎，支援從現場操作到企業決策各個層級的分析與應用。
