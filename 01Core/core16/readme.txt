https://www.youtube.com/watch?v=TCFDO34ZQkg&list=PLJq4rR8tWINyOrvwxbIjRvgTtoyuuEfSz&index=16
AVEVA Shorts - Big String Data Feature in AVEVA System Platform

請取得完整字幕

生成中文教程，格式 md ，含引用圖片 images 目錄，圖片為依序取得


In this video, follow along with as we take you through a quick demo of the big string data feature in AVEVA System Platform. See how it enables users to store and transmit large strings by supporting a virtually unlimited string size.

For more information on AVEVA System Platform visit:
https://www.aveva.com/en/products/system-platform/

這支影片 AVEVA Shorts - Big String Data Feature in AVEVA System Platform（影片連結：https://www.youtube.com/watch?v=TCFDO34ZQkg）的完整字幕內容摘要整理如下：
字幕內容摘要與時間軸

    [00:05] 功能介紹： AVEVA System Platform 2023 推出的 Big String（大字串）資料型態功能，支援幾乎無限長的字串大小，讓使用者能夠儲存與傳輸大規模字串。

    [00:21] 使用限制說明：

        不支援應用於警報訊息（Alarm Messages）中。

        若具有 I/O 擴充（Input Output Extensions），則不支援快取緩衝（Buffering）。

        歷史紀錄化（Historization）最高支援至 1,000 個字元，超過部分會被截斷（Truncated）。

    [00:44] 範例演示： 建立一個 Query，將所有國家名稱及其經緯度資訊儲存在 Big String 資料型態中。

    [00:59] 建立屬性： 新建衍生範本（Derived Template），新增一個名為 CMD query 的屬性，以及另一個名為 response Json 的屬性，並將後者的資料型態設定為 Big String。

    [01:06] 撰寫腳本： 在腳本頁籤中新增 Script，設定為非同步（Asynchronously）執行的 While True，觸發週期設為 0。腳本內指定拉取所有國家及其經緯度資料。

    [01:31] 部署與實例化： 依此範本建立實例（Instance），指定至導覽樹位置後部署至執行期環境（Runtime Environment）。

    [01:45] 物件檢視器測試： 開啟 Object Viewer，將 CMD query 與 response Json 新增至觀察視窗（Watch Window）。

    [02:02] 觸發與結果展示： 將 CMD query 改為 True 後觸發腳本，系統回傳包含各國經緯度的完整 JSON 字串。傳統 String 資料型態無法支援此長度的訊息。

    [02:16] 總結： AVEVA System Platform 2023 的 Big String 功能大幅提升了長字串資料傳輸與儲存的彈性。