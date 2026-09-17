https://www.youtube.com/watch?v=jTx2tV_BRUI&list=PLJq4rR8tWINyOrvwxbIjRvgTtoyuuEfSz&index=15

Demo of importing and converting of SVG (Scalable Vector Graphics) to AVEVA Industrial Graphics (AIG) into InTouch HMI.  This video will show you how to bring them into Industrial Graphics, as layers and groups and then animate them as AIG.Hear about why AVEVA supports SVG, and what is supported and some of the technical tips and tricks.

生成中文教程，格式 md ，含引用圖片 images 目錄，圖片為依序取得


Download InTouch HMI:
https://www.aveva.com/en/products/intouch-hmi/

Learn more by short video bytes:
https://learningacademy.aveva.com/pages/intouch-hmi-learning-bytes

影片 SVG image Import and conversion into AVEVA Industrial Graphics 的完整字幕內容與時間軸整理如下：

    [00:05] My name is Scott Cortier and I have a quick video for you today highlighting a new SVG import tool.

    [00:12] This SVG import will bring in SVG Graphics (Scalable Vector Graphics) into the AVEVA Industrial Graphics editor in AVEVA InTouch HMI 2023 Patch 1 and the upcoming AVEVA Edge 2023 release due mid-2023.

    [00:35] What is this? So first of all, it's going to convert from SVG Graphics to Native Industrial Graphics,

    [00:43] and this will allow you to use third-party vector graphics applications such as Adobe Illustrator, Figma, Vecteezy, Inkscape...

    [00:53] and by the way, these are not sold or supported by AVEVA, they are third-party tools, and I'm going to quickly demonstrate Inkscape here today.

    [01:01] So why are we doing this? Well, we've had some customer requests to do this, but it's an important step forward in allowing graphics—so these will be vector graphics, they're basically defined by math as opposed to individual pixels,

    [01:16] so vector versus raster, and they'll be infinitely scalable without loss, you won't have pixelated images if you scale them up or scale them down.

    [01:24] And why are we doing this? Well, often system integrators and a lot of our customers will hire a third-party design team to create user interface elements such as dashboard layouts,

    [01:41] and so again, you can use the third-party vector graphics applications that I mentioned above for things like being able to very clearly define shapes and sizes, specific RGB values,

    [02:01] and again, having these third-party design teams do these as opposed to somebody who's familiar with these industrial applications such as InTouch HMI or AVEVA Edge.

    [02:09] So what I'm going to do is I'm going to show you here—this is Inkscape, and what I've done is I created a new image first of all.

    [02:21] And one of the things that you have to be aware of in Inkscape—I don't know if this is a specific SVG naming or if this is only Inkscape—but you have to set up the ViewBox.

    [02:35] And to set up the ViewBox and your height and width, in this case, I've done 1920x1080.

    [02:41] The first time through this, I did this with the default front page here as 1920x1080, but when I brought it in, the ViewBox was set to something smaller and it scaled. And again, this is all based on math, so it wasn't exactly right.

    [02:53] So what I did is I changed the display units here to pixels, then set up the ViewBox to match the 1920x1080, and that imports just fine.

    [02:59] So again, this is on the Document Properties, and I'm assuming that there's other similar tools within the other graphics editors as well.

    [03:11] What I wanted to show you here is I've got the Layer Pane open, and I've defined, for example, and I've given a name here—and I'll show you why I've done this in a minute—

    [03:18] but here's the large right pane, here's the bottom left pane, and then what I did is I made these three little individual panes here out of two separate rounded rectangles,

    [03:31] and I've named them and grouped them. So I've named them "right pane", and this is made up of two different rectangles: a purple one and a white one,

    [03:40] and I've done the same thing for the right, the middle, and the left pane, and then I've grouped them all together, so you can see that grouping in there when we bring those into Industrial Graphics.

    [03:46] So another thing that needs to be pointed out: natively when you save within Inkscape, it tries to add some additional information into the SVG file.

    [03:56] So by default, you are saving as an "Inkscape SVG", and I'm not exactly sure what that additional information is, but I always make sure that when I do this, I save as a "Plain SVG".

    [04:10] There may be some other supported types here, like optimized, I'm not sure, but I do know that Plain works, so I've been saving those as Plain SVGs, which you'll see in a minute.

    [04:23] When I replace it, it prompted me to replace that. So now let's go over to our Industrial Graphics editor.

    [04:28] And if I bring this up here, a couple of things to note: you can in the Industrial Graphics editor import an SVG, and this is going to then give me the ability to bring in SVGs here and convert those into Industrial Graphics,

    [04:50] but I'm going to show you a neat little shortcut here.

    [04:58] I'm just going to have the file browser open here, and I'm just going to drag and drop the file onto my Industrial Graphics editor.

    [05:05] And you can see here that it brought that in all in one fell swoop, just nice and easy.

    [05:11] And again, going back to what I had shown before in Inkscape, you can see here that it has the three panes: the bottom left, the bottom right,

    [05:17] and then as I expand this—and again, these are now Industrial Graphics objects—so if I double click on them, I can add normal animations and visualization things to these.

    [05:24] So just be aware that it is now Industrial Graphics objects.

    [05:35] Just some things to note: where we have matching objects from SVG objects, the entire spec of SVG is not supported.

    [05:52] This is our first pass at this, so we have imported, you know, things like rectangles, some shapes, circles, ellipses, and things of that nature,

    [06:00] but all graphics objects in SVG—the entire specification—is not supported. Clipping and masking is not supported,

    [06:07] but you can see to get some nice simple design elements in, we have this, and we will be enhancing the capabilities in upcoming versions.

    [06:14] So stay tuned to that. Just wanted to give you that little tidbit and make sure you're aware of this.

    [06:21] Thanks for watching, and have a great day.
