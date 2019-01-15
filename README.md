# Friends
Friends list for Timeline

# Installation and Usage
Currently, it only supports **Timeline**, but if you want you are free to port it to another source. 

Modification of this file is allowed, but redistribution allowed only with appropriate credits.

 

Grab the flash file, **[Friends.swf](https://github.com/Times-0/Friends/raw/master/media1/play/v2/client/Friends.swf)** (from [media1/play/v2/client](https://github.com/Times-0/Friends/tree/master/media1/play/v2/client)) and put in in your client folder in media-server (media1/play/v2/client)

Now, in the same folder, find and open dependencies.json.

Open it with a text editor, and search for the following:
```json
{
	"id": "interface",
	"title": "Interface"
},
```
below that add the following
```json
{
	"id": "Friends",
	"title": "Dote's HTML5 friends list"
},
```

You are done with the client, now it's time to mess up with your play page. Open your play page (which usually lies in play.localhost), ie play/index.html, 

Now you have to edit that file to add the following. Here I want to make sure, any loss of graphics is entirely dependent on the theme you use for your play page, so you have to fix those all by yourself.

 

Go to the `<head>` tag and add the following below it
```html
<link href="css/timeline-friends.css" rel="stylesheet">

<script src="js/jquery-2.1.4.min.js" type="text/javascript"></script>
<script src="https://code.jquery.com/ui/1.12.1/jquery-ui.js"></script>
```

Then, go the bottom of your page, you'll see `</body>`, just above that add the following
```html
<div id="test-list" style="margin-top: 30px;"> <!--Friends list preview!--> <div id="friends-list" class="friends-outer-shadow friends-box-outer" style="left: 305px; top: 36px; display: none;"> <div class="friends-box"> <!--Drag bar--> <div id="f-drag"> <div class="f-drag"> </div> </div> <div id='f-head'> <img class="friend-icon" src='img/friends_icon.png'> <b><p class="friend-icon-text"> Friends <span style="color:#034C8B; font-size:20px;">(<span id="f-count">00</span>)</span></p></b> <div id='f-close'><div class='close-fx'></div></div> </div> <div id="f-loader"> <div class="f-loader"></div> </div> <div id="f-body"> </div> <div class="f-s-pmd-bar" id = "open-f-r" style="position: absolute; top: 444px; z-index: 3;"></div> <div id="f-requests"> <div class="f-s-pmd-bar" id="close-f-r"></div> <div class="f-loader" style="top:-5px;"> <b><p style="font-size: 14px; color: white; top: 60px; position: relative; text-align: left; left: -65px;">Requests are being mashed down</p></b> </div> <div class='f-s-request'> </div> </div> <div id="f-search-box"> <div class="f-s-pmd-bar"></div> <div class="f-loader" style="display: none; top:-5px;"> <b><p style="font-size: 14px; color: white; top: 60px; position: relative; text-align: left; left: -5px;">Searching</p></b> </div> <div class='f-s-result'> <div class="f-search-result-box"> </div> </div> </div> <div id="f-search"> <input class="f-search" id="f-search-input" maxlength="12" placeholder="Enter nickname to search"> <div class="f-search-button"><b style="position: relative;top: 1px;">Find</b></div> </div> </div> </div> </div> 

<script src="js/friends-timeline.js"></script>
<script type="text/javascript">
$(document).ready( function () {
	$.Timeline.Friends.clientSelector = "#club_penguin"; // change this in all JS file and here if your swf object id is not 'club_penguin'
}
</script>
``` 

That's it you are now set, now download files from **[html](https://github.com/Times-0/Friends/tree/master/html)** folder. Place it in your play directory. (ie, play/, where play.localhost is directed to)

Thats it, client is set. Grab the latest Timeline and enjoy your list!
