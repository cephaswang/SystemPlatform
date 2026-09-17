https://www.youtube.com/watch?v=lE6D4qHUMRA&list=PLJq4rR8tWINyOrvwxbIjRvgTtoyuuEfSz&index=12
Mastering Alarm Latching: AVEVA System Platform 2023 R2 Demo 


生成中文教程，格式 md ，含引用圖片 images 目錄，圖片為依序取得


Discover the latest Alarm Latching capabilities introduced in System Platform 2023 R2! 

This demonstration provides a step-by-step guide on how to effectively use this feature to enhance your system's performance. 

To learn more about System Platform 2023 R2, watch here:    • AVEVA System Platform what's new in 2023 R2




影片 Mastering Alarm Latching: AVEVA System Platform 2023 R2 Demo 的完整字幕內容與時間軸整理如下：

    [00:02] Hello, this is Vern. This is a demo of a new customer-requested feature for System Platform 2023 R2 we call Alarm Latching.

    [00:10] Alarm Latching is used to retain alarms in the EAC (Alarm Control) until a customer explicitly removes them via a dismiss type of action.

    [00:20] Dismissing transitions the alarm to the Acked Returned (Acknowledged Returned) state and thus removes it from the EAC.

    [00:28] Here's an EAC showing both the previously existing states as well as the new latched state.

    [00:38] We'll come back to this momentarily, but let's first see how to enable Alarm Latching.

    [00:50] That is done in IDE by clicking on the Galaxy main menu item, selecting Configure, selecting Galaxy again, clicking on Alarms and Event, and finally clicking on the States tab.

    [01:02] You'll notice in the States tab there is a new backstage configuration item used to enable or disable Alarm Latching.

    [01:12] In this case, it was previously enabled, but when the user checkmarks "Enable Latching" and then saves it, the whole Galaxy will be enabled for Alarm Latching. This includes already existing alarms.

    [01:32] In order to reach the latched state, user must first either acknowledge the alarm or the alarm must return to normal.

    [01:42] It doesn't matter which one comes first, as the alarm will still transition to latched when Alarm Latching is enabled and the alarm transitions through both states.

    [01:50] For dismissing, let's first dismiss the alarm in the simplest way.

    [01:59] In this case, let's select this one by left-clicking, right-clicking, selecting "Dismiss Selected", filling in the comment, clicking OK.

    [02:11] And now it is transitioned back to the Acked Returned state and it is removed from the EAC.

    [02:21] Let's next see how to transition alarms from all the various states through to dismiss.

    [02:27] And remember, there are two ways: Ack first then Return to Normal, or Return to Normal first and then Ack, and then we'll try dismissing using the other method.

    [02:36] So here we see that it's returned to normal and it's an Unacked Returned state, so let's Ack it.

    [02:51] Now it's latched. Here's one that's Acked, let's bring up the Object Viewer and return it to normal.

    [03:03] Here too, we see it's latched. And finally, this last alarm has neither been Acked nor returned to normal.

    [03:13] We'll choose one of those two because they both work to get it to transition to latched. Let's choose Ack Selected.

    [03:28] Guess we should choose it first, shouldn't we?

    [03:38] Let's—yep, and now let's return it to normal and it's latched.

    [03:48] So now let's choose the other way. The other way is you hover over the EAC, you right-click, you'll notice "Dismiss Others".

    [03:58] You'll also notice that "Dismiss Others" has a number of options to choose from.

    [04:09] These options are the same type of options as are presented for Ack Others, Shelf Others, Unshelf Others, Hide Others.

    [04:18] So let's choose the simplest, which is "Dismiss All", enter our demo comment, and voila! All three alarms have transitioned to Acked Returned to Normal state and were removed from the EAC.

    [04:33] Now Alarm Latching retains each of the alarm's value, status, and quality values through both shelving as well as through failovers.

    [04:51] And that's the basics of Alarm Latching. Thank you.