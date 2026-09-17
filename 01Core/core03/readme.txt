https://www.youtube.com/watch?v=FggRsVRxeTk&list=PLJq4rR8tWINyOrvwxbIjRvgTtoyuuEfSz&index=3

AVEVA™ System Platform - Attribute References 

This video explains the three ways to reference a tag in AVEVA™ Application Server: Direct References, Hierarchical Names, and Relative References. 

Learn how to use Tagname, Container dot Contain Name dot Attribute, and syntax like Me.Attribute, MyContainer.Attribute, and MyArea.Attribute for writing scripts or graphical animation links in industrial graphics.



這支影片標題為 《AVEVA™ System Platform - Attribute References》（來源頻道：AVEVA Operations Control）。

以下是影片字幕的主要內容摘要與整理，介紹了在 Application Server 中引用屬性（Attribute References）的三種主要方式：
1. 直接引用 - 標籤名稱（Tag Name）

    說明：由於物件的每個實體（Instance）都必須擁有獨一無二的名稱，可以直接使用該名稱來進行屬性引用。

    語法格式：Tagname.Attribute

    範例：Level_001.PV

2. 直接引用 - 階層名稱（Hierarchical Name / Contained Name）

    說明：當一個物件被包含於另一個物件之中時（例如 Level_001 隸屬於 Mixer_100），會產生一個包含名稱（Contain Name）。

    語法格式：Container.ContainedName.Attribute

    範例：Mixer_100.Level_001.PV

    應用情境：在工業圖形（Industrial Graphics）中，同時顯示多個不同設備（如多個 Mixer）的數值時，可以使用標籤名稱或階層名稱進行直接引用。

3. 相對引用（Relative References）

相對引用通常用於樣板（Template）等級的腳本或圖形設計中。它允許在尚未指定具體實體的情況下建立引用，並於執行階段（Runtime）自動解析為對應的實體。

常見的相對引用關鍵字包含：

    Me：指向物件實體本身。

        語法：Me.Attribute（例如：Me.PV、Me.PV.Units.Range.Max）

    MyContainer：指向包含該物件的容器物件實體之屬性。

        語法：MyContainer.Attribute

    MyArea：指向該物件所屬區域（Area）的屬性。

        語法：MyArea.Attribute

    MyEngine：指向託管（Host）該物件之 Engine 的屬性。

        語法：MyEngine.Attribute

    MyPlatform：指向託管該 Engine 之 Platform 的屬性。

        語法：MyPlatform.Attribute

影片連結：AVEVA™ System Platform - Attribute References
