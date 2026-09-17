https://www.youtube.com/watch?v=FKFarYHU8kk&list=PLJq4rR8tWINyOrvwxbIjRvgTtoyuuEfSz&index=2
AVEVA™ System Platform - Script Function: Embed Content

https://github.com/cephaswang/SystemPlatform/tree/main/01Core/core02


This video introduces the use of the Embed Content and Remove Embedded Content functions in AVEVA™ OMI applications. It explains how to dynamically embed and remove Industrial Graphics within another graphic during runtime, including specifying properties, location and size, and configuring Custom Properties for complex graphics. 

It also includes practical demonstrations with step-by-step instructions.


以下是影片 《AVEVA™ System Platform - Script Function: Embed Content》 的內容摘要與說明：
影片概要與主要功能介紹

    內嵌內容功能 (Embed Content Function)：在 AVEVA OMI 應用程式運行時（Runtime），此功能允許將工業圖形（Industrial Graphic）動態內嵌至另一個父圖形（Parent Graphic）中，且該內嵌圖形會顯示在最頂層（Top of the z-order）[00:07]。

    結構設定：使用時需宣告一個預定義結構 GraphicInfo [00:27]。必填參數包含標識符（Identity）與圖形名稱（Graphic Name）[00:50]。

    自訂屬性 (Custom Properties)：若內嵌圖形包含自訂屬性，可透過 Custom Property Value Pair 陣列進行配置 [01:08]。此外也可設定位置（Location: X, Y）與尺寸（Size）[01:36]。

    移除內嵌內容 (Remove Embedded Content Function)：傳入對應的標識符（Identity），即可從運行時畫面中移除該動態內嵌圖形 [01:46]。

範例操作說明

    基本內嵌與移除設定

        新增內嵌：在按鈕的 Action Script 中，可透過腳本瀏覽器（Script Function Browser）選取 Embed Content 函數 [02:45]。範例中將 AVEVA 標誌內嵌至指定區域，其標識符設定為 logo，座標指定為矩形區域的 X、Y [03:36]。

        新增移除按鈕：在移除按鈕腳本中呼叫 Remove Embedded Content 並傳入 logo 標識符 [04:10]。

        運行效果：點擊 Embed 按鈕即顯示標誌，點擊 Remove 按鈕則會將該標誌移除 [04:30]。

    多圖形與動態資料連結

        示範同時載入包含兩個自訂屬性（裝置名稱 cp1 與數值 cp2）的圖形 [05:01]。

        設定字串屬性與屬性參考（Reference）後，可以在運行時即時更新與顯示設備數據 [05:23]。

    靈活參數配置與特性比較

        可以將參數綁定至自訂屬性，實現運行時動態切換欲內嵌的圖形、位置與大小 [06:36]。

        與 Show Graphic 函數的差異：使用 Embed Content 內嵌的圖形會直接整合在宿主圖形（Hosting Graphic）中，而非像 Show Graphic 那樣跳出獨立的新視窗顯示 [06:09], [08:00]。



Embed Content
Syntax
Dim graphicInfo as aaGraphic.GraphicInfo;
graphicInfo.Identity = "<Indentity>";
graphicInfo.GraphicName = "<SymbolName>";
EmbedContent(graphiclnfo);


Embed Content
Syntax
Dim graphiclnfo as aaGraphic.Graphiclnfo;
Dim cpValues [2] as aaGraphic.CustomPropertyValuePair;
cpValues[1] = new aaGraphic.CustomPropertyValuePair("CP1", 20, true);
cpValues[2] = new aaGraphic.CustomPropertyValuePair("CP2", <Level.TagName>", true);
graphicInfo.Identity = "123";
graphiclnfo.GraphicName = "Level_Symbol1";
graphicInfo.CustomProperties = cpValues;
EmbedContent(graphiclnfo);

