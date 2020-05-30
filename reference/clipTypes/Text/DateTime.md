# Date and Time Formatting
A few [text clip objects](TextClipObjects.md) display times and/or dates. Screen Monkey gives you complete control of how time and date is formatted and allows you to combine dates and times with static text. This flexibity requires a little bit of complexity.

The way Screen Monkey formats dates and time is based on a common set of letter abreviations which are listed below together with examples. Take care to understand how these work and when the special escape character is required.

## Date Time Formats
|Code|Meaning|Example|
|--|--|--|
|h|Hours in 12-hour format|1 to 12|
|hh|Hours in 12-hour format with leading zero|01 to 12|
|H|Hours in 24-hour format|1 to 24|
|HH|Hours in 24-hour format with leading zero|01 to 24|
|m|Minutes|0 to 59|
|mm|Minutes with leading zero|00 to 59|
|S|Date time value converted to seconds (used in countdown captions)|-|
|s|Seconds|0 to 59|
|ss|Seconds with leading zero|00 to 59|
|f|Tenths of a second|0 to 9|
|ff|Hundredths of a second|00 to 99|
|fff|Milliseconds|000 to 999|
|t|A or P|A or P|
|tt|AM or PM|AM or PM|
|d|Day of the month|1 to 31|
|dd|Day of the month with leading zero|01 to 31|
|ddd|Day of the week, abreviated|Tue|
|dddd|Day of the week, full|Tuesday|
|M|Month of the year in decimal format|1 to 12|
|MM|Month of the year in decimal format with leading zero|01 to 12|
|MMM|Month in text, abreviated|Jun|
|MMMM|Month in text, full|June|
|yy|Year, last 2 digits|00 to 99|
|yyyy|Year, full 4 digits|0001-9999|
|\\|The escape character| |


Additional uncommon codes (f,F,g,K,etc) are omitted from the table but maybe found online by searching for custom date and time format strings.

## Escaping Special Characters
Sometimes the date and time string is contained within other text. For example you might want to write `Here is the time: 12:45` or `Next Meeting at 13:00`. The problem with these examples is that Screen Monkey doesn't know which characters are regular letters and which are date time placeholders. 

To identify a character as a regular letter instead of a placeholder you place a backslash `\` before it. In the examples above these letters need to be escaped - H, t, s, h, m, M, g - because they have time or date meanings. The format strings must be re-written as `\Here i\s \t\he \ti\me: HH:mm` and `Nex\t \Mee\tin\g a\t HH:mm`

If you see strange results when displaying your clip then you are probably missing an escape character.

## Examples
A few examples you may find helpful.

|Example|String|
|-|-|
|24 hour clock with seconds|HH:mm:ss|
|24 hour clock|HH:mm|
|12 hour clock|h:mm tt|
|European date format|dd/MM/yyyy|
|North American date format|MM/dd/yyyy|
|Date and time together|dd/MM/yyyy h:mm|
|The time with static text|T\he \ti\m\e i\s h:mm|