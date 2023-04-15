# Functions (Color)

&nbsp;

Gamepad color can be set for PlayStation console platforms, as well as on [Windows or Linux when the Steamworks extension is configured](Steamworks.md) adding Xbox Elite Series 2 and Steam Controller support.

?> Color functions are relevant on PS4 and PS5 platforms as well as Windows or Linux using Steamworks, and apply to PS4, PS5, and Xbox Elite 2 gamepads.

&nbsp;

## …color_get

`input_color_get([playerIndex])`

<!-- tabs:start -->

#### **Description**

**Returns:** [Color](https://manual.yoyogames.com/GameMaker_Language/GML_Reference/Drawing/Colour_And_Alpha/Colour_And_Alpha.htm)

|Name           |Datatype|Purpose                                             |
|---------------|--------|----------------------------------------------------|
|`[playerIndex]`|integer |Player to target. If not specified, player 0 is used|

Gets the LED color of a player's gamepad.

#### **Example**

```gml
//TODO lol
```

<!-- tabs:end -->

&nbsp;

## …color_set

`input_color_set([playerIndex])`

<!-- tabs:start -->

#### **Description**

**Returns:** N/A (`undefined`)

|Name           |Datatype|Purpose                                                                                                                                                    |
|---------------|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
|`color`        |color   |[Color](https://manual.yoyogames.com/GameMaker_Language/GML_Reference/Drawing/Colour_And_Alpha/Colour_And_Alpha.htm) to set the player's gamepad source LED|
|`[playerIndex]`|integer |Player to target. If not specified, player 0 is used                                                                                                       |

Sets the LED color of a player's gamepad.

#### **Example**

```gml
//TODO lol
```

<!-- tabs:end -->

&nbsp;

## …color_reset

`input_color_reset([playerIndex])`

<!-- tabs:start -->

#### **Description**

**Returns:** N/A (`undefined`)

|Name           |Datatype|Purpose                                             |
|---------------|--------|----------------------------------------------------|
|`[playerIndex]`|integer |Player to target. If not specified, player 0 is used|

Resets the player's device's LED colour.

#### **Example**

```gml
//TODO lol
```

<!-- tabs:end -->