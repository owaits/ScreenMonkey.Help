<h1><a name="MiniTOCBookMark1"></a>Version 3.7</h1>
<ul style="text-align:left; font-family:Arial;font-size:12pt;font-weight: normal;font-style: normal;text-decoration: none;"  >
 <li><a href="#MiniTOCBookMark2" class="hcp2">October 2011: Version 3.7</a>
</li>
 <li><a href="#MiniTOCBookMark3" class="hcp2">December 2011: Version 3.7</a>
</li>
 <li><a href="#MiniTOCBookMark4" class="hcp2">January 2012: Version 3.7</a>
</li>
 <li><a href="#MiniTOCBookMark5" class="hcp2">February 2012: Version 3.7</a>
</li>
 <li><a href="#MiniTOCBookMark6" class="hcp2">March 2012: Version 3.7</a>
</li>
 <li><a href="#MiniTOCBookMark7" class="hcp2">July 2012: Version 3.7</a>
</li>
</ul>
<h3><a name="MiniTOCBookMark2"></a>October 2011: Version 3.7</h3>
<ol type="1">
	<li class="hcp3"><p class="hcp4"><a name="StreamingACN"></a>Streaming 
	 <a href="../Glossary.md#ACN">ACN</a> (Pro Feature)<br>
	<br>
	<span class="hcp5">Added support for streaming ACN 
	 between a lighting console or other control device and Screen Monkey. 
	 This allows <a href="javascript:void(0);" id="a2" onmouseover="if (parseInt(navigator.appVersion) >= 4 &amp;&amp; typeof(BSPSPopupOnMouseOver) == 'function') BSPSPopupOnMouseOver(event);" class="BSSCPopup" onclick="BSSCPopup('../Glossary.md#DMX',400,120);return false;">DMX</a></span><span class="hcp5"> 
	 to be sent over a network. For you to use this, your lighting console 
	 must also support Streaming ACN. The control channels follow the standard 
	 DMX control channels as detailed in the Screen Monkey manual.</span><br>
	<br>
	<img alt="" src="../images/NewItem21.png" width="719" height="550" border="0" class="hcp6"><br>
	<br>
	<span class="hcp5">You can configure the Streaming 
	 ACN universe from the ACN tab in the <a href="../Reference/Setup/Settings/ACN.md" class="hcp7">settings</a>. 
	 You will also see other options here such as an indicator to tell 
	 you if you are receiving DMX and the ability to disable certain layers 
	 from Streaming ACN control.</span></p></li>
	<li class="hcp3"><p class="hcp4"><a name="RDM"></a>RDM 
	 (Pro Feature)<br>
	<br>
	<span class="hcp5"><a href="javascript:void(0);" id="a1" onmouseover="if (parseInt(navigator.appVersion) >= 4 &amp;&amp; typeof(BSPSPopupOnMouseOver) == 'function') BSPSPopupOnMouseOver(event);" class="BSSCPopup" onclick="BSSCPopup('../Glossary.md#RDM',400,275);return false;">RDM</a> was developed 
	 by the lighting industry to allow discovery and control of lighting 
	 fixtures over DMX. It is also applicable to Screen Monkey as it allows 
	 lighting consoles to discover Screen Monkey and tell what universe 
	 it is receiving DMX on and what personality to use to control the 
	 software. The RDM support is currently only over ArtNet but will be 
	 added to ACN soon.<br>
	<br>
	With RDM support you will be able to use features such as auto address 
	 and identify from lighting consoles that also support RDM. This simplifies 
	 the process of patching and configuring with a lighting console.<br>
	<br>
	The following RDM messages are supported along with mandatory messages.</span><br>
	<br>
	Device Information</p></li>
</ol>
<ol start="3" type="1">
	<ul type="disc">
		<li><p>Device Model Description</p></li>
		<li><p>Manufacturer Label</p></li>
		<li><p>Software Version Label</p></li>
		<li><p>Device Model Description</p></li>
		<li><p>Dmx Personality</p></li>
		<li><p>Dmx Personality Description</p></li>
		<li><p>Device Hours</p></li>
		<li><p>Lamp Hours</p></li>
		<li><p>Lamp Strikes Hours</p></li>
	</ul>
	<li class="hcp3"><p><a name="ClearPageBookmarksOnNewShow"></a>Clear 
	 <a href="../tutorials/WorkingWithClips/OrganizingClips.md">Page 
	 Bookmarks</a> on New Show<br>
	<br>
	<span class="hcp5">The page bookmarks are now cleared 
	 when you start a new show. Before the bookmarks would be left from 
	 the previous show.</span></p></li>
	<li class="hcp3"><p><a name="FixedPageSizes"></a>Fixed 
	 Page Sizes<br>
	<br>
	<span class="hcp5">A new <a href="../Reference/Setup/Settings/General.md">user 
	 setting</a> allows you to configure fixed page sizes. This can make 
	 it simpler when laying out your show as it ensures that the first 
	 item on page 2 is always the first item. Previously, the page sizes 
	 would change to fit the Window size. If the items on a single page 
	 exceed the number that can be displayed, a scroll bar appears.</span><br>
	<br>
	<img alt="" src="../images/NewItem22.png" border="0" class="hcp6"><br>
	<br>
	<span class="hcp5">From the settings you can select 
	 a number of different page sizes. If you are controlling via DMX then 
	 the page size is automatically set to 255 clips per page to make it 
	 easier to control.</span></p></li>
	<li class="hcp3"><p><a name="SMNetClipControl"></a>SmNet 
	 Clip Control (Pro Feature)<br>
	<br>
	<span class="hcp5">Added much greater support to SmNet 
	 for control of your clips over a network. The most notable change 
	 is the addition of clip events that notify a remote client when a 
	 clip is played or deleted as well as other state notifications.<br>
	<br>
	The networking interfaces have been condensed into the ScreenMonkey.Net.dll 
	 and all you have to do to control Screen Monkey over a network is 
	 reference this assembly. For more information about developing SmNet 
	 applications please visit http://screenmonkey.codeplex.com.<br>
	<br>
	</span>Other SmNet additions in this version:</p></li>
	<ul type="disc">
		<li class="hcp8"><p>Layer Opacity Control</p></li>
		<li class="hcp8"><p>Layer Volume Control</p></li>
		<li class="hcp8"><p>Bookmarks and Pages</p></li>
		<li class="hcp8"><p>Clip Play State</p></li>
		<li class="hcp8"><p>Load SMX and SMZ files over 
		 the network</p></li>
	</ul>
</ol>
<p style="margin-left: 48px;"><a href="#"><img src="../images/120.bmp" alt="" border="0" class="hcp9"> Back to 
 top</a></p>
<h3>&#160;</h3>
<h3><a name="MiniTOCBookMark3"></a>December 2011: Version 3.7</h3>
<ol type="1">
	<li class="hcp3"><p class="hcp10"><a name="MIDIMacro"></a>MIDI 
	 Macro (Pro Feature)<br>
	<br>
	<span class="hcp5">The MIDI macro allows you to send 
	 MIDI commands from Screen Monkey for the control of other devices.</span><br>
	<br>
	<img alt="" src="../images/NewItem23.png" border="0" class="hcp6"><br>
	<br>
	<span class="hcp5">Using the macro you can schedule 
	 or link macro commands in your show to give greater integration between 
	 your video and other devices.</span><br>
	<br>
	<img alt="" src="../images/NewItem24.png" border="0" class="hcp6"><br>
	<br>
	<span class="hcp5">Included is support for all standard 
	 MIDI commands and any number of MIDI devices can be connected.</span></p></li>
	<li class="hcp3"><p class="hcp10"><a name="SongClipHighCPU"></a><a 
	 href="../reference/clipTypes/Song/SongClip.md">Song Clip</a> High 
	 CPU<br>
	<br>
	<span class="hcp5">Fixed bug where song clips with 
	 no transition would require a large amount of CPU to display.</span><br>
	<br>
	<a href="#"><img src="../images/120.bmp" alt="" border="0" class="hcp9"> <span class="hcp5">Back 
	 to top</span></a></p></li>
</ol>
<h3>&#160;</h3>
<h3><a name="MiniTOCBookMark4"></a>January 2012: Version 3.7</h3>
<ol type="1">
	<li class="hcp3"><p class="hcp10"><a name="SelectNetworkAdapterForARTNetACN"></a>Select 
	 Network Adapter (Pro Feature)<br>
	<br>
	<span class="hcp5">You can now select which network 
	 adapter is used for ArtNet and ACN traffic.</span><br>
	<br>
	<img alt="" src="../images/NewItem25.png" border="0" class="hcp6"><br>
	<br>
	<span class="hcp5">Go to settings and select either 
	 the ArtNet or ACN tab. Click the Network tab and click Select to change 
	 the adapter. The currently selected adapter will be displayed.</span></p></li>
	<li class="hcp3"><p class="hcp10"><a name="GrassValleyTritonRouterMacro"></a>Grass 
	 Valley Triton Router Macro (Pro Feature)<br>
	<br>
	<span class="hcp5">The Triton Routing Macro allows 
	 you to control any Grass Valley Triton router through the Screen Monkey 
	 software. Using the macro you can configure the audio and video cross-points 
	 separately or together. This allows you to incorporate video switching 
	 into any Screen Monkey show.<br>
	</span><br>
	<img alt="" src="../images/NewItem26.png" border="0" class="hcp6"><br>
	<br>
	<span class="hcp5">The router must be connected via 
	 a RS232 port and any number of connected routers is supported.<br>
	</span><br>
	<img alt="" src="../images/NewItem27.png" width="614" height="442" border="0" class="hcp6"><br>
	<br>
	<span class="hcp5">As well as controlling the router, 
	 the macro also supports feedback from the router and will indicate 
	 the selected cross-points even when changed from the router's hardware 
	 switches.</span></p></li>
	<li class="hcp3"><p class="hcp10"><a name="LightwaveRFMacro"></a>LightwaveRF 
	 Macro (Pro Feature)<br>
	<br>
	<span class="hcp5">Lightwave RF is a home lighting 
	 automation control protocol which allows control of light dimmers, 
	 relays and socket power. Its applications go beyond home use and could 
	 be used for raising and lowering screens or anywhere where control 
	 of low power (13A) devices is required. To use this macro you must 
	 purchased a LightwaveRF Wifi router which connects to your network 
	 with Screen Monkey.</span><br>
	<br>
	<img alt="" src="../images/NewItem28.png" border="0" class="hcp6"><br>
	<br>
	<span class="hcp5">Using this macro you can change 
	 light dimer levels, select pre-configured moods and turn 13A Sockets 
	 On and Off. A relay unit is also available.<br>
	<br>
	Once you add the macro it can be incorporated into your normal Screen 
	 Monkey show. Once your command has been setup you can click on the 
	 &quot;Try Command&quot; button to check that everything is working.<br>
	<br>
	To setup your LightwaveRf devices. please visit the <a href="http://www.lightwaverf.com/manager.php" target="_blank" class="hcp7">LightwaveRF 
	 website</a>.</span><br>
	<br>
	<img alt="" src="../images/NewItem30.png" border="0" class="hcp6"><br>
	</p></li>
	<li class="hcp3"><p class="hcp10"><a name="37TextClipObjects"></a><a 
	 href="../reference/clipTypes/Text/TextClip.md">Text Clip</a> Objects<br>
	<br>
	<span class="hcp5">Your basic text clip function just 
	 got so much better. It now allows you to display a vast array of different 
	 text items on the screen and these can be added to your template along 
	 with other text items to build up an information screen that dynamically 
	 updates. Each text object you add can be styled to give you the precise 
	 layout and look you want. <a href="../reference/clipTypes/Text/TextClipObjects.md" class="hcp7">Click 
	 here</a> for more on the Text Clip Objects.</span></p></li>
	<li class="hcp3"><p class="hcp10"><a name="ScheduleDashboard24HourClock"></a>Schedule 
	 Dashboard 24Hour Clock<br>
	<br>
	<span class="hcp5">The schedule dashboard now shows 
	 a 24 hour clock instead of a 12 hour clock.</span><br>
	<br>
	<img alt="" src="../images/NewItem50.png" border="0" class="hcp6"><br>
	</p></li>
	<li class="hcp3"><p class="hcp10"><a name="ScheduleWaitForBreak"></a>Schedule 
	 Wait For Break<br>
	<br>
	<span class="hcp5">You can now set the scheduler to 
	 wait for a break in the program before running a scheduled item. This 
	 ensures that the scheduler waits for the playing clip to finish before 
	 running the next item. You can choose to enable this through the settings.</span><br>
	<br>
	<img alt="" src="../images/NewItem51.png" border="0" class="hcp6"></p></li>
	<li class="hcp3"><p class="hcp10"><a name="ClipScheduleIndicator"></a>Clip 
	 Schedule Indicator<br>
	<br>
	<span class="hcp5">Displays a click icon in all clips 
	 that are scheduled to play.</span><br>
	<br>
	<img alt="" src="../images/NewItem52.png" border="0" class="hcp6"><br>
	</p></li>
	<li class="hcp3"><p class="hcp10"><a name="37MultipleClipLiinks"></a>Multiple 
	 Clip Links<br>
	<span class="hcp5"><br>
	You can now link a clip to multiple items rather than just a single 
	 clip as before. The default as before is to link to just a single 
	 clip but if you select either &quot;More Options&quot; or the &quot;Link&quot; 
	 option from the clip menu it will allow you to specify additional 
	 links. <a href="../tutorials/WorkingWithClips/LinkingClips.md#Using_Multiple_Clip_Links" class="hcp7">Click here</a> for more on 
	 this feature.</span></p></li>
	<li class="hcp3"><p class="hcp10"><a name="ClipTemplates"></a>Clip 
	 Templates<br>
	<br>
	<span class="hcp5">Using templates you can export any 
	 existing clip as a template to create new clips. The template includes 
	 all clip settings and allows you to quickly and easily duplicate the 
	 clip settings. <a href="../reference/clipTypes/ClipTemplates.md" class="hcp7">Click here</a> for 
	 more on Clip Templates.</span></p></li>
	<li class="hcp3"><p class="hcp10">Links in 
	 Tooltip Text<br>
	<br>
	<span class="hcp5">The clip links are now displayed 
	 in the clip tooltip.</span><br>
	<br>
	<img alt="" src="../images/NewItem57.png" border="0" class="hcp6"></p></li>
	<li class="hcp3"><p class="hcp10"><a name="LiveAudioClip"></a>Live 
	 Audio Clip<br>
	<br>
	<span class="hcp5">You can use the live audio clip 
	 to play audio from any sound card input. This is useful if you want 
	 to automatically switch between live and pre-recorded content or you 
	 want to mix live audio with content from Screen Monkey. <a href="../reference/clipTypes/LiveAudioClip.md" class="hcp7">Click here</a> for more.</span></p></li>
	<li class="hcp3"><p class="hcp10"><a name="MacrosInSpaceClips"></a><a 
	 href="../reference/Macros/Macros.md">Macros</a> in Space 
	 Clips<br>
	<br>
	<span class="hcp5">Macros now work from space clips.</span></p></li>
	<li class="hcp3"><p class="hcp10"><a name="ScheduleClipsFromScheduleDashboard"></a>Schedule 
	 Clips from Schedule Dashboard<br>
	<br>
	<span class="hcp5">Using the schedule dashboard you 
	 can directly add clips using the Add button.</span><br>
	<br>
	<img alt="" src="../images/NewItem60.png" border="0" class="hcp6"><br>
	<br>
	<span class="hcp5">You can then select a clip and choose 
	 the schedule time to add it to the scheduler.</span></p></li>
	<li class="hcp3"><p class="hcp10"><a name="ShowLinkedClipsInScheduler"></a>Show 
	 Linked Clips in Scheduler<br>
	<br>
	<span class="hcp5">This option allows you to display 
	 any linked clips along with any scheduled items is the same schedule 
	 dashboard. This makes it easier when setting up complex scheduled 
	 shows. To display the linked clips click on the links icon.</span><br>
	<br>
	<img alt="" src="../images/NewItem62.png" border="0" class="hcp6"><br>
	<br>
	<span class="hcp5">This will show any linked clips 
	 in grey.</span><br>
	<br>
	<img alt="" src="../images/NewItem61.png" border="0" class="hcp6"><br>
	<a href="#"><img src="../images/120.bmp" alt="" border="0" class="hcp9"> <span class="hcp5">Back 
	 to top</span></a></p></li>
</ol>
<h3>&#160;</h3>
<h3><a name="MiniTOCBookMark5"></a>February 2012: Version 3.7</h3>
<ol type="1">
	<li class="hcp3"><p><a name="ExemptClipScheduleFromCopyPaste"></a>Exempt 
	 Clip Schedule from Copy/Paste<br>
	<br>
	<span class="hcp5">Stopped a clip's schedule settings 
	 from being copied with copy and paste.</span></p></li>
	<li class="hcp3"><p><a name="RepairAllClips"></a>Repair 
	 All Clips<br>
	<br>
	<span class="hcp5">Allows you to repair all clips in 
	 a show not just a single clip. Using this function you can specify 
	 a folder path to be searched for all the media in the show. If the 
	 missing file is found it will be assigned to any broken clips. The 
	 selected folder is searched recursively for media files.</span><br>
	<br>
	<img alt="" src="../images/NewItem63.png" border="0" class="hcp6"></p></li>
	<li class="hcp3"><p><a name="ResolvedLIveVideoDVDClipsx64"></a>Resolved 
	 <a href="../reference/clipTypes/LiveVideoClip.md">Live Video</a> 
	 and <a href="../reference/clipTypes/DVDClip.md">DVD Clips</a> on 
	 x64<br>
	<br>
	<span class="hcp5">You may now use Live Video and DVD 
	 clips on all x64 systems.</span></p></li>
	<li class="hcp3"><p><a name="LinkColumnAddedToScheduleDashboard"></a>Link 
	 Column added to Schedule Dashboard<br>
	<br>
	<span class="hcp5">A link column has been added to 
	 the Schedule dashboard.</span></p></li>
	<li class="hcp3"><p><a name="SearchClip"></a>Search Clip<br>
	<br>
	<span class="hcp5">A search field has been added to 
	 the select clip dialog to make it easier to find the clip you want.</span><br>
	<br>
	<img alt="" src="../images/NewItem64.png" border="0" class="hcp6"></p></li>
	<li class="hcp3"><p>Link Clip Edit Tool<br>
	<br>
	<span class="hcp5">A new dashboard edit tool has been 
	 added to make it easier to create links between clips. To enter the 
	 link edit mode select the link tool from the main dashboard toolbar.</span><br>
	<br>
	<img alt="" src="../images/NewItem65.png" border="0" class="hcp6"><br>
	<br>
	Once you enter the mode, select a clip with links.<br>
	<br>
	<span class="hcp5">The selected clip with links will 
	 be highlighted with a blue border. The linked clips will be highlighted 
	 with green borders and all other clips will be have gray borders.</span><br>
	<br>
	<img alt="" src="../images/NewItem66.png" border="0" class="hcp6"><br>
	<br>
	<span class="hcp5">You can now select on any clip to 
	 edit or add a link from the selected clip. The link type is shown 
	 in the clip panel.<br>
	<br>
	Using this tool it is much easier to create and view complicated links.</span></p></li>
	<li class="hcp3"><p><a name="NewHotkeysAdded"></a>New 
	 <a href="../Reference/Hotkeys.md">Hotkeys</a> Added</p></li>
</ol>
<table cellspacing="0" border="1" class="hcp11">
	<col>
	<col>
	<tr>
		<td>Home</td>
		<td>Goto Page 1</td>
	</tr>
	<tr>
		<td>PageUp</td>
		<td>Next Page</td>
	</tr>
	<tr>
		<td>PageDown</td>
		<td>Previous Page</td>
	</tr>
	<tr>
		<td>Ctrl + P</td>
		<td>Playback/Live Mode</td>
	</tr>
	<tr>
		<td>Ctrl + E</td>
		<td>Edit Mode</td>
	</tr>
	<tr>
		<td>Ctrl + L</td>
		<td>Link Edit Mode</td>
	</tr>
</table>
<ol start="8" type="1">
	<li class="hcp3"><p><a name="New_Mouse_Shortcuts"></a>New 
	 Mouse Shortcuts</p></li>
</ol>
<table cellspacing="0" border="1" class="hcp11">
	<col>
	<col>
	<tr>
		<td>Alt + Right Click</td>
		<td>Edit Links</td>
	</tr>
	<tr>
		<td>Ctrl + Right Click</td>
		<td>Edit Schedule</td>
	</tr>
</table>
<ol start="9" type="1">
	<li class="hcp3"><p><a name="TextClipBackgroundImageAspectRatio"></a>Text 
	 Clip Background Image Aspect Ratio<br>
	<br>
	<span class="hcp5">The image background of a text clip 
	 will now obey the aspect ratio settings specified for a layer. Previously 
	 the image would always be stretched.</span></p></li>
	<li class="hcp3"><p><a name="MacrosLoggedInStatistics"></a>Macros 
	 Logged in Statistics<br>
	<br>
	<span class="hcp5">Macro events are now logged in the 
	 statistics output along with standard media clips.</span></p></li>
	<li class="hcp3"><p><a name="UserClipThumbnails"></a>User 
	 Clip Thumbnails<br>
	<br>
	<span class="hcp5">You may now add your own thumbnail 
	 images to clips rather than having to use the default images. To change 
	 the thumbnail, right click the clip and choose Rename. this will open 
	 a dialog that allows you to rename the clip and choose a clip thumbnail.</span><br>
	<br>
	<img alt="" src="../images/NewItem67.png" border="0" class="hcp6"><br>
	<a href="#"><img src="../images/120.bmp" alt="" border="0" class="hcp9"> <span class="hcp5">Back 
	 to top</span></a></p></li>
</ol>
<p>&#160;</p>
<h3><a name="MiniTOCBookMark6"></a>March 2012: Version 3.7</h3>
<ul type="disc">
	<li class="hcp8"><p><span class="hcp12"><a 
	 name="MultiLineInTextClip"></a>Multi Line in Text Clip</span><br>
	<br>
	You may add multiple lines to text clip items by using <span class="hcp12">Shift+Enter</span>.</p></li>
	<li class="hcp8"><p><span class="hcp12"><a 
	 name="3764BitWebBrowserFix"></a>Fix for Web Browser on 64Bit Systems<br>
	<br>
	</span>On 64 bit systems there was previously no option for using the 
	 <a href="../reference/clipTypes/WebBrowserClip.md" class="hcp7">Web 
	 Browser clip</a>. Version 3.7 corrects this issue.<br>
	<br>
	<a href="#"><img src="../images/120.bmp" alt="" border="0" class="hcp9"> Back to top</a></p></li>
</ul>
<p>&#160;</p>
<h3><a name="MiniTOCBookMark7"></a>July 2012: Version 3.7</h3>
<ol type="1">
	<li class="hcp3"><p><a name="NewAndImprovedSetup"></a>New 
	 and Improved Setup<br>
	<br>
	<span class="hcp5">Created a new setup process to ensure 
	 Screen Monkey is always installed correctly every time.</span></p></li>
	<li class="hcp3"><p><a name="LiveStreamClip"></a>Live 
	 Stream Clip<br>
	<br>
	<span class="hcp5">You can use the Live Stream clip 
	 to display live video streams across the internet. <a href="../reference/clipTypes/LiveStream.md" class="hcp7">Click 
	 here</a> for more.</span></p></li>
	<li class="hcp3"><p><a name="BlackMagicDeckLinkRenderer"></a>Blackmagic 
	 DeckLink Renderer (Pro Feature)<br>
	<br>
	<span class="hcp5">Support has been added for the Blackmagic 
	 DeckLink Renderer. <a href="../Reference/Setup/BlackMagicDeckLink.md" class="hcp7">Click here</a> 
	 for more.</span></p></li>
	<li class="hcp3"><p><a name="NewHelpFile"></a>New Help 
	 File <br>
	<br>
	<span class="hcp5">The help system has experienced 
	 a major overhaul and should now be more up to date and more accurately 
	 reflect Screen Monkey functionality.</span></p></li>
	<li class="hcp3"><p><a name="DashBoardChanges"></a>Dashboard 
	 Changes<br>
	<br>
	<span class="hcp5">The <a href="../tutorials/WorkingWithClips/MainWindow.md">Main 
	 Dashboard</a> has experienced some cosmetic changes as well as some 
	 new functionality.</span></p></li>
	<li class="hcp3"><p><a name="RelativePaths"></a><a href="../Glossary.md#RelativePathing">Relative 
	 Paths</a><br>
	<br>
	<span class="hcp5">Screen Monkey has been modified 
	 so that inside the show file relative paths to the media are written. 
	 This means that when you move the show between computers Screen Monkey 
	 will be able to find the correct media files.</span></p></li>
	<li class="hcp3"><p><a name="MIDIShowControl"></a><a 
	 href="../Glossary.md#MIDI">MIDI</a> Show Control<br>
	<br>
	<span class="hcp5">Screen Monkey now supports </span>MIDI 
	 Show Control<span class="hcp5"> Protocol.<br>
	<br>
	<a href="http://en.wikipedia.org/wiki/MIDI_Show_Control" target="_blank">Click 
	 here</a> for more via the Internet.</span><br>
	<br>
	<a href="#"><img src="../images/120.bmp" alt="" border="0" class="hcp9"> <span class="hcp5">Back 
	 to top</span></a></p></li>
</ol>
