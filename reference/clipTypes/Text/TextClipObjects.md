<h1>Text Clip Objects</h1>
<p class="hcp1">Text</p>
<p class="hcp2">Displays formatted text to the screen. Using 
 the format option you can specify how the text is displayed. This is helpful 
 if you want to specify text that won't change and then allow dynamic input 
 of text through the clip. So in the template you might specify the following 
 &quot;Next seminar is starting in {0}&quot; and then in each clip that 
 you create you input the location text &quot;downstairs hall&quot;.</p>
<p class="hcp2">Or you just want to title the text &quot;Destination: 
 {0}&quot; and each clip has the destination &quot;Hatton Cross&quot;, 
 &quot;Charing Cross&quot; etc.</p>
<p class="hcp2">&#160;</p>
<p class="hcp1"><a name="Date_and_Time"></a>Date 
 and Time</p>
<p class="hcp2">Using the Date/Time object you can display 
 the current date and time on the screen.</p>
<p class="hcp2">The format of the time and date is specified 
 using the standard date and time formatting code. Here are some examples.</p>
<table cellspacing="0" border="1" class="hcp3">
	<col>
	<col>
	<tr>
		<td>h:mm:ss</td>
		<td>Time with seconds</td>
	</tr>
	<tr>
		<td>h:mm</td>
		<td>Time without seconds</td>
	</tr>
	<tr>
		<td>dd/MM/yyyy</td>
		<td>English date format</td>
	</tr>
	<tr>
		<td>MM/dd/yyyy</td>
		<td>American date format</td>
	</tr>
	<tr>
		<td>dd/MM/yyyy h:mm</td>
		<td>Date and time together<br>
		</td>
	</tr>
	<tr>
		<td>The time is h:mm</td>
		<td>The time with static text.</td>
	</tr>
	<tr>
		<td>dddd</td>
		<td>Day of the week e.g. Monday</td>
	</tr>
	<tr>
		<td>dd MMMM</td>
		<td>Full month with date e.g. 1st January</td>
	</tr>
</table>
<p class="hcp4">&#160;</p>
<p class="hcp1">Image</p>
<p class="hcp2">The image object allows you to insert images 
 and logos into your text template to add extra visual flair to the text 
 clip.</p>
<p class="hcp2">Once you add the image object, select the 
 format tab from the menu and click Browse to locate the image file to 
 add. The image can be resized and moved like any other text object.</p>
<p class="hcp5"><img alt="" src="../../../images/NewItem33.png" border="0" class="hcp6"></p>
<p class="hcp2">&#160;</p>
<p class="hcp1">Countdown</p>
<p class="hcp2">You can use this object to display a countdown 
 from a specific number.</p>
<p class="hcp2">Once you add the countdown object it will 
 display &quot;[Invalid Countdown]&quot; until you configure the text to 
 a start number in the clip's settings.</p>
<p class="hcp5"><img alt="" src="../../../images/NewItem34.png" border="0" class="hcp6"></p>
<p class="hcp5">&#160;</p>
<p class="hcp5"><img alt="" src="../../../images/NewItem35.png" border="0" class="hcp6"></p>
<p class="hcp2">Once you have set the start number, it will 
 count down from this value each time you play the clip.</p>
<p class="hcp2"><a href="../../../tutorials/WorkingWithClips/CreatingACountdown.md">Click 
 here for a step-by-step guide on creating a Countdown clip</a>.</p>
<p class="hcp2">&#160;</p>
<p class="hcp1">Countdown Clock</p>
<p class="hcp2">Similar to the Countdown, this object also 
 allows you to display a countdown on the screen. The difference is that 
 with this object, you can specify an end date or time to countdown to. 
 Once you have set the target time, the clip will continuously show a countdown 
 to this time on the screen when the text clip is playing.</p>
<p class="hcp2">When you add the Countdown Clock it will 
 display [Invalid Time Format!] till you set the target time. The target 
 time is set through the clips edit panel.</p>
<p class="hcp5"><img alt="" src="../../../images/NewItem36.png" border="0" class="hcp6"></p>
<p class="hcp2">&#160;</p>
<p class="hcp5"><img alt="" src="../../../images/NewItem37.png" border="0" class="hcp6"></p>
<p class="hcp2">You can change the format of the countdown 
 from the template editor by selecting format.</p>
<p class="hcp2">Please see the <a href="#Date_and_Time">Date 
 and Time</a> object settings for details on the date and time format.</p>
<p class="hcp5"><img alt="" src="../../../images/NewItem38.png" border="0" class="hcp6"></p>
<p class="hcp2">&#160;</p>
<p class="hcp1">Schedule</p>
<p class="hcp2">Using this object you can display the current 
 clips scheduled for playback in a text clip. This is a great feature when 
 running an automated TV station and you want to display the next programs 
 to be shown during a break. The layout and format of the schedule items 
 is fully customizable. The title and description for each item can be 
 set in the scheduler.</p>
<p class="hcp5"><img alt="" src="../../../images/NewItem40.png" border="0" class="hcp6"></p>
<p class="hcp2">Once you add the schedule object to your 
 template you can use the Format tab to configure how each item is displayed 
 and what items are displayed.</p>
<p class="hcp5"><img alt="" src="../../../images/NewItem39.png" border="0" class="hcp6"></p>
<p class="hcp5">&#160;</p>
<table cellspacing="0" border="1" class="hcp3">
	<col>
	<col>
	<tr>
		<td class="hcp7"><span class="hcp8">Date 
		 Format</span></td>
		<td class="hcp7">Determines the format to display 
		 the start time of each scheduled clip. Please see the <a href="#Date_and_Time">Date/Time</a> 
		 object for details on how to specify the format.</td>
	</tr>
	<tr>
		<td class="hcp7"><span class="hcp8">Entry 
		 Format</span></td>
		<td class="hcp7">Specifies how each scheduled item 
		 is displayed in the list. Special tags allow you to insert information 
		 from the scheduled item. 
		<p class="hcp4">{date} - the start date for the scheduled 
		 item.</p>
		<p class="hcp4">{time} - the start time for the scheduled 
		 item.</p>
		<p class="hcp4">{name} - the clip name.</p>
		<p class="hcp4">{title} - a special field set through 
		 the scheduler for each scheduled item. This is initially blank 
		 for each clip and you must set through the scheduler. You can 
		 use this to display a different title from the clip name.</p>
		<p class="hcp4">{description} - a special field set 
		 for each clip through the scheduler.</p>
		<p style="margin-left: 0px; background-color: #c0c0c0;">When you 
		 use the {title} or {description} tags you need to ensure you set 
		 the text through the scheduler. You can open the scheduler by 
		 clicking on the clock icon in the main dashboard. The scheduled 
		 items list will open and contains two columns for the title and 
		 description. You can enter your text here.<br>
		<br>
		<img alt="" src="../../../images/NewItem43.png" border="0" class="hcp6"><br>
		<br>
		The default is to hide scheduled items from display in the scheduled 
		 object. This ensures that while you add scheduled items they are 
		 not visible. To show the item and display them in the text schedule 
		 you need to open the scheduler and clear &quot;Hide&quot; for 
		 each scheduled clip. Without doing this, the schedule will appear 
		 blank.<br>
		<br>
		<img alt="" src="../../../images/NewItem41.png" border="0" class="hcp6"><br>
		<br>
		<span class="rvts6">The following shows a template which has a 
		 title with a schedule item.</span><br>
		<br>
		<img alt="" src="../../../images/NewItem44.png" border="0" class="hcp6"></p>
		<p class="hcp4">You can also add a limited set of 
		 formatting.</p>
		<p class="hcp4">[t] - add a tab</p>
		<p class="hcp4">[nl] - new line</p></td>
	</tr>
	<tr>
		<td class="hcp7"><span class="hcp8">Max 
		 Display Items</span></td>
		<td class="hcp7">The number of scheduled items 
		 to display at a time.</td>
	</tr>
	<tr>
		<td class="hcp7"><span class="hcp8">Time 
		 Period</span></td>
		<td class="hcp7">The amount of time to look ahead 
		 in the schedule for items to display. setting to zero will display 
		 all scheduled items.</td>
	</tr>
	<tr>
		<td class="hcp7"><span class="hcp8">End 
		 At Midnight</span></td>
		<td class="hcp7">Only displays scheduled items 
		 till midnight of the day specified in the Time Period property.</td>
	</tr>
</table>
<p class="hcp4">&#160;</p>
<p class="hcp1">Text File</p>
<p class="hcp2">Using the text file object you can display 
 the contents of a text file within the text clip. All the text from the 
 file is displayed using the template's formatting.</p>
<p class="hcp5"><img alt="" src="../../../images/NewItem45.png" border="0" class="hcp6"></p>
<p class="hcp2">Once you add the Text File object you then 
 need to select the text file to use. This is done by clicking the format 
 tab and selecting Browse. You can now select the file to display. The 
 text file can be created using applications such as Windows Notepad. Once 
 you select the file it will show you the text that is going to be displayed.</p>
<p class="hcp2">The text file is constantly being monitored 
 for changes even when the clip is live so any changes you save to the 
 file will be immediately updated on the screen. This can be helpful if 
 you want to update the text over a network as you can update the file 
 remotely to change the text being displayed on the screen.</p>
