# General

![](../../../images/SettingsDialogGeneral.png)  

General settings are split into five areas:

*   [Clip Preview](#clip-preview)
*   [Dashboard](#dashboard)
*   [Show](#show)
*   [Schedule](#schedule)
*   [Display Settings](#display-settings)
*   [Events and Errors](#events-and-Errors)

## Clip Preview
This area contains settings related to clips.

- *Show Clip Names* When enabled, the clip name is shown in the bottom of the clip panel. (This setting is recommended to be on)

- *Enable Global Hotkeys* When enabled, [Global Hotkeys](../advanced/Hotkeys.md) are enabled. This means that the Hotkeys for Screen Monkey will work regardless of which application has focus. With this option enabled the Hotkey will always perform its function. 

- *Generate thumbnail images for clips* This option governs whether thumbnails are generated from the clips’ media content or not. When this option is turned off the default clip logo will be displayed. This may speed up the load time of clips such as video clips as Screen Monkey won’t spend time generating a thumbnail.

- *Generate chapter thumbnails for clips* 

## Dashboard
This area contains settings related to how the Main Dashboard user interface appears in Screen Monkey.

- *Lock to Prevent Edit*

- *Always On Top* When enabled, the Screen Monkey Dashboard window will always be on top of any other windows. This prevents other windows from obscuring the control window.

- *Show Infobar* Whether or not to display the info bar at the bottom of the dashboard which displays information about the mouse over clip or the live clip on the selected layer.

- *Double Click to Play* The default behavior of Screen Monkey is to play a clip when it has been single clicked. If this option is enabled, Screen Monkey will only play a clip if it has been double-clicked.

Style

The drop-down allows you to choose whether the Screen Monkey Dashboard is presented as a Panel or a List.

  

Panel

![](../../../images/img_321.jpg)

List

![](../../../images/img_322.jpg)

Panel Size

The drop-down allows you to choose whether the Screen Monkey Dashboard is presented using Small, Medium or Large panels. This setting is ignored if Screen Monkey is configured to present the Main Dashboard as a List.

![](../../../images/PanelSize.png)

Page Stride

As you resize the Main Dashboard window, the slots are grouped according to pages. The number of slots in any given page is determined by the size of the window and whether Screen Monkey is configured to present Small, Medium or Large clips. The drop-down here allows you more control over how many clips are assigned to a given page.

  

Dynamic

Screen Monkey determines the number dynamically based on Panel Size setting and size of Window.

100

Each Page contains 100 slots.

256

Each Page contains 256 slots.

  

![](../../../images/Tipimage.png)

The 255 clip option is specifically useful when controlling via [DMX](../DMXControl.md) as it ensures that each page fits on a DMX channel.

Toolbox Size

This option allows you to choose whether the Toolbox icons in the Main Dashboard are Large or Small.

![](../../../images/ToolboxSize.png)

  

![](../../../images/Tipimage.png)

Large Toolbox icons are especially useful when using Screen Monkey on a touch screen.

## Show

- *Auto Save* Screen Monkey will automatically save your configuration file after a set amount of time. This means that if the application should close unexpectedly or the computer loses power, your show will be reloaded from the last time it auto saved when you next start the software.

![](../../../images/AutoSave.png)

You can choose to auto save from 1 minute to 1 hour. Or you may choose to turn it off.

- *Auto load show when file is modified*

- *Auto play first clip after show load*

## Schedule

- *Wait for Break before Playing*

## Display Settings

Screen Monkey allows you to work with all sorts of display devices. Additional Monitors, Projection Systems, Lighting Systems, Midi devices, etc. You may configure different profiles that allow you to accommodate different situations and environments.

![](../../../images/DisplaySettings.png)  

Profile

See the [Display Profile](../DisplayProfiles.md) topic for more information.

Use Effect on Clip Out

When enabled, the effect of the last played clip is used to clear the effect when the Clear panel is pressed. If this is set and a fade to black was the last clip run then pressing clear would fade back to the desktop. (It is highly recommended to ensure this setting is enabled.)

## Events and Errors

See the [Events & Errors](../EventsAndErrors.md) topic for more information.

You may also change the size of the thumbnail images of the clips presented in the dashboard. This is controlled by visiting the \[Screen Monkey Settings\](../../reference/setup/Settings/Settings.md). !\[\](../../images/MainDashboard3.png) ## Autosave Additionally, Screen Monkey has an ‘Auto Save’ feature that is enabled by default. The default increment is every 5 minutes, but you are able to change this to suit your taste in \[General Settings\](../Settings/General.md). Choices vary from Never to 1 Hour.