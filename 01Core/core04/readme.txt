https://www.youtube.com/watch?v=bFHncdxlj50&list=PLJq4rR8tWINyOrvwxbIjRvgTtoyuuEfSz&index=4

AVEVA™ System Platform - Deploying the OMI Web Client


生成中文教程，格式 md ，含引用圖片 images 目錄，圖片為依序取得


This video explains the objects needed to deploy applications to the OMI Web Client, a browser-based view application users can access and interact with, as if they were using a regular view application. It covers the essential concepts and processes of application deployment. 

A demonstration of deploying the WebViewEngine and ViewApps is also provided.


影片 AVEVA™ System Platform - Deploying the OMI Web Client 的完整字幕內容與時間軸整理如下：

    [00:04] In this video, I'll explain the workflow for deploying view apps to the OMI web client.

    [00:13] To discuss this workflow, we need to understand the role of web view engine. This component is crucial for supporting the OMI web client.

    [00:23] Its purpose is to deploy and start the services which enables the connections.

    [00:33] Ground the OMI web client here requires a platform to run on, similar to an app engine. Web view engine hosts OMI view apps which are accessed through the OMI web client.

    [00:43] It also enables OMI clients using browsers to subscribe to and receive values from the Galaxy.

    [00:52] If you double-click web view engine, you'll see it requires no configuration, but displays the URL format.

    [01:05] Localhost here can be replaced with the location where web view engine is deployed.

    [01:16] However, if the OMI web client is on a machine with a different domain than the web view engine, you should use the fully qualified domain name (FQDN) of the platform where web view engine is deployed.

    [01:32] In my environment, there are two view apps under web view engine. I'll choose to deploy the web view engine.

    [01:43] And I'll keep the cascade deploy, click the deploy button.

    [01:55] The deployment is now complete for both view apps and web view engine.

