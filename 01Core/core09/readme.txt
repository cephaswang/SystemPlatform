https://www.youtube.com/watch?v=Xq4NuX5W7v4&list=PLJq4rR8tWINyOrvwxbIjRvgTtoyuuEfSz&index=9
Publish Historian data to CONNECT with Assets 

生成中文教程，格式 md ，含引用圖片 images 目錄，圖片為依序取得


影片 Publish Historian data to CONNECT with Assets 的完整字幕內容與時間軸整理如下：

    [00:00] We now export the Galaxy model from System Platform into Data Services. Let's see how to do that.

    [00:07] From Historian, I add a new replication server, select "Data Services" as the type, and give it a name.

    [00:13] Hit "Register" and then log into CONNECT.

    [00:24] Once I've logged in, I select from the available namespaces and press "Register". That sets up a trusted connection from Historian to Data Services.

    [00:38] There are some tuning options including the default naming scheme, but I'll keep those defaults.

    [00:45] Once I have a server configured, I can add tags. Enter a wildcard and find the matches, then add them to the list, and repeat that as needed.

    [00:58] Once they're all added, I get a preview of the destination stream name, which I can manually edit if needed.

    [01:04] Then apply that. To complete this, I commit those changes.

    [01:14] Switching over to Data Services, I see all those streams were created. So far, that workflow was the same as in earlier releases,

    [01:19] but I now also see a flat list of the assets matching the Galaxy model with all the properties assigned.

    [01:27] I can select them and see the trend.

    [01:35] Selecting a shorter time period makes it more obvious. I can also run a utility on the Historian to backfill older data into Data Services.

    [01:40] Switch over to Visualization, I see a hierarchical view of these assets.

    [01:51] Select one, and I see the automatically generated asset page.

    [01:58] These can be easily customized to better suit my particular needs, but this is the default view. And it's that simple.