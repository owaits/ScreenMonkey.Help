# General

![](../../../images/settings-general.png)  

## Clip Preview
This area contains settings related to clips.

- **Show Clip Names** When enabled the clip name is shown in the bottom of the clip panel. This setting is recommended to be on.

- **Enable Global Hotkeys** When ticked [Global Hotkeys](../advanced/Hotkeys.md) are enabled. This means that the Hotkeys for Screen Monkey will work regardless of which application has focus. With this option enabled the Hotkey will always perform its function. This setting is recommended to be off.

- **Generate thumbnail images for clips** This option governs whether thumbnails are generated from the clips’ media content or not. When this option is turned off the default clip logo will be displayed. This may speed up the load time of clips such as video clips as Screen Monkey won’t spend time generating a thumbnail. This setting is recommended to be on.

- **Generate chapter thumbnails for clips** creates additional thumbnails throughout the clip. This setting is recommended to be off.

## Dashboard
This area contains settings related to how the Main Dashboard user interface appears and behaves in Screen Monkey.

- **Lock to Prevent Edit** Prevents new clips from being created.

- **Always On Top** When enabled, the Screen Monkey Dashboard window will always be on top of any other windows. This prevents other windows from obscuring the control window.

- **Show Infobar** Whether or not to show the info bar at the bottom of the dashboard which displays information about the mouse over clip or the live clip on the selected layer.

- **Double Click to Play** The default behavior of Screen Monkey is to play a clip when it has been single clicked. If this option is enabled, Screen Monkey will only play a clip if it has been double-clicked.

- **Style** The drop-down allows you to choose whether the Screen Monkey Dashboard is presented as a grid panel (recommended) or as a list. The list view is useful for re-ordering clips or viewing a lot of clips on screen.

- **Panel Size** The drop-down allows you to choose whether the Screen Monkey Dashboard is presented using Small, Medium (recommended) or Large panels. This setting is ignored if Screen Monkey is configured to present the Main Dashboard as a List.

- **Page Stride** As you resize the Main Dashboard window, the slots are grouped according to pages. The number of slots in any given page is determined by the size of the window and whether Screen Monkey is configured to present Small, Medium or Large clips. The drop-down here allows you more control over how many clips are assigned to a given page. [Learn more about these options](../pages.md).

- **Toolbox Size** This option allows you to choose whether the Toolbar icons at the top of the Main Dashboard are Large (default) or Small.

## Show
Configure Screen Monkey show files.

- **Auto Save** Screen Monkey will automatically save your show after a set amount of time. This means that if the application should close unexpectedly or the computer loses power, your show will be reloaded from the last time it auto saved when you next start the software. You can choose to auto save from 1 minute to 1 hour or you may choose to turn it off. Recommended setting is 5 minutes.

- **Auto load show when file is modified** With this option enabled you can replace the live show file with an updated version and Screen Monkey will load and activate it. This maybe useful for remote management of Screen Mokney installations.

- **Auto play first clip after show load** Often used in conjuction with the previous setting. When the show is loaded the first clip is played without user intervention.

## Schedule
Screen Monkey can run cilps on a timed schedule. Learn more about [scheduling clips](../clipSettings/schedule.md).

- **Wait for Break before Playing** When enabled this setting will prevent scheduled clips playing if a manually triggered clip is active. The scheduled clip will play as soon as the manual clip completes.

## Display Settings
Screen Monkey allows you to work with all sorts of display devices. Additional Monitors, Projection Systems, Lighting Systems, MIDI devices, etc. You may configure different profiles that allow you to accommodate different situations and environments. See [Display Profiles](../toolbar/display.md) for more information.

- **Use transition effects when clips are cleared** If enabled then when a clip is cleared from a layer it will use the clip transition if one is set. It is recommended this setting is enabled.

## Events and Errors
Clicking the 'Show Event Log' button here will open the log. See [Events and Errors](../EventsAndErrors.md) for more information.
