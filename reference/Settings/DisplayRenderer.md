# Display Renderer

When a clip is played and appears on the screen it uses a display renderer to actually display the clip. The renderer also handles mixing the layers together as well as the effects and animations. Screen Monkey allows you to choose a different renderer for both the main output and the stage output.

![](../../../images/settings-display-main-2.png)

![](../../../images/settings-display-stage-2.png)

Each renderer has different functionality and compatibilities, so you need to choose a renderer that is right for your application.

## Disabled
Do not display anything on this output.

## Standard (Recommended)
The standard renderer uses the Microsoft GDI and DirectX technology to display clips to the screen. This renderer is compatible with all clip types but only supports 2D graphics and simple transition effects.

## Blackmagic Decklink (Pro Feature)
Output to a [Blackmagic Decklink](https://www.blackmagicdesign.com/products) HDMI or SDI card installed in the computer. The video resolution and frame rate can be set here.

## NDI (Pro Feature)
Create a new [NDI](https://ndi.tv) source on the local network. Any NDI compatible devices or applications can decode and display this output.

## Pixel Mapper (Pro Feature)
In conjunction with a DMX output profile enables output to pixel mapped displays.

## Fast Renderer
In development.

## WPF (Experimental)
This uses the latest WPF technology built into Windows to display the clips to the screen. It supports 3D graphics and allows for more elaborate transition effects. You may also notice that the animations are smoother with higher performance. Currently not all clip types will play in this renderer but this will be resolved in a future version.