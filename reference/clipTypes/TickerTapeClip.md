<h1><img src="../../images/TickerTapeIcon.png" alt="" style="border: none; margin-left: 0px; 
		 margin-right: 0px; margin-top: 0px; margin-bottom: -6px;" border="0"> 
 Ticker Tape Clip</h1>
<h2>What a Ticker Tape Clip does</h2>
<p>The Ticker Tape clip displays some scrolling text and allows you to 
 specify a list of messages to scroll through. This works in much the same 
 way as a news crawl and presents a scrolling bar of text across the screen.</p>
<p>The messages may be pre-configured by the Screen Monkey operator or 
 an RSS or Atom feed may be used to supply the messages.</p>
<p>&#160;</p>
<h2>How to configure a Ticker Tape Clip</h2>
<p>Click or Right-click an empty slot and choose Ticker Tape. After clicking 
 <span class="hcp2">OK</span> the slot simply shows Ticker 
 Tape. </p>
<p>Right-click the Ticker Tape Clip and choose <span class="hcp2">Edit 
 / Cue</span>.</p>
<p>The <span class="hcp2">Cue Tickertape</span> dialog is 
 presented.</p>
<p style="margin-left: 24px;"><img src="../../images/TickerTapeDialog.png" alt="" border="0" class="hcp3"></p>
<p>There are a number of configuration options to choose here.</p>
<p>Type the text you wish to present in the <span class="hcp2">Enter 
 message text</span> field. Most of the other options should be self-explanatory, 
 such as Font, Font Color, etc. But there are some options that do warrant 
 a bit of explanation.</p>
<table style="margin-left: 24px; border-collapse: separate; border-collapse: separate;" 
		 cellspacing="0" border="1">
	<col>
	<col>
	<tr>
		<td colspan="2" bgcolor="#C0C0C0"><span class="hcp2">Single 
		 Message Tab</span></td>
		
	</tr>
	<tr>
		<td colspan="2" bgcolor="#C0C0C0"><span class="hcp2">Position</span></td>
		
	</tr>
	<tr>
		<td><span class="hcp2">Offset (pixels)</span></td>
		<td>This value allows you to control the vertical position of the 
		 Ticker. 
		<br>&#160;</td>
	</tr>
	<tr>
		<td><span class="hcp2">Relative to</span></td>
		<td>This allows you to choose whether the Ticker appears at the 
		 top of the display or at the bottom. 
		<br>&#160;</td>
	</tr>
	<tr>
		<td colspan="2" bgcolor="#C0C0C0"><span class="hcp2">Background</span></td>
		
	</tr>
	<tr>
		<td class="hcp4"><span class="hcp2">Type</span></td>
		<td><span class="hcp2">None</span> 
		<br>No background appears and only text scrolls across 
		 the display 
		<br>&#160; 
		<br><img src="../../images/TickerExample1.png" alt="" border="0" class="hcp3"> 
		<br>&#160; 
		<br><span class="hcp2">Box</span> 
		<br>A background color surrounds only the message 
		 and both scroll across the display. 
		<br>&#160; 
		<br><img src="../../images/TickerExample2.png" alt="" border="0" class="hcp3"> 
		<br>&#160; 
		<br><span class="hcp2">Banner</span> 
		 
		<br>A background color appears only when the message 
		 is scrolling. Once the message finishes scrolling, the background 
		 disappears until the message is presented again. At that time 
		 the banner will re-appear. 
		<br>&#160; 
		<br><img src="../../images/TickerExample3.png" alt="" border="0" class="hcp3"> 
		<br>&#160; 
		<br><span class="hcp2">Banner Always</span> 
		 
		<br>A background color appears whether the message 
		 is present or not. 
		<br>&#160;</td>
	</tr>
	<tr>
		<td class="hcp4"><span class="hcp2">Color</span></td>
		<td>Configures the color used for the background. 
		<br>&#160;</td>
	</tr>
	<tr>
		<td class="hcp4"><span class="hcp2">Opacity</span></td>
		<td>Configures the opacity of the background color. 
		<br>Values are 0-255 with 0 meaning transparent and 
		 255 meaning totally opaque. 
		<br>&#160;</td>
	</tr>
	<tr>
		<td colspan="2" bgcolor="#C0C0C0"><span class="hcp2">Message 
		 Queue tab</span></td>
		
	</tr>
	<tr>
		<td colspan="2">This tab allows you to store several messages. 
		 For example, perhaps you wish to store the following messages 
		 so that you might be able to recall them as needed: <br>
		<br>
		
		<ul type="disc">
			<li>Please silence your cell phones</li>
			<li>Please remember to complete your keynote evaluations</li>
			<li>Please hold all questions until the end of the discussion</li>
			<li>Please begin forming lines at the microphones for our Q&amp;A</li>
		</ul>
		&#160;
		<br>Type your messages into the <span class="hcp2">New 
		 message</span> field and press <span class="hcp2">Enter</span> 
		 to add it to the queue. To rearrange messages in the queue, click 
		 and drag them to their new location. To delete them, click to 
		 select and press the <span class="hcp2">Delete</span> 
		 key. 
		<br>&#160;</td>
		
	</tr>
	<tr>
		<td colspan="2" bgcolor="#C0C0C0"><span class="hcp2">RSS 
		 Feed tab</span></td>
		
	</tr>
	<tr>
		<td class="hcp4"><span class="hcp2">Feed 
		 URL</span></td>
		<td>Type the URL used for the feed into this field 
		<br>&#160;</td>
	</tr>
	<tr>
		<td class="hcp4"><span class="hcp2">Feed 
		 Type</span></td>
		<td>Choose Detect Automatically if you would like Screen Monkey 
		 to try and detect the type of feed for you. Otherwise, choose 
		 the type of feed. (RSS or Atom) 
		<br>&#160;</td>
	</tr>
	<tr>
		<td class="hcp4"><span class="hcp2">Format 
		 String</span></td>
		<td>What is used here determines the way the feed appears when 
		 presented. Click the links to the right to add these to the field. 
		 
		<br>&#160;</td>
	</tr>
	<tr>
		<td class="hcp4"><span class="hcp2">Refresh 
		 Every</span></td>
		<td>This determines the interval at which Screen Monkey will check 
		 the Feed URL for any message updates. 
		<br>&#160;</td>
	</tr>
	<tr>
		<td colspan="2" bgcolor="#C0C0C0" class="hcp4"><span class="hcp2">Bottom of dialog</span></td>
		
	</tr>
	<tr>
		<td class="hcp4"><span class="hcp2">Automatically 
		 advance through messages</span></td>
		<td>If you have added two or more messages to the Message Queue, 
		 the messages will be cycled through the list. 
		<br>If a single message has been used on the Single 
		 Message tab, it is looped and plays over and over until stopped.</td>
	</tr>
	<tr>
		<td class="hcp4"><span class="hcp2">Delay</span></td>
		<td>After each message leaves the screen, the amount of time specified 
		 here will elapse before the next message is presented or before 
		 the message is repeated (if being looped).</td>
	</tr>
</table>
<p>&#160;</p>
<table cellspacing="0" border="1" class="hcp5">
	<col>
	<col>
	<tr>
		<td><img src="../../images/Tipimage.png" alt="" border="0" class="hcp3"></td>
		<td>More than one Ticker Tape clip may be configured. the settings 
		 are independent and changes to one clip don't affect others. For 
		 example, perhaps you want some Ticker Tape messages to have a 
		 bright red background while others have a bright yellow background.</td>
	</tr>
</table>
<p>&#160;</p>
<h2>How to use a Ticker Tape Clip during a show</h2>
<p>Click the Ticker Tape Clip to begin playing. If you have configured 
 multiple messages, right-click and choose Edit / Cue or click the middle 
 mouse button to open the Cue Tickertape dialog. From there you may choose 
 the message to be used by double-clicking the message. You must also click 
 <span class="hcp2">Apply</span> to set it.</p>
<p>If a check mark is cleared in the Messages queue, the clip will play 
 the message followed by Screen Monkey removing the message.</p>
<table cellspacing="0" border="1" class="hcp5">
	<col>
	<col>
	<tr>
		<td><img src="../../images/Tipimage.png" alt="" border="0" class="hcp3"></td>
		<td>If your Ticker Tape is pointing to an RSS feed, you may right-click 
		 the Ticker Tape Clip in the Main Dashboard and choose <span class="hcp2">Update 
		 RSS Feed now</span> to refresh. This saves you from being forced 
		 to open the Cue dialog.</td>
	</tr>
</table>
<p>&#160;</p>
<h2 class="rvps3">Enhancement History</h2>
<p><a href="../../releases/Version_3.md#Ticker_Tape_Clip">Version 3 - 
 25th September 2007: Ticker Tape Clip added and announced</a></p>
<p><a href="../../releases/Version_3_1.md#Ticker_Tape_Setup_Opens_on_New_Clip">Version 
 3.1 - 16th March 2008: Ticker Tape Setup Opens on New Clip</a></p>
<p><a href="../../releases/Version_3_3.md#Ticker_Tape_Settings">Version 
 3.3 - 1st August 2009: Ticker Tape Settings</a></p>
