<h1>Writing Your Own Effects Scripts</h1>
<p>This topic explains the concepts relating to the <b>Effect Generator</b> 
 clip type, and how to create your own effects scripts. For information 
 on creating and getting started with effects clips themselves check out 
 the <a href="WritingYourOwnEffectsScripts.md">Writing your own Effects 
 Scripts</a> topic. For reference information on the effect generator scripting 
 language take a look at the <a href="ScriptingLanguageReference.md">Scripting 
 Language Reference</a>. </p>
<p>&#160;</p>
<h2>How the Effects Generator works</h2>
<p>Effects consist of 3 parts:</p>
<ol type="1">
	<li><p>A list of <b>shapes</b> which make up the effect.</p></li>
	<li><p>A <b>color scheme</b> which determines what colors the shapes 
	 will be.</p></li>
	<li><p>A <b>cycle time</b> which determines how quickly new shapes 
	 are created and how long they last for.</p></li>
</ol>
<p>&#160;</p>
<p>We will look at how these three things are combined to make an effect 
 in this section. </p>
<ol type="1">
	<li><p><span class="hcp2">Shapes</span><br>
	<br>
	Shapes are the building blocks you will use to create effects. Each 
	 shape supports different parameters which allow its appearance and 
	 behavior to be customized. A full list of shapes and the parameters 
	 supported by each is available in the <a href="ScriptingLanguageReference.md">language 
	 reference</a>.</p></li>
	<li><p><span class="hcp2">Color Scheme</span><br>
	<br>
	Up to four colors may be used for shapes in your effect as well as 
	 an optional additional background color (specifying no background 
	 color makes the background transparent). Each shape uses one or more 
	 of the scheme colors, and may optionally be configured with a <b>tint</b> 
	 (darkness) and <b>opacity</b> for the color.</p></li>
	<li><p><span class="hcp2">Cycle Time</span><br>
	<br>
	When a shape is added to an effect, you must choose how often the shape 
	 should be generated. This value is specified in <b>cycles</b>.<br>
	<br>
	For example, specifying a shape generation interval of 1 cycle means 
	 that 1 shape will be generated for each cycle. But what exactly is 
	 a cycle?<br>
	<br>
	A cycle is an arbitrary length of time which you may adjust in order 
	 to make your effect play faster or slower: By specifying all the shape 
	 intervals in terms of cycles it's easy to make the effect faster (by 
	 specifying a shorter cycle time) or slower (by specifying a longer 
	 one). </p></li>
</ol>
<p>&#160;</p>
<h2>Creating a New Effect</h2>
<p>Writing effect scripts can be tricky at first. Fortunately the editor 
 includes a useful feature called the <b>assistant</b> which allows quick 
 creation of script entries. You may then customize the generated script 
 by editing it.</p>
<ol type="1">
	<li><p>To Create a New Effect, right-click an empty slot and choose 
	 the <span class="hcp2">Effect Generator</span> Clip 
	 type.<br>
	<br>
	The <span class="hcp2">Effect Library</span> dialog opens.</p></li>
	<li><p>Click the <span class="hcp2">Create New Effect</span> 
	 button in the lower left corner of the dialog.<br>
	<br>
	<img src="../../../images/CreateNewEffect.png" alt="" border="0" class="hcp3"><br>
	<br>
	The <span class="hcp2">Cue - Effect</span> dialog opens.<br>
	<br>
	<img src="../../../images/CueEffectDialog.png" alt="" border="0" class="hcp3"></p></li>
</ol>
<p>&#160;</p>
<p style="font-weight: bold;">Using the Assistant</p>
<p>To access the assistant, right-click the large gray area in the left 
 side of the dialog.</p>
<p>The Add Shape dialog opens.</p>
<p><img src="../../../images/AddShapeDialog.png" alt="" border="0" class="hcp3"></p>
<p>Each feature has a check box which allows you to decide whether you 
 want the feature enabled or not. If you don't specify a feature it will 
 keep its default value.</p>
<p>We will add a <b>LINE</b> shape to our effect:</p>
<ol type="1">
	<li><p>Click the shape type drop-down and select <b>LINE</b> from the 
	 list.<br>
	<br>
	<img src="../../../images/SelectingLine.png" alt="" border="0" class="hcp3"></p></li>
	<li><p>Click <b>Create Shape<span class="hcp4">.</span></b><br>
	<br>
	(Create Shape is the yellow box in the lower right corner of the dialog.)<br>
	<br>
	The preview window should now show a horizontal line moving from top 
	 to bottom. Notice that each line has a random height, and one line 
	 is being generated each second. (this is because the cycle time is 
	 1 second by default). At this point your script looks like this:<br>
	<br>
	<img src="../../../images/LineOne.png" alt="" border="0" class="hcp3"><br>
	<br>
	This tells the effect to generate a LINE every 1 cycles, this is called 
	 the <b>pulse time</b>. Since the shape will by default have a <b>life 
	 time </b>that matches its <b>pulse time</b>, a new LINE is generated 
	 each time the old one dies.</p></li>
	<li><p>We may also specify a different <b>life time </b>to the <b>pulse 
	 time</b>, the <b>life time</b> is specified by entering it after the 
	 <b>pulse time</b>, separated by a comma. Change the script to read:<br>
	<br>
	<span class="hcp2">LINE (1,2);</span><br>
	<br>
	Click <b>Update Preview<span class="hcp4"> and observe 
	 the preview window </span></b><span class="hcp4">to 
	 see</span> the results of this change.<br>
	<br>
	We now see two lines on screen at the same time because one new LINE 
	 is being generated each cycle, and each LINE lives for two cycles.</p></li>
</ol>
<table cellspacing="0" border="1" class="hcp5">
	<col>
	<col>
	<tr>
		<td><img src="../../../images/Noteimage.png" alt="" border="0" class="hcp3"></td>
		<td>All shapes support <b>pulse time</b> and <b>life time</b>, 
		 combining these two settings allows you to control the speed of 
		 generated shapes, and the number of shapes on the screen at once.</td>
	</tr>
</table>
<p>&#160;</p>
<h2>Creating a color scheme</h2>
<p>Creating a color scheme for your effect is as simple as clicking the 
 numbered palette buttons and choosing a color. Do this now by clicking 
 each palette button in turn and choosing a color.</p>
<p>Notice that our color scheme definition has now been added to the script, 
 you may change these numbers if you like, or you may simply use the palette 
 buttons to update them at any time.</p>
<p>The color scheme definitions look like the this (note that the numbers 
 will be different depending on the colors you selected:</p>
<p class="hcp6"><img src="../../../images/ColorsAdded.png" alt="" border="0" class="hcp3"></p>
<p>The color scheme may be placed anywhere you choose within the script.</p>
<table cellspacing="0" border="1" class="hcp5">
	<col>
	<col>
	<tr>
		<td><img src="../../../images/Noteimage.png" alt="" border="0" class="hcp3"></td>
		<td><b class="hcp7">Note that for consistency with 
		 other scripting languages, the American spelling of &quot;color&quot; 
		 is used for color scheme definitions.</b></td>
	</tr>
</table>
<p>&#160;</p>
<h2><b class="hcp7">Assigning colors to shapes</b></h2>
<p>You may have noticed that when you changed color scheme entry number 
 1, the LINE shape we have already added to our scene changed color to 
 match, this is because by default all shapes use color index 1. So how 
 do we assign a different color to a shape? It's easy!</p>
<p>Shapes may be configured with up to 3 colors. (see the table in the 
 <a href="ScriptingLanguageReference.md">language reference</a> for details)</p>
<p>For all shapes, the first two colors are the <b>fill color</b> and the 
 <b>border color</b>. To change the color assignments we enter the colors 
 to use in order, enclosed in square brackets and separated with semicolons.</p>
<p>For example, to use color 2 for <b>fill color </b>and color 3 and <b>border 
 color</b> we would need to add:</p>
<p class="hcp8">[2];[3];</p>
<p>Add this to your script now, you should have the following: </p>
<p class="hcp6"><img src="../../../images/ColorBorderAndFill.png" alt="" border="0" class="hcp3"></p>
<p>Click <b>Update Preview</b> to see your changes.</p>
<table cellspacing="0" border="1" class="hcp5">
	<col>
	<col>
	<tr>
		<td><img src="../../../images/Noteimage.png" alt="" border="0" class="hcp3"></td>
		<td>Be certain to avoid using spaces. all the characters need to 
		 be one after the other.</td>
	</tr>
</table>
<p>Now wait a minute? Why did the border of the LINEs not change color?</p>
<p>This is because the default border thickness is zero. We will look at 
 how to fix this by assigning border and other parameters later.</p>
<p>&#160;</p>
<h2>Adding more shapes to the effect</h2>
<p>While it's possible to create a nice effect using a single shape, more 
 often we will want to add more shapes to the effect. </p>
<p>Lets add another shape to the effect using the assistant:</p>
<ol type="1">
	<li><p>Right click the script area to show the assistant.</p></li>
	<li><p>Choose <b>LINE</b> from the drop-down.</p></li>
	<li><p>Click the <b>Direction</b> check box and select <b>Up</b> from 
	 the drop-down.</p></li>
	<li><p>Click the <b>Colour 1 (Fill) </b>check box and select <b>1</b> 
	 in the drop-down.</p></li>
	<li><p>Click <b>Create Shape</b>.</p></li>
</ol>
<p>If all goes to plan you should now have a line traveling up the screen 
 for every two that travel down. Notice that the lines going up and the 
 lines going down are in sync.</p>
<p>Our script so far looks like this:</p>
<p class="hcp6"><img src="../../../images/SecondLineAdded.png" alt="" border="0" class="hcp3"></p>
<p>Wait a minute! Why is the <b>up</b> parameter on a line of its own? 
 And what does &quot;<b>// direction</b>&quot;<b> </b>mean?</p>
<p>The answer is it's okay to split your shape definitions onto separate 
 lines, but with one rule: <b>each line which forms part of the shape definitions 
 MUST end with a semicolon!</b></p>
<p>This means that:</p>
<p class="hcp8">LINE (1,2);[2];[3];</p>
<p>is the same as</p>
<p class="hcp8">LINE (1,2);</p>
<p class="hcp8">[2];</p>
<p class="hcp8">[3];</p>
<p>But the lines below will <b>NOT</b> work as expected as they break the 
 rule.</p>
<p class="hcp8"><span class="hcp2">LINE 
 (1,2);</span></p>
<p class="hcp8">[2]<span class="hcp4"> 
 &#160;&#160;&lt;=== Note that the semicolon is missing</span></p>
<p class="hcp8">[3];</p>
<p>As for the &quot;<b>// direction</b>&quot; part, this is known as a 
 &quot;comment&quot; and it's a way of leaving notes in a script that provide 
 helpful information. In this case describing the parameter to the left 
 of it. </p>
<p>You might notice the comments in the color scheme definition. These 
 help identify which color is which. You can learn more about comments 
 in the <a href="ScriptingLanguageReference.md">language reference.</a></p>
<p>&#160;</p>
<h2>Spicing things up - using <b><i>delay time</i></b></h2>
<p>What we have so far is very nice, but the lines are perfectly in sync: 
 each upward line is generated perfectly in time with every other, this 
 is because both are generated at the same time in the cycle, this is represented 
 as follows:</p>
<p class="hcp6"><img src="../../../images/image5.gif" alt="" border="0" class="hcp3"> </p>
<p>The outer (blue) line represents the first LINE shape, which is generated 
 twice per cycle. The inner (red) track represents the second LINE shape. 
 Notice that the first and second lines are generated at the same point 
 in the cycle. While sometimes this is desirable, other times we may want 
 to make the effect more interesting or make it look more natural by offsetting 
 shape generation.</p>
<p>This is achieved using a third time parameter when specifying the shape, 
 this is added after the <b>life time</b> parameter and is known as <b>delay 
 time</b>.</p>
<p>We will delay our second LINE shape by quarter of a cycle in order to 
 bring it out of sync with the other line object, we will leave the <b>life 
 time</b> as 1 cycle. Change your script to include the new parameter, 
 you should have:</p>
<table width="576" class="hcp9">
	<tr>
		<td height="40" bgcolor="#000000" class="hcp10"><div class="hcp11">
			<font><span style="font-size: 10pt; font-family: Arial; color: #010101;"><br>
			</span></font> 
		</div>
		<div class="hcp11">
			<font><span class="hcp12">LINE(1,2);[2];[3];</span></font> 
			 
		</div>
		<div class="hcp11">
			<font><span class="hcp12"><br>
			</span></font> 
		</div>
		<div class="hcp11">
			<font><span class="hcp12">LINE(1,1,0.25);</span></font> 
			 
		</div>
		<div class="hcp11">
			<font><span class="hcp12">&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;up;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;// 
			 direction</span></font> 
		</div>
		<div class="hcp11">
			&#160; 
		</div></td>
	</tr>
</table>
<p>Press <b>Update Preview </b>to see your changes, the end result is a 
 system which can be represented as follows:</p>
 
 
<p>6. Using color tints and opacity</p>
<p>As mentioned above, when assigning colors to shapes, you can also choose 
 a tint and an opacity value, we have already seen how to specify colors 
 by palette number:</p>
<p>[<i>&lt;number&gt;</i>]&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;<font><span class="hcp13">example:&#160;&#160;&#160;</span></font><font><span class="hcp14">[1]</span></font> 
 </p>
<p>However, it is also possible to specify an opacity from 0 to 255 where 
 0 is transparent and 255 is fully opaque:</p>
<p>[<i>&lt;number&gt;,</i>&lt;opacity&gt;]&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;<font><span class="hcp13">example:&#160;&#160;&#160;</span></font><font><span class="hcp14">[1,128]</span></font> 
 </p>
<p>You can also specify a &quot;tint value&quot; from 0 to 1 where 0 is 
 black and 1 is full color:</p>
<p>[<i>&lt;number&gt;,</i>&lt;opacity&gt;,&lt;tint&gt;]&#160;&#160;&#160;example:&#160;&#160;&#160;[1,128,0.5]</p>
<p>Let's try it out by assigning a partially transparent color to the upward 
 lines. Add the following at the end of the script:</p>
<p>[4,120];</p>
<p>You should now have:</p>
<table width="576" class="hcp9">
	<tr>
		<td height="40" bgcolor="#000000" class="hcp10">LINE(1,2);[2];[3];</td>
		<td>color: #ffff00;&quot;&gt;LINE(1,1,0.25);</td>
		<td>&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;up;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;// 
		 direction</td>
		<td>&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;[4,120];</td>
	</tr>
</table>
<p>Click <b>Update Preview</b> to apply the changes, you should now notice 
 that the upward lines are partially see-through, and when they pass over 
 the downward lines the colors are blended.</p>
<p>Digging Deeper - Customising Shapes Using Parameters</p>
<p>Whilst using different shapes allows you to create cool effects, you 
 can also take control of how your shapes behave by using <b>parameters</b>. 
 We have already seen an example of a parameter that changes a shape's 
 behaviour above - that is the <i>direction</i> parameter we used to make 
 the LINE move up instead of down.</p>
<p>Before we get started, it helps to know a couple of things about parameters: 
 </p>
<p>All shape parameters have a <b>default value</b>. This is the value 
 that the shape will assume if the parameter is not specified.p&gt; </p>
<p>Parameters come in two flavors, <b>flags</b> and <b>parameters</b></p>
<p>&#160;&#160;&#160;&#160;&#160;<b>Flags</b> are kind of like a selector 
 switch for your shape that alter the behaviour in some way, the <i>direction</i> 
 flag is a good example of a <b>flag</b> parameter. <b>Flags</b> are specified 
 by simply putting the name of the flag you want to use. For example UP, 
 DOWN, LEFT or RIGHT for the <i>direction</i> flag.<br>
</p>
<p>Here is an example of a flag:/p&gt; </p>
<p>&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;LEFT;</p>
<p>&#160;&#160;&#160;&#160;&#160;Parameters are used to control a value 
 and consist of a parameter name and a value in brackets. The <i>size </i>parameter 
 for example specifies the size of a shape in percentage points:</p>
<p>&#160;&#160;&#160;&#160;&#160;&#160;SIZE(50);</p>
<p>This tells the shape's size to be 50% of the screen size.</p>
<p>A full list of parameters is available in the <a href="ScriptingLanguageReference.md">language 
 reference</a>.</p>
<p>1. Using the assistant to set initial parameters</p>
<p>To make it easy to experiment and see how different parameters affect 
 different shapes, you can use the assistant to generate parameters for 
 you, and then simply change the values.</p>
<p>Have fun making your own effects!</p>
