https://www.youtube.com/watch?v=LQtvNRI3HZw&list=PLJq4rR8tWINyOrvwxbIjRvgTtoyuuEfSz&index=10
Mastering the Deployment Model in AVEVA™︎ System Platform 

生成中文教程，格式 md ，含引用圖片 images 目錄，圖片為依序取得


Explore the structure of the Deployment Model in AVEVA™ System Platform! 📊💻 

This video explains the roles of Win Platform, App Engine, and Area Objects within the Deployment View, showing how Automation Objects relate to the computers they run on when deployed 🚀. 

Learn about WinPlatform objects, App Engines, View Engines, and WebView Engines 🌐, along with the configuration and features of these components in the process of deploying a Galaxy 🌌. 

The video presents an overview of containment relationships and the execution of applications, Device Integration Objects, and Areas within the Galaxy.



影片 Mastering the Deployment Model in AVEVA™︎ System Platform 的完整字幕內容與時間軸整理如下：

    [00:04] In this video, we will describe the deployment model's structure and explain the role of the WinPlatform, App Engine, and Area objects in this model.

    [00:13] The deployment view shows how automation objects are related to the computers they run on when deployed.

    [00:22] Each computer in the Galaxy is represented by a WinPlatform object. These platforms host other objects in the Galaxy, which are distributed across different computers.

    [00:32] This arrangement is known as the deployment model. This view shows all automation object instances in the Galaxy, excluding templates.

    [00:43] In this model, WinPlatform objects are the top-level objects, and they host the engines.

    [00:54] Each type of engine hosts a different kind of object: App Engines host Device Integration objects and Areas with their assigned application objects;

    [01:04] View Engines host visualization applications, such as the View App for OMI applications and the InTouch View App for InTouch application objects;

    [01:17] Lastly, Web View Engines host View App objects for OMI applications, which can be accessed through a web browser.

    [01:29] The WinPlatform is the first object deployed on a target computer, serving as the foundation for the deployment model.

    [01:36] It includes features such as representing a computer in the Galaxy, monitoring computer stats, starting and stopping hosted engines, and managing off-node communications.

    [01:59] A special instance of the WinPlatform object is needed for Galaxy Repository operations. It is indicated by a special GR Platform icon and must be deployed first for any other deployment-related actions to take place.

    [02:09] Each WinPlatform instance needs to be configured with its network address. The Galaxy Repository platform is automatically configured with the computer name of the host GR (Galaxy Repository).

    [02:31] The number of computers determines the deployment model's base, followed by distributing other objects based on hosting relationships.

    [02:41] The deployment view also shows containment relationships between application objects, with contained objects displaying their name in brackets.

    [02:52] The App Engine is the primary runtime application engine for the Galaxy alongside the WinPlatform object. It executes applications, Device Integration objects, and Areas.

    [03:05] Its key features include real-time schedule-driven execution, communication with the Historian server, and redundancy configuration.

    [03:18] The App Engine runs all hosted objects on a scan-based schedule, executing each object once per scan, one at a time.

    [03:29] Areas are then assigned to these engines.

    [03:37] Let's take a look at our Galaxy. Here we have a WinPlatform object configured as the Galaxy Repository.

    [03:48] Then we have a second WinPlatform object configured to host the plant areas, engines, Device Integration objects, and equipment.