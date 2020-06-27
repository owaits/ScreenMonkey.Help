# Statistics
Screen Monkey can create a CSV (Comma Separated Variable) log of the clips which have been played. This feature is enabled in the Statistics section of the Settings dialog.

![](../../../images/settings-stats.png)  

## Purpose
There are several uses for this feature.

- An 'as run' log is essential in some TV stations to record the time advertisements are played
- A church may wish to see how often a song has been used
- For checking automated schedule items played as intended when Screen Monkey is unattended
- Logging playback of music clips for the payment of royalties or fees

## Enabling Statistics

1. Click to place a check mark in the Enabled check box. This will enable the feature and allow you to choose the name and location of the logging file.
2. Click the Browse button on the far right to open a Windows Save As dialog.
3. Browse to where you wish to store the logging file, type a suitable name, (eg `asrun.csv`) and click Save.
4. Click OK to close the Settings dialog

The log file will now be created and updated every time a clip is played.

## Viewing the statistics logfile
After you have run a show with statistics logging enabled you will be able to view the data you have collected.

To do this use the Windows File Explorer and locate the log file and open it using the application of your choice. A variety of spreadsheet or text editor applications may be used to view the file.

An example logfile is shown below. 

    21/06/2020 21:19:44,1,51052f36-8918-4b61-ac8e-aabc141fb09e,Blank 1,Playing
    21/06/2020 21:19:48,1,1fb61cf7-5d28-425b-b9d3-0d1e89220170,Blank 2,Playing
    21/06/2020 21:19:50,1,77c4ffdd-b791-4cde-aa04-42a41787515f,152-BR-3-CD,Playing
    21/06/2020 21:19:53,1,959c72ff-6a8a-4279-bcb8-0295aa71f955,Blank 8,Playing
    21/06/2020 21:20:12,1,1c8c8848-97eb-488c-9154-1541b3c132b3,152-BR-1-CD,Playing
    21/06/2020 21:20:38,0,00000000-0000-0000-0000-000000000000,,Playing
    21/06/2020 21:20:39,1,1c8c8848-97eb-488c-9154-1541b3c132b3,152-BR-1-CD,Playing
    21/06/2020 21:20:40,2,68cf5202-2606-491d-b955-13b2b9908a9d,152-BR-2-CD,Playing
    21/06/2020 21:20:41,3,425550a2-2e55-4723-bedb-3af7969fde93,152-BR-3-CD,Playing
    21/06/2020 21:20:42,4,77c4ffdd-b791-4cde-aa04-42a41787515f,152-BR-3-CD,Playing
    21/06/2020 21:20:42,0,00000000-0000-0000-0000-000000000000,,Playing
    21/06/2020 21:22:47,1,1c8c8848-97eb-488c-9154-1541b3c132b3,152-BR-1-CD,Playing
    21/06/2020 21:22:48,0,00000000-0000-0000-0000-000000000000,,Playing
    21/06/2020 21:23:19,0,959c72ff-6a8a-4279-bcb8-0295aa71f955,Blank 8,Playing
    21/06/2020 21:23:20,0,00000000-0000-0000-0000-000000000000,,Playing
    21/06/2020 21:23:33,0,fce10bf9-87dd-40e6-8fac-16ce7f17fa81,Song,Playing
    21/06/2020 21:23:34,0,00000000-0000-0000-0000-000000000000,,Playing
    21/06/2020 21:23:42,0,7d03b513-6b01-4b11-b742-dcee3be04613,01 For What It's Worth.m4a,Playing
    21/06/2020 21:23:48,0,7d03b513-6b01-4b11-b742-dcee3be04613,01 For What It's Worth.m4a,Paused
    21/06/2020 21:24:04,0,7d03b513-6b01-4b11-b742-dcee3be04613,01 For What It's Worth.m4a,Playing
    21/06/2020 21:27:58,0,7d03b513-6b01-4b11-b742-dcee3be04613,01 For What It's Worth.m4a,Finished

Each column is separated by a comma.

|Column number|Column letter|Item|Description|
|-|-|-|-|
|1|A|Date And Time|Date and Time the event was logged|
|2|B|Layer|The layer the clip is playing on. The Audio is 0, Layer1 is 1, Layer2 is 2 etc.|
|3|C|Handle|Each clip has a unique identifier which is logged here. If the identifier shows all zeros then it is a clear layer clip.|
|4|D|Clip Name|This is the name of the clip|
|5|E|Action|This is the action that occurred - Playing, Paused, Finished|

*Note:* If a clip is faded in or faded out using the Layers Dashboard then these actions are not logged.
