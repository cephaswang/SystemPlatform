https://www.youtube.com/watch?v=VbKD7PqkfL4&list=PLJq4rR8tWINyOrvwxbIjRvgTtoyuuEfSz&index=8
How It Works: AVEVA System Platform Components Deep Dive 

生成中文教程，格式 md ，含引用圖片 images 目錄，圖片為依序取得

This video provides an overview of the components and clients that make up AVEVA™ System Platform, such as Application Server, Operations Management Interface, Historian, Historian Client, and so on. It also explains the role each of the components and clients play in developing and running a project, including object distribution capabilities and the collection, storage, retrieval, and visualization of data.

影片 How It Works: AVEVA System Platform Components Deep Dive 的完整字幕內容與時間軸整理如下：

    [00:05] All AVEVA System Platform software products are based on industry standards and Microsoft technologies such as Windows, .NET, SQL Server, IIS, and others.

    [00:18] The System Platform components and its clients provide the framework and tools to develop, execute, monitor, and visualize your application.

    [00:29] System Platform on the whole accesses all external data from software applications and third-party data sources and controllers.

    [00:41] It is comprised of the following products: AVEVA Application Server — this is the heart of System Platform. It provides the services and tools to create, manage, and deploy your application.

    [00:51] An application created with Application Server is called a Galaxy.

    [01:02] Based on object-oriented framework, Application Server allows you to assemble a project out of smaller individual objects that represent the different parts of your plant and your application.

    [01:14] These are assembled from an area or a section of the factory to every piece of equipment in the field, such as valves, tanks, pumps, and so on.  

    [01:31] These objects are then sent to the computers running your application. Almost everything that is part of your project can be modeled as an object in a Galaxy.  

    [01:39] A point-and-click interface allows you to easily create, configure, and manage your objects, and at the same time allows the extension and enhancement of your application through integration with the .NET framework, particularly through a powerful scripting engine.

    [01:58] Applications created with Application Server have distribution capabilities by nature. Going from one computer to a multi-node networked environment is simply a matter of modeling the computers that will be part of your project and distributing the load of the application across them.

    [02:18] This functionality also allows you to easily create and deploy redundant configurations.

    [02:29] Some of the main characteristics and benefits of Application Server are: extensibility through a scripting engine with .NET capabilities;

    [02:42] Object-oriented framework that provides a modeling approach for creating and managing applications; native support for DDE, SuiteLink, and OPC to access AVEVA and third-party drivers such as OI servers and legacy I/O servers;

    [02:52] And redundancy capabilities for your application; security features to prevent users from performing unauthorized activities within the development and runtime environments;

    [03:04] Multi-user development environment; out-of-the-box graphic libraries, one of them designed to create situational awareness HMIs;

    [03:18] Self-documenting objects; and versioning and diagnostic tools for troubleshooting the application.

    [03:32] Next is the AVEVA Historian. It provides process data historization and alarm and event logging for Application Server.

    [03:41] It exposes the data through SQL Server or an OData (Open Data Protocol) interface, or both.

    [03:50] Historian bridges the gap between a real-time, high-volume plant monitoring environment and an open, flexible business information environment. Historian is tightly coupled with Microsoft SQL Server.

    [04:01] Historian acquires plant data from high-speed I/O servers, DA servers, OI servers, Application Server, and other devices.

    [04:13] It also acquires data from other AVEVA software such as Edge, Plant SCADA, and InTouch HMI. It compresses and stores the data and responds to SQL requests for plant data.

    [04:22] Historian also contains event, alarm summary, configuration, security, backup, and system monitoring information.

    [04:41] Next is the AVEVA Communication Drivers. The drivers are provided to communicate with third-party controllers.

    [04:50] These come in from the OI servers and legacy DA and I/O servers, if needed. System Platform also works with third-party drivers such as OPC servers.

    [05:00] The System Platform clients on the whole access information from System Platform. It is comprised of the following products:

    [05:11] The Supervisory Clients: There are two visualization clients — Operations Management Interface (OMI), based on an object-oriented and rapid design visualization framework;

    [05:22] And InTouch for System Platform, based on the InTouch HMI software. Both components can coexist in the same System Platform solution and share the same content graphics.

    [05:31] They run the operator interface and provide real-time access to Application Server data, alarms, and events.

    [05:41] There are two web clients for both Operations Management Interface and InTouch for System Platform. These are web-based clients as part of the software; it gives users instant access to their supervisory clients and supports several common browsers.

    [05:58] Next is AVEVA Historian Client. The client contains a collection of tools to access the historical data in the Historian.

    [06:08] It includes a feature-rich trend application, a query application that allows the construction of SQL queries through a point-and-click interface, and report generation through add-ons for Microsoft Excel and Word.

    [06:31] Finally, AVEVA Historian Client Web: This is a web-based client as part of Historian. It is the on-premises version of AVEVA Insight.

    [06:39] It gives users instant access to production data in a variety of formats.

    [06:49] It provides an easy-to-use graphical interface for analyzing data, creating charts, and compiling dashboards of related information. Just like the web-based supervisory clients, Historian Client Web supports several common browsers.

    [07:02] Thanks for watching.