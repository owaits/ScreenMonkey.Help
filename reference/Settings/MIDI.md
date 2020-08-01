# MIDI

The MIDI section in the settings dialog enables you to use a MIDI controller or MIDI keyboard to control Screen Monkey and activate clips.

Set-up is as easy as pressing a key or button on your MIDI controller or MIDI keyboard then double clicking the action that you need to control. Any actions that have keys assigned to them will appear in bold.

![](../../../images/img_325.jpg)

|Setting|Description|
|-|-|
|Channel|MIDI Channel Number 0=MIDI Channel 1|
|Command|This is the MIDI command, which can be; NoteOn, NoteOff, PolyPressure, Controller, ProgramChange, ChannelPressure or PitchWheel.|
|Data1|The MIDI data, for example; note number.|
|Data2|The MIDI data, for example; note velocity.|
|Level|Sets which parameters to ignore when matching the MIDI trigger with the incoming MIDI note.|
|Enabled|Whether Screen Monkey should use this action or not.|

Any action can be triggered by more than one MIDI command so you can assign multiple notes to the same function.

To clear any key assignments you have made, select the action and click the clear trigger button at the top or press the Delete key.

![](../../../images/img_326.jpg)

## Select MIDI Device

If you have more than one MIDI device connected to your computer you may need to select which one Screen Monkey uses. You can do this by clicking on the setup icon in the MIDI settings. This will open a new window from which you can select the MIDI device you want to use.

![](../../../images/img_327.jpg)

## Trigger Level

The MIDI trigger level allows you to specify whether data2 is ignored or used in matching the trigger.

This is useful if you want to change the behavior for different MIDI devices. If we have a MIDI trigger Command = NoteOn, data1 = 16, data2 = 32 and we get a MIDI NoteOn data1 = 16, data2 = 42. With the level set to data1 the action would be executed because the disparity in data2 is ignored. If the level was set to data2 then the action would not occur because the two data2 values are different.

![](../../../images/img_328.jpg)

## Special Actions

Play Clip allows you to play a specific clip on any layer. Each layer supports this action. The data1 parameter is the index of the clip to play on that layer.