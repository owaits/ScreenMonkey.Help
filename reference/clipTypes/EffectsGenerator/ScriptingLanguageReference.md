<h1>Scripting Language Reference</h1>
<h2>Effect Generator Scripting Reference</h2>
<p>This section contains reference information for the Effect Generator 
 scripting language. For an introductory tutorial see the <a href="WritingYourOwnEffectsScripts.md">Creating 
 Your Own Effects Scripts</a> topic.</p>
<h2>Syntax Overview</h2>
<p>A brief outline of the general syntax for the scripting commands</p>
<p class="hcp2">Color scheme definitions</p>
<p class="hcp3">Color scheme definitions can appear anywhere 
 in your script, although convention is to put them at the start. Scheme 
 definitions are not indexed must appear in palette order. To change the 
 palette order change the order of the definitions.</p>
<p class="hcp3">Color scheme definition</p>
<div>
	<table style="border-width: 0px; margin-left: 36px;" cellspacing="0">
		<tr class="hcp4">
			<td height="32" width="526" class="hcp5"><p>COLOR(<span>{red}</span>,<span>{green}</span>,<span>{blue}</span>);</p></td>
		</tr>
	</table>
</div>
<p class="hcp3">When defining Color scheme, the background 
 Color can be specified.</p>
<p class="hcp6">Background Color definition</p>
<div>
	<table style="border-width: 0px; margin-left: 48px;" cellspacing="0">
		<tr class="hcp4">
			<td height="32" width="526" class="hcp5"><p>BACKGROUND({red},{green}{blue});</p></td>
		</tr>
	</table>
</div>
<p class="hcp3">The following is an example of a full Color 
 scheme definition block including all 4 palette Colors:</p>
<p class="hcp3">Example Color scheme definition</p>
<p class="hcp6"><img src="../../../images/ColorsAdded.png" alt="" style="border: none;" border="0"></p>
<p class="hcp2">Shape definitions</p>
<p class="hcp3">Shape definitions consist of the shape name 
 and from 1 to 3 timing parameters. (The second and third timing parameters 
 are optional.)</p>
<p class="hcp7">Shape Timing definition</p>
<p class="hcp8">The Shape Timing definition consists of the 
 shape name and from 1 to 3 timing parameters.</p>
<p class="hcp8">(The second and third timing parameters are 
 optional.)</p>
<div>
	<table style="border-width: 0px; margin-left: 60px;" cellspacing="0">
		<tr class="hcp4">
			<td height="32" width="526" class="hcp5"><p>{shapename}<span>(</span>{pulsetime}<span>,</span>{lifetime*}<span>,</span>{delaytime*}<span>);</span></p></td>
		</tr>
	</table>
</div>
<p style="font-size: 6pt;">&#160;</p>
<table cellspacing="0" border="1" class="hcp9">
	<col>
	<col>
	<tr>
		<td>Pulse Time</td>
		<td>Defines the period (in cycles) between generation of new shapes.</td>
	</tr>
	<tr>
		<td>Life Time</td>
		<td>If omitted, is the same as pulse time. Otherwise, &#160;specifies 
		 the lifespan for each generated shape (in cycles).</td>
	</tr>
	<tr>
		<td>Delay Time</td>
		<td>Is the delay period (in cycles) before shapes begin to be generated, 
		 useful for offsetting shapes from each other (forcing them &quot;out 
		 of phase&quot; with one another).</td>
	</tr>
</table>
<p style="margin-left: 60px;">The following example shows a BOX shape with 
 a pulse time of 2 cycles and life span of 3 cycles and no delay:</p>
<div>
	<table cellspacing="0" class="hcp10">
		<tr class="hcp4">
			<td height="32" width="526" class="hcp5"><p>BOX<span>(</span>2<span>,</span>3<span>);</span></p></td>
		</tr>
	</table>
</div>
<p>&#160;</p>
<p class="hcp7">Shape Parameters</p>
<p class="hcp8">Shape parameters follow the shape definition. 
 There are 3 types of supported parameters and they can appear in any order 
 following the shape definition:</p>
<ol>
	<li><p class="hcp6">Color palette mappings<br>
	</p></li>
</ol>
<div>
	<table cellspacing="0" class="hcp10">
		<tr class="hcp4">
			<td height="32" width="526" class="hcp5"><p>[<span>{index}</span>,<span>{opacity*}</span>,<span>{tint*}</span>];</p></td>
		</tr>
	</table>
</div>
<p>&#160;</p>
<table cellspacing="0" border="1" class="hcp9">
	<col>
	<col>
	<tr>
		<td>Index</td>
		<td>Color palette number to use</td>
	</tr>
	<tr>
		<td>Opacity</td>
		<td><span>Optional</span> transparency value from 0 (transparent) 
		 to 255 (opaque)</td>
	</tr>
	<tr>
		<td>Tint</td>
		<td>Optional darkness of the specified Color from 0 (black) to 
		 1 (full Color)</td>
	</tr>
</table>
<p>&#160;</p>
<p>Each shape supports a number of mappable Color slots. Slot 1 and Slot 
 2 always correspond to the fill Color for the shape, and the border Color 
 for the shape respectively. Some shapes support more than one Color.</p>
<p>To map palette Colors to shape Color slots specify the Colors in order.</p>
<p>For example to map Color 2 to fill and Color 3 to border, use the following:</p>
<div>
	<table cellspacing="0" class="hcp11">
		<tr class="hcp4">
			<td height="32" width="526" class="hcp5"><p>[<span>2</span>];[<span>3</span>];</p></td>
		</tr>
	</table>
</div>
<p>You may optionally specify opacity values for each Color mapping:</p>
<div>
	<table cellspacing="0" class="hcp11">
		<tr class="hcp4">
			<td height="32" width="526" class="hcp5"><p>[<span>2</span>,<span>128</span>];[<span>3</span>,<span>160</span>];</p></td>
		</tr>
	</table>
</div>
<p>And tints if you require:</p>
<div>
	<table cellspacing="0" class="hcp11">
		<tr class="hcp4">
			<td height="32" width="526" class="hcp5"><p>[<span>2</span>,<span>128</span>,<span>0.5</span>];[<span>3</span>,<span>160</span>,<span>0.5</span>];</p></td>
		</tr>
	</table>
</div>
<ol>
	<li>Flags</li>
	<li>Flags are simple one-word parameters which change the shape's behaviour, 
	 there are currently two supported flag sets: fade and direction. To 
	 specify the flag just enter the flag name you want to use. The flag 
	 sets are as follows:</li>
</ol>
<ol>
	<li>Fade supports FADE, FADEIN and NONE. These correspond to fade from 
	 fully opaque to transparent during the shape's lifetime; the reverse 
	 effect, and no fade (fully opaque always).</li>
	<li>Direction supports UP, DOWN, LEFT and RIGHT. These correspond to 
	 directions of travel.</li>
</ol>
<p>While it's possible to specify multiple flags from the same flag set, 
 this makes no sense as flags within a set are mutually exclusive. Specifying 
 LEFT and RIGHT flags together for example makes no sense.</p>
<ol>
	<li><p>Parameters</p></li>
	<li><p>Parameters are like flags except that they take a value as well, 
	 which affects how the shape behaves. Parameters are discusses in more 
	 detail in the shapes section below.</p></li>
	<li><p>Parameters always have the following form:</p></li>
</ol>
<p><span>Shape parameter syntax</span></p>
<div>
	<table cellspacing="0" class="hcp11">
		<tr class="hcp4">
			<td height="32" width="526" class="hcp5"><p>{name}<span>(</span>{value}<span>);</span></p></td>
		</tr>
	</table>
</div>
<p class="hcp2">Supported Shape Types</p>
<p>&#160;</p>
<table cellspacing="0" border="1" class="hcp12">
	<col>
	<col>
	<tr>
		<td><p class="hcp13">BLOCK</p></td>
		<td>&#160;</td>
	</tr>
	<tr>
		<td><p class="hcp13">BOX</p></td>
		<td><span>Creates a box which appears at a random location and 
		 expands to a random size. Defaults to the</span> fadein fade type. 
		 The maximum size may be overridden using the size parameter.</td>
	</tr>
	<tr>
		<td><p class="hcp13">BUBBLE</p></td>
		<td>Creates a bubble which appears at a random location along the 
		 bottom of the screen and rises to the top. The size is chosen 
		 at random but may be set to a fixed size using the size parameter 
		 or a minimum size specified using the min parameter.</td>
	</tr>
	<tr>
		<td><p class="hcp13">CHEVRON</p></td>
		<td>Creates a chevron which moves across the screen. The sweep 
		 parameter specifies the angle of the chevron as a percentage of 
		 the screen size.</td>
	</tr>
	<tr>
		<td><p class="hcp13">CIRCLE</p></td>
		<td><span>Creates a circle which appears at a random location and 
		 expands to a random size. Defaults to the</span> fadein fade type. 
		 The maximum size may be overridden using the size parameter.</td>
	</tr>
	<tr>
		<td><p class="hcp13">CONFETTI</p></td>
		<td>&#160;</td>
	</tr>
	<tr>
		<td><p class="hcp13">DIAMOND</p></td>
		<td><span>Creates a diamond which appears at a random location 
		 and expands to a random size. Defaults to the</span> fadein fade 
		 type. The maximum size may be overridden using the size parameter.</td>
	</tr>
	<tr>
		<td><p class="hcp13">LEAF</p></td>
		<td><span>Creates a leaf shape at a random location along the top 
		 of the screen which floats downward. Size is selected at random 
		 or may be overridden using the</span> size <span>or</span> min 
		 parameters.</td>
	</tr>
	<tr>
		<td><p class="hcp13">LINE</p></td>
		<td>Creates a horizontal or vertical line that moves across the 
		 screen. The size of the line is selected at random or may be specified 
		 using the <span>size</span> parameter. The line begins at the 
		 screen edge.</td>
	</tr>
	<tr>
		<td><p class="hcp13">LINEM</p></td>
		<td>Creates a horizontal or vertical line that moves across the 
		 screen. The size of the line is selected at random or may be specified 
		 using the <span>size</span> parameter. The line begins in the 
		 middle of the screen.</td>
	</tr>
	<tr>
		<td><p class="hcp13">RADAR</p></td>
		<td>&#160;</td>
	</tr>
	<tr>
		<td><p class="hcp13">ROTOR</p></td>
		<td>&#160;</td>
	</tr>
	<tr>
		<td><p class="hcp13">SNAKE</p></td>
		<td>&#160;</td>
	</tr>
	<tr>
		<td><p class="hcp13">SNOWFLAKE</p></td>
		<td><span>Creates a snowflake shape at a random location along 
		 the top of the screen which floats downward. Size is selected 
		 at random or may be overridden using the</span> size <span>or</span> 
		 min parameters.</td>
	</tr>
	<tr>
		<td><p class="hcp13">STAR</p></td>
		<td><span>Creates a star shape at a random location along the top 
		 of the screen which floats downward. Size is selected at random 
		 or may be overridden using the</span> size <span>or</span> min 
		 parameters.</td>
	</tr>
	<tr>
		<td><p class="hcp13">STROBE</p></td>
		<td>&#160;</td>
	</tr>
	<tr>
		<td><p class="hcp13">VUMETER</p></td>
		<td>&#160;</td>
	</tr>
</table>
<p>&#160;</p>
<p>Shape Parameters</p>
<p>Some parameters are supported by all shapes and some by only a few, 
 see the table below for which parameters are supported by which shapes. 
 The following is a description of each parameter and the values it will 
 accept.</p>
<table cellspacing="0" border="1" class="hcp12">
	<col>
	<col>
	<col>
	<tr>
		<td bgcolor="#808080"><span class="hcp14">Parameter</span></td>
		<td bgcolor="#808080"><span class="hcp14">Range/Values</span></td>
		<td bgcolor="#808080"><span class="hcp14">Description</span></td>
	</tr>
	<tr>
		<td>size()</td>
		<td><span>percentage</span></td>
		<td>Sets the maximum (or fixed) size for a shape. Specified as 
		 a percentage of the screen size, can exceed 100% if you want a 
		 large shape.</td>
	</tr>
	<tr>
		<td colspan="3" bgcolor="#C0C0C0"><span class="hcp14">Example: 
		 SIZE(50);</span> 
		<p>Note: do not include the % sign!</p>
		<p>&#160;</p></td>
		
	</tr>
	<tr>
		<td>border()</td>
		<td>pixels</td>
		<td>Sets the border width for the shape. Specified in pixels.</td>
	</tr>
	<tr>
		<td colspan="3" bgcolor="#C0C0C0"><span class="hcp14">Example: 
		 BORDER(4);</span> 
		<br>&#160;</td>
		
	</tr>
	<tr>
		<td>min()</td>
		<td>percentage</td>
		<td>Sets the minimum size for a shape which supports random size 
		 such as <span>BUBBLE</span> and <span>CIRCLE</span>.</td>
	</tr>
	<tr>
		<td colspan="3" bgcolor="#C0C0C0"><span class="hcp14">Example:&#160;MIN(10);</span> 
		 
		<br>&#160; 
		<p>Note: min should be less than size!</p>
		<p>&#160;</p></td>
		
	</tr>
	<tr>
		<td>sweep()</td>
		<td>percentage</td>
		<td>Sets the sweep angle for the CHEVRON shape.</td>
	</tr>
	<tr>
		<td colspan="3" bgcolor="#C0C0C0"><span class="hcp14">Example:&#160;SWEEP(50);</span> 
		 
		<br>&#160;</td>
		
	</tr>
	<tr>
		<td>&#160;</td>
		<td>&#160;</td>
		<td>&#160;</td>
	</tr>
</table>
<p>&#160;</p>
<p>Shape Parameter Support and Color Slot Mapping Table</p>
<p>The following table summarizes the parameters and flags supported by 
 each shape.</p>
<p><img alt="" src="../../../images/img_279.jpg" style="margin-top: 1px; margin-bottom: 1px; 
		 margin-left: 1px; margin-right: 1px;" border="0"></p>

