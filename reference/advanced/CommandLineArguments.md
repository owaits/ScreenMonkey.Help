# Command Line Arguments

You may use a variety of command line arguments to control Screen Monkey. You will need to browse the installation folder using the cd command first. Below is a list of supported commands.

`ScreenMonkey.exe {filename} /play {clip_index} /layer {layer_index} /go /pause /next /previous /clear /clearall`

|Parameter|Description|
|-|-|
|`{filename}`|The name that was used to save the show|
|`/play {clip_index}`|Plays the clip at the specified index. `{clip_index}` = the handle index of the clip to play
|`/layer {layer_index}`|Changes the active layer. `{layer_index}` = the index of the layer to make active|
|`/go`|Manual activation of linked clips|
|`/pause`|Pauses the current clip|
|`/next`|Moves to the next clip or the first clip if on clear|
|`/previous`|Moves to the previous clip|
|`/clear`|Clears the active layer|
|`/clearall`|Clears all layers|
|`/debug`|Opens the developer console which is a window that developers can print messages to for debug purposes|