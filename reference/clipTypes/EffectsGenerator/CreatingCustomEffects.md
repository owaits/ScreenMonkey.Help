<h1 class="rvps6">Creating Custom Effects</h1>
<p>This topic explains the concepts relating to the <a href="EffectsGeneratorClip.md">Effect 
 Generator clip</a> type, and how to create your own effect scripts</p>
<p>For reference information on the effect generator scripting language 
 take a look at the <a href="ScriptingLanguageReference.md">Scripting 
 Language Reference</a>.</p>
<p>&#160;</p>
<p class="hcp2">How the Effects Generator works</p>
<p>Effects are made up of 3 parts:-+ </p>
<ol>
	<li><p class="hcp3">A list of <span class="hcp4">shapes</span> 
	 which make up the effect.</p></li>
	<li><p class="hcp3">A <span class="hcp4">color 
	 scheme</span> which determines what colors the shapes will be.</p></li>
	<li><p class="hcp3"><span class="rvts13">A</span> <span 
	 class="rvts15" style="font-weight: bold;">cycle time</span> <span 
	 class="rvts13">which determines how quickly new shapes are created 
	 and how long they last.</span></p></li>
</ol>
<p>&#160;</p>
<p>We will look at how these three things are combined to make an effect 
 in this section.</p>
<ol type="1">
	<li><p><span class="hcp4">Shapes</span><br>
	<br>
	Shapes are the building blocks you will use to create effects, each 
	 shape supports different parameters which allow its appearance and 
	 behavior to be customized. A full list of shapes and the parameters 
	 supported by each is available in the <a href="ScriptingLanguageReference.md">language 
	 reference</a>.</p></li>
	<li><p><span class="hcp4">Color Scheme</span><br>
	<br>
	Up to four scheme colors can be used for shapes in your effect, and 
	 an optional additional background color (specifying no background 
	 color makes the background transparent). Each shape can use 1 or more 
	 of the scheme colors, and can optionally specify a tint (darkness) 
	 and opacity for the color.</p></li>
	<li><p><span class="hcp4">Cycle Time</span><br>
	<br>
	When you add a shape to your effect, you have to choose how often it 
	 should be generated, this value is specified in cycles. For example 
	 specifying an shape generation interval of 1 cycle means that 1 shape 
	 will be generated for every 1 cycle. But what is a cycle?<br>
	<br>
	A cycle is an arbitrary length of time which you can change to make 
	 your effect go faster or slower: by specifying all the shape intervals 
	 in terms of cycles it is easy to make the effect faster (by specifying 
	 a shorter cycle time) or slower (by specifying a longer one).</p></li>
</ol>
<p>&#160;</p>
<p class="hcp2">Getting Started</p>
<p>Writing effects scripts can be tricky at first, luckily the editor includes 
 a useful feature called the assistant which allows quick creation of script 
 entries. You can then customize the generated script by editing it.</p>
<ol type="1">
	<li>Using the Assistant</li>
</ol>
<p>To access the assistant, right-click the script area:</p>
<p><img alt="" src="../../../images/img_276.jpg" border="0" class="hcp5"></p>
<p>Each feature has a check box which allows you to decide whether you 
 want the feature included or not, if you do not specify a feature it will 
 keep its default value.</p>
<p>We will add a LINE shape to our effect:</p>
<ol>
	<li><p>Select shape type LINE from the drop-down list.</p></li>
	<li><p>Click Create Shape.</p></li>
</ol>
<p>The preview window should now show a line moving downward, notice that 
 each line has a random thickness, and one line is being generated every 
 second (because the cycle time is 1 second by default). The script that 
 has been created looks like:</p>
<div>
	<table cellspacing="0" class="hcp6">
		<tr class="hcp7">
			<td height="40" width="568" class="hcp8"><p><br>
			</p>
			<p>LINE(1);</p></td>
		</tr>
	</table>
</div>
<p>This tells the effect to generate a LINE every 1 cycles, this is called 
 the pulse time. Since the shape will by default have a life time that 
 matches its pulse time, a new LINE is generated each time the old one 
 dies.</p>
<p>We can also specify a different life time to the pulse time, the life 
 time is specified by entering it after the pulse time, separated by a 
 comma. Change the script to read:</p>
<div>
	<table cellspacing="0" class="hcp6">
		<tr class="hcp7">
			<td height="40" width="568" class="hcp8"><p><br>
			</p>
			<p>LINE(1,2);</p></td>
		</tr>
	</table>
</div>
<p>Click Update Preview to see the results of this change.</p>
<p>We now have 2 lines on screen at a time because 1 new LINE is being 
 generated every 1 cycle, and each LINE lives for 2 cycles.</p>
<p>All shapes support pulse time and life time, combining these two settings 
 allows you to control the speed of generated shapes, and the number of 
 shapes on the screen at once.</p>
<p>2. Creating a color scheme</p>
<p>Creating a color scheme for your effect is as simple as clicking the 
 numbered palette buttons and choosing a color. Do this now by clicking 
 each palette button in turn and choosing a color.</p>
<p>Notice that our color scheme definition has now been added to the script, 
 you can change these numbers if you like, or you can simply use the palette 
 buttons to update them at any time.</p>
<p>The color scheme definitions looks like the this (note that the numbers 
 will be different depending on the colors you choose:</p>
<div>
	<table cellspacing="0" class="hcp6">
		<tr class="hcp7">
			<td height="40" width="568" class="hcp8"><p><br>
			</p>
			<p>// Color scheme definitions</p>
			<p>COLOR(250,255,0)&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;// 
			 color 1</p>
			<p>COLOR(255,0,0)&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;// 
			 color 2</p>
			<p>COLOR(255,128,0)&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;// 
			 color 3</p>
			<p>COLOR(0,255,0)&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;// 
			 color 4</p>
			<p>BACKGROUND(0,0,0)&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;// 
			 background</p></td>
		</tr>
	</table>
</div>
<p>The color scheme can be placed anywhere within the script that you like. 
 Note that for consistency with other scripting languages, the American 
 spelling of &quot;color&quot; is used for color scheme definitions.</p>
<p>3. Assigning colors to shapes</p>
<p>You may have noticed that when you changed color scheme entry number 
 1, the LINE shape we have already added to our scene changed color to 
 match, this is because by default all shapes use color index 1. So how 
 do we assign a different color to a shape? It's easy!</p>
<p>Shapes can support up to 3 colors, see the table in the <a href="ScriptingLanguageReference.md">language 
 reference</a> for details: for all shapes the first two colors are the 
 fill color and the border color. To change the color assignments we enter 
 the colors to use in order, enclosed in square brackets and separated 
 with semicolons: For example to use color 2 for fill color and color 3 
 and border color we would need to add:</p>
<p>[2];[3];</p>
<p>Add this to your script now, you should have the following:</p>
<div>
	<table cellspacing="0" class="hcp6">
		<tr class="hcp7">
			<td height="40" width="568" class="hcp8"><p><br>
			</p>
			<p>LINE(1,2);[2];[3];</p></td>
		</tr>
	</table>
</div>
<p>Click Update Preview to see your changes.</p>
<p>Now wait a minute? Why did the border of the LINEs not change colour. 
 This is because the default border thickness is zero, we will look at 
 how to fix this by assigning border and other parameters later.</p>
<p>4. Adding more shapes to the effect</p>
<p>While it's possible to make a cool effect with a single shape, more 
 often we will want to add more shapes to the effect. Lets add another 
 shape to the effect using the assistant:</p>
<ol>
	<li>Right click the script area to show the assistant.</li>
	<li>Choose LINE from the drop-down.</li>
	<li>Tick the Direction checkbox and select Up from the drop-down.</li>
	<li>Tick the Colour 1 (Fill) checkbox and select 1 in the drop-down.</li>
	<li>Click Create Shape.</li>
</ol>
<p>If all goes to plan you should now have a line travelling up the screen 
 for every two which travel down, notice that the lines going up and the 
 lines going down are in sync.</p>
<p>Our script so far looks like this:</p>
<div>
	<table cellspacing="0" class="hcp6">
		<tr class="hcp7">
			<td height="40" width="568" class="hcp8"><p><br>
			</p>
			<p>LINE(1,2);[2];[3];</p>
			<p><br>
			</p>
			<p>LINE(1);</p>
			<p>&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;up;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;// 
			 direction</p></td>
		</tr>
	</table>
</div>
<p>Wait a minute! Why is the up parameter on a line of its own? And what 
 does &quot;// direction&quot; mean?</p>
<p>The answer is it's okay to split your shape definitions onto separate 
 lines, but with one rule: each line which forms part of the shape definitions 
 MUST end with a semicolon!</p>
<p>This means that:</p>
<div>
	<table cellspacing="0" class="hcp6">
		<tr class="hcp7">
			<td height="40" width="568" class="hcp8"><p><br>
			</p>
			<p>LINE(1,2);[2];[3];</p></td>
		</tr>
	</table>
</div>
<p>is the same as</p>
<div>
	<table cellspacing="0" class="hcp6">
		<tr class="hcp7">
			<td height="40" width="568" class="hcp8"><p><br>
			</p>
			<p>LINE(1,2);</p>
			<p>[2];</p>
			<p>[3];</p></td>
		</tr>
	</table>
</div>
<p>but this will NOT work as expected since it breaks the rule.</p>
<div>
	<table cellspacing="0" class="hcp6">
		<tr class="hcp7">
			<td height="40" width="568" class="hcp8"><p><br>
			</p>
			<p>LINE(1,2)</p>
			<p>;[2]</p>
			<p>;[3];</p></td>
		</tr>
	</table>
</div>
<p>As for the &quot;// direction&quot;, this is known as a &quot;comment&quot;, 
 and it is a way of leaving notes in a script that provide helpful information 
 (in this case describing the parameter to the left of it. You might notice 
 the comments in the colour scheme definition, these help identify which 
 colour is which. You can learn more about comments in the <a href="ScriptingLanguageReference.md">language 
 reference</a>.</p>
<p>5. Spicing things up - using delay time</p>
<p>What we have so far is very nice, but the lines are perfectly in sync: 
 each upward line is generated perfectly in time with every other, this 
 is because both are generated at the same time in the cycle, this is represented 
 as follows:</p>
<p><img alt="" src="../../../images/img_277.jpg" border="0" class="hcp5"></p>
<p>The outer (blue) line represents the first LINE shape, which is generated 
 twice per cycle. The inner (red) track represents the second LINE shape. 
 Notice that the first and second lines are generated at the same point 
 in the cycle. While this is desirable sometimes, other times we may want 
 to make the effect more interesting or make it look more natural by offsetting 
 shape generation.</p>
<p>This is achieved using a third time parameter when specifying the shape, 
 this is added after the life time parameter and is known as delay time.</p>
<p>We will delay our second LINE shape by quarter of a cycle in order to 
 bring it out of sync with the other line object, we will leave the life 
 time as 1 cycle. Change your script to include the new parameter, you 
 should have:</p>
<div>
	<table cellspacing="0" class="hcp6">
		<tr class="hcp7">
			<td height="40" width="568" class="hcp8"><p><br>
			</p>
			<p>LINE(1,2);[2];[3];</p>
			<p><br>
			</p>
			<p>LINE(1,1,0.25);</p>
			<p>&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;up;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;// 
			 direction</p></td>
		</tr>
	</table>
</div>
<p>Press Update Preview to see your changes, the end result is a system 
 which can be represented as follows:</p>
<p><img alt="" src="../../../images/img_278.jpg" border="0" class="hcp5"></p>
<p>6. Using color tints and opacity</p>
<p>As mentioned above, when assigning colors to shapes, you can also choose 
 a tint and an opacity value, we have already seen how to specify colors 
 by palette number:</p>
<p>[&lt;number&gt;] &#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;example:&#160;&#160;&#160;[1]</p>
<p>However, it is also possible to specify an opacity from 0 to 255 where 
 0 is transparent and 255 is fully opaque:</p>
<p>[&lt;number&gt;,&lt;opacity&gt;] &#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;example:&#160;&#160;&#160;[1,128]</p>
<p>You can also specify a &quot;tint value&quot; from 0 to 1 where 0 is 
 black and 1 is full color:</p>
<p>[&lt;number&gt;,&lt;opacity&gt;,&lt;tint&gt;] &#160;&#160;&#160;&#160;&#160;&#160;&#160;example:&#160;&#160;&#160;[1,128,0.5]</p>
<p>Let's try it out by assigning a partially transparent color to the upward 
 lines. Add the following at the end of the script:</p>
<p>[4,120];</p>
<p>You should now have:</p>
<div>
	<table style="border-width: 0px; margin-left: 24px;" cellspacing="0">
		<tr class="hcp7">
			<td height="40" width="568" class="hcp8"><p>LINE(1,2);[2];[3];</p>
			<p>LINE(1,1,0.25);</p>
			<p>&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;up;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;// 
			 direction</p>
			<p>&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;[4,120];</p></td>
		</tr>
	</table>
</div>
<p>Click Update Preview to apply the changes, you should now notice that 
 the upward lines are partially see-through, and when they pass over the 
 downward lines the colors are blended.</p>
<p>Digging Deeper - Customizing Shapes Using Parameters</p>
<p>While using different shapes allows you to create cool effects, you 
 can also take control of how your shapes behave by using parameters. We 
 have already seen an example of a parameter that changes a shape's behavior 
 above - that is the direction parameter we used to make the LINE move 
 up instead of down.</p>
<p>Before we get started, it helps to know a couple of things about parameters:</p>
<ol>
	<li><p>All shape parameters have a default value. This is the value 
	 that the shape will assume if the parameter is not specified.</p></li>
	<li><p>Parameters come in two flavours, flags and parameters:</p></li>
	<li><p>Flags are kind of like a selector switch for your shape that 
	 alter the behavior in some way, the direction flag is a good example 
	 of a flag parameter. Flags are specified by simply putting the name 
	 of the flag you want to use. For example UP, DOWN, LEFT or RIGHT for 
	 the direction flag.<br>
	<br>
	Here is an example of a flag:<br>
	<br>
	&#160;&#160;&#160;&#160;&#160;&#160;&#160;LEFT;</p></li>
	<li><p>Parameters are used to control a value and consist of a parameter 
	 name and a value in brackets. The size parameter for example specifies 
	 the size of a shape in percentage points:<br>
	<br>
	&#160;&#160;&#160;&#160;&#160;&#160;&#160;SIZE(50);<br>
	<br>
	This tells the shape's size to be 50% of the screen size.</p></li>
</ol>
<p>A full list of parameters is available in the <a href="ScriptingLanguageReference.md">language 
 reference</a>.</p>
<p>1. Using the assistant to set initial parameters</p>
<p>To make it easy to experiment and see how different parameters affect 
 different shapes, you can use the assistant to generate parameters for 
 you, and then simply change the values.</p>
<p>Have fun making your own effects!</p>
