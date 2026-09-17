https://www.youtube.com/watch?v=hLNudct1GcA&list=PLJq4rR8tWINyOrvwxbIjRvgTtoyuuEfSz


AVEVA ProveIt! Conference 2026 - IIoT Platform: System Platform Demo 


See how data comes to life across our customers’ digital transformation journeys—from COLLECT and CONNECT to ANALYZE, VISUALIZE, and STORE. 

Powered by the ProveIt Infrastructure Unified Namespace (UNS) Broker, this demonstration highlights how enterprises unlock measurable business value from their data by leveraging AVEVA System Platform, as the core IIoT platform, and AVEVA Historian to securely store and analyze data using advanced AI‑driven capabilities.

https://github.com/AVEVA/Galaxy-Builder


這支影片 《AVEVA ProveIt! Conference 2026 - IIoT Platform: System Platform Demo》 的完整字幕重點整理如下：
影片字幕重點內容

    影片介紹與團隊成員 [00:07]

        主講人：Ahmed Khalil（System Platform 技術產品經理）與 Jacob Hawks（HMI SCADA 團隊戰略產品經理）。

        主題：展示 AVEVA 如何協助客戶進行數位轉型，涵蓋收集（Collect）、連接（Connect）、分析（Analyze）、視覺化（Visualize）及儲存（Store）系統資料。

    MQTT Broker 與模型架構構建 [00:37]

        為了改善資料平坦化的問題並進行 AI 分析演示，團隊構建了模擬環境，並在 MQTT Broker 中新增名為 Aviva 的站點 [01:02]。

        使用 GitHub 上的開源工具連接至 MQTT Broker，自動讀取結構並建立標準範本，方便擴充與複製至其他站點 [01:25]。

        只需簡單點擊幾下，即可將整個模型回傳發布至 Broker 中 [02:07]。

        支援導入 SVG 向量圖檔案作為圖形元件，讓應用程式在幾天內即可快速部署完成 [02:31]。

    AI 與 MCP (Model Context Protocol) 整合展示 [03:44]

        模擬資料與 Unified Namespace：透過模擬器將資料寫入區域 Broker，由 System Platform 接收後再重新發布至 ProveIt Broker，供現場其他廠商共享 UNS 資料 [03:54]。

        MCP Gateway 整合：System Platform 搭配 AVEVA Historian，並建立 MCP Gateway 來公開 Historian 豐富的資料檢索與分析 API [04:20]。

        Claude AI Agent 分析實例：

            直接向 Claude AI Agent 提出自然語言問題：「能否找出熔爐溫度偏差（furnace temperature deviation）與冷端不良率（cold end reject rate）之間的關聯性？」[04:53]

            在未提供任何 Tag 名稱或歷史資料庫連線設定的情況下，AI 透過 MCP Server 自動尋找適當工具、識別 Tag 並分析數據 [05:12]。

            AI 進行自我分析與提示修正後，成功找出溫度變化的異常趨勢與關聯性 [05:47]。

    OMI 邊緣端整合與一鍵式分析 [06:10]

        結合 OMI（Operational Management Interface）產品，將 Historian 節點的視覺化圖表嵌入至介面中 [06:20]。

        透過背景 Context 共享，點擊單一按鈕（Analyze 功能）即可自動觸發 Process Value API，呼叫 AI 對畫面上顯示的 4 個 Tag 數據進行即時分析 [06:30]。

    雲端平台部署 (AVEVA Connect) [07:25]

        將地端（On-premise）應用程式無縫搬移至雲端平台 AVEVA Connect [07:44]。

        僅需短短數小時即可在雲端發布並運行相同的應用程式，提供一致的使用者體驗 [07:53]。


《AVEVA ProveIt! Conference 2026 - IIoT Platform: System Platform Demo》完整字幕

    **** Hello, welcome to AVEVA ProveIt conference booth. My name is Ahmed Khalil, the technical product manager for System Platform,

    **** and with me Jacob Hawks, a strategic product manager in the HMI SCADA group. And we're going to show you

    **** today how we are helping our customers in the digital transformation journey, same like last year, to collect, connect, analyze,

    **** visualize, and store their systems. First, we got to start with how was the enterprise A came from the Pro

    **** Infrastructure Broker. Okay, as you can see on the top right here on the screen, uh, the Dallas

    **** site came as lines one and site, and the values there wasn't like flat line. So we needed

    **** to add some simulation uh to be able to run some of or to show how our AI is doing

    **** uh some analysis on it. Uh, with that being said, we needed to create another site, okay, called AVEVA, okay,

    **** based on uh the templates that been gathered by uh the tool that we're using uh to connect to the

    **** MQTT broker. As you can see on the

    **** uh left corner, okay, bottom left corner, we are using a tool that's source code is

    **** currently on GitHub. Okay, this tool helps to connect to the MQTT broker uh ingest the structure, okay,

    **** and on top of that building the templates and the standards for you to be able to use it with

    **** other uh sites or to create on top of that another sites. Uh, so what we did is like creating

    **** another site called AVEVA and we pushed our simulation there. So right now you are connecting MQTT and publishing back.

    **** As you can see here, with just a matter of couple of clicks uh within our software, you can publish

    **** the whole model back to the broker and uh that will give you, you know, how to see the

    **** model inside our application.

    **** Then with the help of some features, helpful features inside System Platform and OMI, we will be able, you know,

    **** to ingest uh as well the graphics from SVG files which make application uh ready in

    **** in couple of days after, you know, like fixing stuff, and I will go through the application for you right

    **** now.

    **** So as you can see here, you can find the whole model ingested from the MQTT

    **** on the screen, and also the SVG uh import symbols are on the screen right now. We were able,

    **** you know, to uh visualize every single level for AVEVA and you see our simulation is going there.

    **** So Line 1 called end,

    **** Batch House and Hotend.

    **** That's taking care of the connect and collect and visualize. Okay, for the store part, uh we added some uh

    **** simulation plus uh we run some AI visualization for that based on this architecture which Jake will taking you

    **** through. Exactly. Yeah, so as we've said before, we have our simulator here that is injecting simulated values

    **** into our local broker, which is being picked up by System Platform and then republished out to the ProveIt

    **** broker, and in this way then all of the other vendors on the floor can take advantage of our unified

    **** namespace additions, which is that simulated data set which is changing. Um System Platform is paired up with the AVEVA

    **** Historian and on top of that AVEVA Historian, we um wrote an MCP gateway which exposes the very rich set

    **** of APIs that Historian has for data retrieval, analysis, and and so on. Um the first experiment we did was

    **** just hooking up that MCP server to the Claude agent

    **** and then asking it a question which we knew the answer to. So we wrote our own simulator and with

    **** that simulator we were able to inject some anomalies as well as data that was changing. So knowing that, we

    **** then asked this Claude agent a very simple question as you see here, just one sentence, um asking it if

    **** it could find a correlation between the furnace temperature deviation and the cold end reject rate. So we didn't tell

    **** it any tag names, we didn't tell it to connect to the Historian, but it has an MCP server built

    **** uh connected in. So the first thing it did is it understood the query. Then it started to find

    **** the tools that it had available to it in the Historian MCP server and then started to use those tools

    **** to find the tag names and to start getting a look at some of that data. These API requests

    **** are already in the AVEVA Historian today and they underpin our own visualization tools. Um so making them available via

    **** MCP was actually a relatively straightforward endeavor. We can see here then that the agent continues to analyze and self-analyze

    **** and self-prompt itself until it got to the point where it was finding some significant excursions in the temperature

    **** profile. It continued to look at that uh downstream and then was able to find that correlation that we knew

    **** was there in the beginning. But we weren't satisfied with that, so we took it one step further. If I

    **** bring us now to the furnace, we'll go to the edge using the power of the OMI, the Operational Management

    **** Interface product. We are embedding here a visualization that's actually being served from that Historian node. With one click, we

    **** have context sharing between that iframe from the Historian node and the OMI app. And we're seeing here

    **** now that we're plotting those four tags that are present on that OMI screen. One of the beauties of having

    **** your own agent is that you can wire it in to your UI

    **** the way you want. And so with one mouse click here, I haven't typed anything yet, but with one mouse

    **** click here I was able to select the analyze feature on that process value API call, and the AI is

    **** now going to look at those four tags and give you a generic kind of analysis of what it's seeing

    **** um with a pre-canned prompt that we've got in our agent. Um we think this is very exciting. It's only

    **** the beginning. Um and uh we're very excited to bring more tools to our MCP agent including tools in

    **** from the System Platform node and and other nodes in the system. Um and that's the AI portion.

    **** Thank you. Yeah, moreover we added one more step, which is taking our customers to cloud.

    **** Okay, and we're going to show you the same exact application that was here on-prem, okay, to the cloud.

    **** Uh let me connect quickly here to the cloud. This is our cloud called Connect,

    **** to show you the same exact application in matter of hours, matter of like couple of hours, and it will

    **** be used in the cloud as well, published to the cloud as well.

    **** This is... there we go. This is the same application that's been on the prem. You show it on the

    **** prem and we are running it from the cloud. So our customers can go through the old digital transformation steps:

    **** connect, collect, analyze, store, visualize. Okay, and also go to the cloud and in decent amount of time get that

    **** same experience in the cloud and get the same experience on the cloud.

    **** And that's why we are here for. Uh that was like the enterprise A simulation for ProveIt this year.

    **** See you next year. Thank you.



