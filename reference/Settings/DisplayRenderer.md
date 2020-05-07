<h1>Display Renderer</h1>
<p>Click the area of interest on the image below to learn more about that 
 option.</p>
<p style="margin-left: 24px;"><img alt="" src="../../../images/SettingsDisplayRenderer.png" usemap="#MAP439448451" border="0" class="hcp2">
<map id="MAP439448451" name="MAP439448451">
<area shape="rect" coords="6, 25, 133, 39" href="General.md" alt="">
<area shape="rect" coords="6, 59, 133, 75" href="Artnet.md" alt="">
<area shape="rect" coords="6, 59, 133, 75" href="Artnet.md" alt="">
<area shape="rect" coords="6, 77, 133, 93" href="CITP.md" alt="">
<area shape="rect" coords="6, 95, 133, 111" href="Network.md" alt="">
<area shape="rect" coords="6, 112, 133, 128" href="MouseandKeyboard.md" alt="">
<area shape="rect" coords="6, 130, 133, 146" href="MIDI.md" alt="">
<area shape="rect" coords="6, 147, 133, 163" href="ProUpgrade.md" alt="">
<area shape="rect" coords="6, 165, 133, 181" href="Statistics.md" alt="">
<area shape="rect" coords="145, 43, 567, 62" href="#Standard_Renderer" alt="">
</map> </p>
<p>When a clip is played and appears on the screen it uses a display renderer 
 to actually display the clip. The renderer also handles mixing the layers 
 together as well as the effects and animations. Screen Monkey allows you 
 to choose which renderer is used.</p>
<p>Why would you want to do this?</p>
<p>Each renderer has different functionality and compatibilities, so you 
 need to choose a renderer that is right for your application.</p>
<p>The display renderer is selected by opening Screen Monkey <a class="rvts11" 
	 href="General.md">settings</a> and selecting the &quot;Display 
 Renderer&quot; section.</p>
<p class="rvps2" style="margin-left: 24px;"><img alt="" src="../../../images/img_340.jpg" border="0" class="hcp2"></p>
<p>The display renderers are pluginable so you can develop your own renderer 
 plugin should you wish.</p>
<p>&#160;</p>
<h2><a name="Standard_Renderer"></a>Standard Renderer</h2>
<p>The standard renderer uses the Microsoft GDI and DirectX technology 
 to display clips to the screen. This renderer is compatible with all clip 
 types but only supports 2D graphics and simple transition effects.</p>
<p>&#160;</p>
<h2>WPF Renderer</h2>
<p>This uses the latest WPF technology built into Windows Vista to display 
 the clips to the screen. It supports 3D graphics and allows for more elaborate 
 transition effects. You may also notice that the animations are smoother 
 with higher performance. Currently the only clip types that support the 
 WPF renderer are Image, Color, Song and Video but this will be extended 
 in future versions.</p>
<p>When the WPF renderer is enabled extra 3D <a href="../../../tutorials/WorkingWithClips/Transitions.md">transition 
 effects</a> become available.</p>
<p>WPF is an initialism meaning <a href="http://en.wikipedia.org/wiki/Windows_Presentation_Foundation" 
									 target="_blank">Windows Presentation 
 Foundation</a>.</p>
