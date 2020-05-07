<h1>MIDI</h1>
<p>Click the area of interest on the image below to learn more about that 
 option.</p>
<p class="hcp2"><img alt="" src="../../../images/SettingsMIDI.png" usemap="#MAP439593630" border="0" class="hcp3">
<map id="MAP439593630" name="MAP439593630">
<area shape="rect" coords="6, 25, 133, 39" href="General.md" alt="">
<area shape="rect" coords="6, 41, 133, 57" href="DisplayRenderer.md" alt="">
<area shape="rect" coords="6, 59, 133, 75" href="Artnet.md" alt="">
<area shape="rect" coords="6, 59, 133, 75" href="Artnet.md" alt="">
<area shape="rect" coords="6, 77, 133, 93" href="CITP.md" alt="">
<area shape="rect" coords="6, 95, 133, 111" href="Network.md" alt="">
<area shape="rect" coords="6, 112, 133, 128" href="MouseandKeyboard.md" alt="">
<area shape="rect" coords="6, 147, 133, 163" href="ProUpgrade.md" alt="">
<area shape="rect" coords="6, 165, 133, 181" href="Statistics.md" alt="">
</map> </p>
<p>The MIDI Section in the Settings dialog enables you to use a MIDI controller 
 or MIDI keyboard to control Screen Monkey and activate clips.</p>
<p>Set-up is as easy as pressing a key; button on your MIDI controller 
 or MIDI keyboard then double clicking the action that you need to control. 
 Any actions that have keys assigned to them will appear in bold.</p>
<p class="rvps3" style="margin-left: 24px;"><img alt="" src="../../../images/img_325.jpg" width="510" height="351" border="0" class="hcp3"></p>
<table style="margin-left: 24px; border-collapse: separate;" cellspacing="0" 
		 border="1">
	<col>
	<col>
	<tr>
		<td class="hcp4"><p class="hcp5"><span class="hcp6">Channel </span></p></td>
		<td class="hcp4">MIDI Channel Number 
		<br>0=MIDI Channel 1</td>
	</tr>
	<tr>
		<td class="hcp4"><p class="hcp5"><span class="hcp6">Command</span></p></td>
		<td class="hcp4">This is the MIDI command, which 
		 can be; NoteOn, NoteOff, PolyPressure, Controller, ProgramChange, 
		 ChannelPressure or PitchWheel.</td>
	</tr>
	<tr>
		<td class="hcp4"><p class="hcp5"><span class="hcp6">Data1</span></p></td>
		<td class="hcp4">The MIDI data, for example; note 
		 number.</td>
	</tr>
	<tr>
		<td class="hcp4"><p class="hcp5"><span class="hcp6">Data2</span></p></td>
		<td class="hcp4">The MIDI data, for example; note 
		 velocity.</td>
	</tr>
	<tr>
		<td class="hcp4"><p class="hcp5"><span class="hcp6">Level</span></p></td>
		<td class="hcp4">Sets which parameters to ignore 
		 when matching the MIDI trigger with the incoming MIDI note.</td>
	</tr>
	<tr>
		<td class="hcp4"><p class="hcp5"><span class="hcp6">Enabled</span></p></td>
		<td class="hcp4">whether Screen Monkey should use 
		 this action or not (if Enabled=False).</td>
	</tr>
</table>
<p>Any action can be triggered by more than one MIDI command so you can 
 assign multiple notes to the same function.</p>
<p>To clear any key assignments you have made, select the action and click 
 the <span class="hcp6">clear trigger</span> button at the 
 top or press the <span class="hcp6">Delete</span> key.</p>
<p class="hcp2"><img alt="" src="../../../images/img_326.jpg" border="0" class="hcp3"></p>
<p>&#160;</p>
<h2>Select MIDI Device</h2>
<p class="rvps2">If you have more than one MIDI device connected to your 
 computer you may need to select which one Screen Monkey uses. You can 
 do this by clicking on the setup icon in the MIDI settings. This will 
 open a new window from which you can select the MIDI device you want to 
 use.</p>
<p class="rvps3" style="margin-left: 24px;"><img alt="" src="../../../images/img_327.jpg" border="0" class="hcp3"></p>
<p class="rvps3" style="margin-left: 24px;">&#160;</p>
<h2><span class="rvts16">Trigger Level</span></h2>
<p class="rvps4">The MIDI trigger level allows you to specify whether data2 
 is ignored or used in matching the trigger. </p>
<p class="rvps4">This is useful if you want to change the behavior for 
 different MIDI devices. If we have a MIDI trigger Command = NoteOn, data1 
 = 16, data2 = 32 and we get a MIDI NoteOn data1 = 16, data2 = 42. With 
 the level set to data1 the action would be executed because the disparity 
 in data2 is ignored. If the level was set to data2 then the action would 
 not occur because the two data2 values are different.</p>
<p class="rvps4" style="margin-left: 24px;"><img alt="" src="../../../images/img_328.jpg" width="494" height="326" border="0" class="hcp3"></p>
<p>&#160;</p>
<h2><span class="rvts16">Special Actions</span></h2>
<p><span class="hcp6">Play Clip</span> allows you to play 
 a specific clip on any layer. Each layer supports this action. The data1 
 parameter is the index of the clip to play on that layer.</p>
