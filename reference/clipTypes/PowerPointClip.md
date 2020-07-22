![](../../images/PowerPointIcon.png) 
# PowerPoint Clip

PowerPoint is a Microsoft Office product for creating and displaying slide based presentations. Many organizations use PowerPoint to create and present content.

By using the PowerPoint Clip you can play a PowerPoint presentation file directly from within ScreenMonkey. When using this clip type you have full control of the presentation including the ability to advance the slides forwards and backwards and to trigger slide element animations (eg, bullet points which appear one at a time).

## Create a PowerPoint Clip
Click an empty slot and choose the PowerPoint clip, you are presented with a file browsing dialog from which you may browse the Windows file system and select the PowerPoint presentation you wish to use.

It may take a few moments for the clip to load depending on the size of the presentation. Once the presentation has loaded you will see a thumbnail image of the first slide in the presentation.

## Configure a PowerPoint Clip
There are a few clip settings which can be adjusted for PowerPoint clips.

**Start Slide** You may wish to begin the presentation at a specific slide number. Right-click the clip and choose Start Slide > Slide Number.

**Auto Rewind** Normally when you move to another clip or clear the screen the presentation is rewound back to slide 1. However if you turn Auto Rewind off under the PowerPoint Playback Settings then the presentation will be run from the slide being viewed when the clip was last stopped.
<!--
**Loop** With this option set the presentation will loop back to the first slide when it reaches the last slide. This option can be set in PowerPoint and if set will be shown as such in Screen Monkey. However you can override this setting by selecting loop and toggle whether the presentation is looped or not.
-->
## Use a PowerPoint Clip in a show
Like other clips, you click once on the clip to begin presenting. 

### Control from the dashboard
The simplest way to control the presentation is to use the dashboard icon. 

- Left clicking on the icon will advance to the next slide or show the next animation (bullet point) on the current slide. When you reach the end of the presentation the final slide will be shown and left clicking will have no effect.

- To move the animations or slides backwards hold the Shift key and left click.

<!-- Control Click -->

### Using the Preview Window
If you require more control over the flow of the presentation open the preview window for the layer the PowerPoint clip is playing on.

![](/images/clip-powerpoint-preview.png)

The preview window will show a thumbnail for every slide in the presentation in a column on the left. Note that the *preview* will show the slide after all animations have been run. Clicking a preview thumbnail will display that slide. Clicking again will run any animations. To disable a slide right click the preview thumbnail and untick 'Active'.

A large preview of the currently playing slide will on the right. At the top there are left and right arrow buttons for moving forwards and backwards.

Below the preview there is a status bar showing the current slide number, total slide count, current animation and total animations for the current slide.

![](/images/clip-powerpoint-preview2.png)

In this screenshot slide 2 is active (white border), slide 3 is disabled (grey border), and slide 4 is coming up (no border). 

## Using a Remote Control
Sometimes a speaker will want to advance the presentation themselves. They can do this by means of a wireless remote clicker. Screen Monkey has been tested with the Logitec Wireless Presenter R400 but other makes and models will work if they are reconginsed by Windows as pointing devices. No special configuration should be necessary.

<!--
## Export Cue Sheet
A PowerPoint clip can be exported in a few ways. Right-click on the clip and choose Export Cue Sheet.

- Cue sheet XML (single file)
- Enhanced podcast chapter album art with XML (zip archive)
- Image files with XML (zip archive)

To export the clip right click on the dashboard icon and then choose 'Export Cue Sheet'. A new dialog opens which allows you to choose the cue list and then the type of export you require.
-->