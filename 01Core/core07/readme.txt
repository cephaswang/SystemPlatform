https://www.youtube.com/watch?v=TItqvmCSwu8&list=PLJq4rR8tWINyOrvwxbIjRvgTtoyuuEfSz&index=7
AVEVA Historian to CONNECT Agent

生成中文教程，格式 md ，含引用圖片 images 目錄，圖片為依序取得


In this demo, see how the new AVEVA Historian Agent makes it simple to stream process, alarm, and event history from your existing on-premise AVEVA Historian to the cloud-based AVEVA CONNECT platform—no upgrade required. Whether you’re managing legacy deployments or exploring hybrid industrial data strategies, this agent makes your transition to the cloud seamless.


影片 AVEVA Historian to CONNECT Agent 的完整字幕內容與時間軸整理如下：

    [00:00] Welcome to this demo where we'll walk through core functionalities of Historian Agent and performing data backfill in just a few simple steps.
    [00:06] Let's begin by logging into the agent. Enter your CONNECT Data Services credentials provided by AVEVA and select the account where your namespace is available.
    [00:13] After successful login, you can see Configure button is enabled and a few other pages—Configuration and Backfill pages—are also enabled.
    [00:20] Here we can see Backfill page only works when publishing status is active.
    [00:28] So let me start off with configuration by clicking on Configure button to proceed with namespace and tags configuration.
    [00:36] Select the namespace where you want all the tags to be replicated.
    [00:41] And at the pick tags page, it's optional to add prefix or suffix to distinguish the tags accordingly and proceed with the tag selection.
    [00:48] User can select as many tags as needed, either by selecting all or using filter.
    [00:55] Once required tags are under selected tags list, hit Save and Next at the pick tags page.
    [01:01] Once you are at the homepage, you will observe status service configuration and Start Publishing button is enabled.
    [01:09] Hit on Start Publishing to replicate the tags to CONNECT Data Services.
    [01:15] Once all the required services are up and running, you will see the status message turns to "Publishing in Progress" and you can see all the services which are running.
    [01:21] At this point, let's verify on CONNECT Data Services to see if the tags are available and data is being replicated.
    [01:27] Great, all the four tags are available. And finally, let's also look at the data.
    [01:37] Perfect, looks like data is also being replicated properly to the CONNECT Data Services.
    [01:43] Now it's time to look at the Backfill page. Since publishing is active, Backfill page is enabled, and we can input start and end time interval to backfill the data for the selected tags.
    [01:51] Let's start with a basic test by selecting 2 to 3 days of backfill and start the job.
    [01:56] But before starting backfill, let's walk through the past dates where we can see the data is not available on CDS for any of the replicated tag.
    [02:06] Let's start off by hitting the Start button.
    [02:13] Navigate to homepage to see the sync values updating per second and total sync queue items pending.
    [02:21] Once sync queue items reaches to zero, check the replication job is completed successfully.
    [02:28] Finally, let's take a quick look on CDS to see if the data is available for the backfilled dates.
    [02:36] Looks good for the selected dates. To confirm, let's also check a date outside our backfill range. There should be no other data available.
    [02:43] Similarly for other tags as well.
    [02:49] Successful. Finally, let's also see if we can cancel backfill job.
    [02:56] Start by selecting a few time intervals and hit Cancel when decided.
    [03:04] Once Cancel button is selected, you see an error message saying "Backfill canceled" and also see the result is canceled.
    [03:11] Finally, let's confirm if backfill is processed to CDS.
    [03:19] Filter by selecting the date range and see if the data is backfilled. We are seeing data for 2 days. It's because backfill job is canceled after 20% of the job is completed in which it processed two history blocks.
    [03:26] Same for all the four tags.
    [03:30] Let's close the session by taking a quick look at the backfill history text file where it resides all the backfill jobs performed.
    [03:35] Since we performed two jobs, one job ID shows status as "Succeeded" and another job ID shows the status as "Canceled".