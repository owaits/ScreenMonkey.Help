# Statistics

Click the area of interest on the image below to learn more about that option.

![](../../../images/SettingsStatistics.png)  

Screen Monkey offers the ability to log statistical information about a show. This will allow you to save the information to a playback log in CSV format. (CSV means Comma Separated Value)

## Why might this be useful?

This can be very useful in TV stations to record the air time a particular advertisement has been played.

Perhaps you are using Screen Monkey for a church service and you wish to see how it has been used in order for planning. You want an automated way to know the timing of when certain elements of Screen Monkey were used.

## Turning on Statistics

Click to place a check mark in the Enabled check box.

![](../../../images/LogEnabled.png)

This should enable the option and allow you to choose the name and location of the logging file.

Click the Browse button on the far right of the field to open a Windows File Browsing dialog.

![](../../../images/LogFileLocation.png)

Browse to where you wish to store the logging file, type a name to identify the file and click Save.

## Viewing a saved Statistics file

After you have worked your way through one or more shows with statistics logging enabled you will likely wish to view the data you have collected.

To do this, you must use the Windows File Explorer and locate the file and open it using the application of your choice. A variety of applications may be used to view the file. In this case, the screen capture depicts using Microsoft Excel to view the file.

You may find that double-clicking the file causes Windows Notepad or another application to open. The application that opens depends on what the .CSV file type has been [associated](../FileAssociation.md) with in Windows.

![](../../../images/ViewLogFile.png)

The image above was shaded using different colors to better illustrate the data captured.

  

A

Date And Time

As you might expect, this is the Date and Time the clip was played or cleared.

B

Layer

This is the layer the clip is playing on. The number here begins at zero, so Layer 1 is 0 and Layer 4 is 3.

C

Handle

Each clip has a unique handle number. This is the handle number assigned to the clip.

D

Clip Name

This is the name of the clip that was played or cleared.

E

Action

This is the action that occurred.  
   
Playing means the clip was played  
Paused means a video or other timed clip was paused  
Finished means a video or other timed clip played until it reached its end  
NoItem means the clip was cleared.


![](../../../images/Noteimage.png)

While it's not obvious from the example above, if a Clip is playing and is faded in or out of view using the Layers Dashboard, these actions are ignored and not logged.  
   
If it's important to you to know when the clip was made visible to your audience, you need to ensure you play it when you want it to appear, then clear it when you want it to disappear and avoid playing, then using the Layers Dashboard to fade it into and out of view.