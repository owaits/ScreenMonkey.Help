# Effect Generator Scripting Reference

This page contains reference information for the Effect Generator scripting language. For an introductory tutorial read [Creating Your Own Effects Scripts](CreatingCustomEffects.md).

## Syntax Overview

A brief outline of the general syntax for the scripting commands.

### Color Scheme Definitions
Color scheme definitions can appear anywhere in your script, although convention is to put them at the start. Scheme definitions are not indexed must appear in palette order. To change the palette order change the order of the definitions.

#### Color Scheme Definition
Specify values between 0 and 255 for each of red, green, blue.

    COLOR({red},{green},{blue});

#### Background Color Definition
When defining Color scheme, the background Color can also be specified.

    BACKGROUND({red},{green},{blue});

#### Color Scheme Example

The following is an example of a full color scheme definition block including all 4 palette colors:

![](../../../images/ColorsAdded.png)

### Shape Definitions

#### Shape Timing definition

The Shape Timing definition consists of the shape name and from 1 to 3 timing parameters. The second and third timing parameters are optional.

    {shapename}({pulsetime},{lifetime*},{delaytime*});

|Parameter|Description|
|-|-|
|Pulse Time|Defines the period (in cycles) between generation of new shapes.|
|Life Time|If omitted, is the same as pulse time. Otherwise,  specifies the lifespan for each generated shape (in cycles).|
|Delay Time|Is the delay period (in cycles) before shapes begin to be generated, useful for offsetting shapes from each other (forcing them 'out of phase' with one another).|

The following example shows a BOX shape with a pulse time of 2 cycles and life span of 3 cycles and no delay:

    BOX(2,3);

#### Shape Parameters

Shape parameters follow the shape definition. There are 3 types of supported parameters and they can appear in any order following the shape definition:

#### Color Palette Mappings

    [{index},{opacity*},{tint*}];

|Name|Description|
|-|-|
|Index|Color palette number to use|
|Opacity|Optional transparency value from 0 (transparent) to 255 (opaque)|
|Tint|Optional darkness of the specified Color from 0 (black) to 1 (full color)|

Each shape supports a number of mappable color slots. Slot 1 and Slot 2 always correspond to the fill color for the shape, and the border color for the shape respectively. Some shapes support more than one color.

To map palette colors to shape color slots specify the colors in order. For example to map color 2 to fill and color 3 to border, use the following:

    [2];[3];

You may optionally specify opacity values for each color mapping:

    [2,128];[3,160];

And tints if you require:

    [2,128,0.5];[3,160,0.5];

#### Flags

Flags are simple one-word parameters which change the shape's behaviour, there are two supported flag sets: fade and direction. To specify the flag just enter the flag name you want to use. The flag sets are as follows:

* Fade supports FADE, FADEIN and NONE. These correspond to fade from fully opaque to transparent during the shape's lifetime; the reverse effect, and no fade (fully opaque always).
* Direction supports UP, DOWN, LEFT and RIGHT. These correspond to directions of travel.

While it's possible to specify multiple flags from the same flag set, this makes no sense as flags within a set are mutually exclusive. 

#### Parameters

Parameters are like flags except that they take a value as well, which affects how the shape behaves. Parameters are discusses in more detail in the shapes section below. Parameters always have the following form:

    {name}({value});

#### Supported Shape Types

|Shape|Description|
|-|-|
|BLOCK| |
|BOX|Creates a box which appears at a random location and expands to a random size. Defaults to the fadein fade type. The maximum size may be overridden using the size parameter.|
|BUBBLE|Creates a bubble which appears at a random location along the bottom of the screen and rises to the top. The size is chosen at random but may be set to a fixed size using the size parameter or a minimum size specified using the min parameter.|
|CHEVRON|Creates a chevron which moves across the screen. The sweep parameter specifies the angle of the chevron as a percentage of the screen size.|
|CIRCLE|Creates a circle which appears at a random location and expands to a random size. Defaults to the fadein fade type. The maximum size may be overridden using the size parameter.|
|CONFETTI|Small falling triangles|
|DIAMOND|Creates a diamond which appears at a random location and expands to a random size. Defaults to the fadein fade type. The maximum size may be overridden using the size parameter.|
|LEAF|Creates a leaf shape at a random location along the top of the screen which floats downward. Size is selected at random or may be overridden using the size or min parameters.|
|LINE|Creates a horizontal or vertical line that moves across the screen. The size of the line is selected at random or may be specified using the size parameter. The line begins at the screen edge.|
|LINEM|Creates a horizontal or vertical line that moves across the screen. The size of the line is selected at random or may be specified using the size parameter. The line begins in the middle of the screen.|
|RADAR|Spinning block with one corner in the centre of the screen.|
|ROTOR|Spinning block.|
|SNAKE|A line which moves and turns corners (inspired by the snake game).|
|SNOWFLAKE|Creates a snowflake shape at a random location along the top of the screen which floats downward. Size is selected at random or may be overridden using the size or min parameters.|
|STAR|Creates a star shape at a random location along the top of the screen which floats downward. Size is selected at random or may be overridden using the size or min parameters.|
|STROBE| |
|VUMETER| |

#### Shape Parameters

Some parameters are supported by all shapes and some by only a few, see the table below for which parameters are supported by which shapes. The following is a description of each parameter and the values it will accept.

|Parameter|Range/Values|Description|
|-|-|
|size()|percentage|Sets the maximum (or fixed) size for a shape. Specified as a percentage of the screen size, can exceed 100% if you want a large shape. Example: `SIZE(50);` Note: do not include the % sign!
|border()|pixels|Sets the border width for the shape. Specified in pixels. Example: `BORDER(4);`|
|min()|percentage|Sets the minimum size for a shape which supports random size such as BUBBLE and CIRCLE. Example: `MIN(10);` Note: min should be less than size!|
|sweep()|percentage|Sets the sweep angle for the CHEVRON shape. Example: `SWEEP(50);`|

### Shape Parameter Support and Color Slot Mapping Table

The following table summarizes the parameters and flags supported by each shape.

![](../../../images/img_279.jpg)