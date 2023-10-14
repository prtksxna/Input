# Frequently Asked

&nbsp;

Common issues encountered by fellow library users are presented below along with known solutions. Please feel free to [join us on Discord](https://discord.gg/8krYCqr) for further discussion and [open an Issue on GitHub](https://github.com/JujuAdams/Input/issues?q=is%3Aissue+is%3Aopen) if you find a persistent problem with the library.

&nbsp;

<details><summary>

### I have connected a gamepad but verbs aren't activating, or are behaving strangely
</summary>

1. Check if your gamepad is working OK on an OS level. On Windows, use the Game Controllers dialogue. See [Gamepad Troubleshooting](Gamepad-Troubleshooting) for additional details
2. Download the [example project](https://github.com/JujuAdams/Input/archive/refs/heads/master.zip) from GitHub and try out the `obj_gamepad_tester` object. This helps visualize what's going on with your gamepad. You may need to cycle through gamepad indexes in some cases
3. Have a look at the [Output log](https://i.imgur.com/gy3CUcu.png) for more information on gamepad connection. If you need to follow up for additional help, we will need you to share the information you see here.

Some common issues to consider: remappers like Steam Input, DS4Windows, etc. may cause trouble, so try quitting these. Nintendo Switch controllers do not work on many platforms over USB, so try Bluetooth instead. Some devices require additional setup, see [Gamepad Troubleshooting](https://www.jujuadams.com/Input/#/6.2/Gamepad-Troubleshooting) for additional details
</details>



<details><summary>

### How do I check if the player is (or is not) using gamepad?
</summary>

Check the player with [`input_player_get_gamepad()`](Functions-(Players)?id=player_get_gamepad), or the source device with [`input_source_using(INPUT_GAMEPAD)`](Functions-(Sources)?id=input_source_usingsource-playerindex)
</details>



<details><summary>

### How can I check analogue input values (eg. trigger, thumbstick)?
</summary>

1. Set up your bindings using `input_binding_gamepad_axis()`
2. Check verbs using `input_value()`
</details>



<details><summary>

### How do I set up aiming for both mouse and gamepad thumbstick?
</summary>

[Cursor functions!](Functions-(Cursor))<br>
For a sophisticated example, refer to the [GitHub example project](https://github.com/JujuAdams/Input/archive/refs/heads/master.zip), specifically the `obj_example_tds_player` object.
</details>


<details><summary>

### Does Input support Steamworks?
</summary>

[Yes, using the official extension](Steamworks)
</details>



<details><summary>

### How many simultaneous gamepads are supported?
</summary>

OS limitations [per GameMaker](https://manual.yoyogames.com/GameMaker_Language/GML_Reference/Game_Input/GamePad_Input/Gamepad_Input.htm):

Windows XInput, Apple, PlayStation, Web: 4<br>
Windows DInput, Switch, Xbox: 8<br>
Linux, Android: Many<br>

?> Regarding DInput and XInput: https://wikipedia.org/wiki/DirectInput#DirectInput_vs_XInput
</details>



<details><summary>

### How do I update my project to a newer Input version?
</summary>

1. Backup edited config scripts
2. Delete Input folder
3. Import new release
4. Copy old config changes to new

_Note: This process is easiest if your project is version control managed_
</details>



<details><summary>

### How do I save and load player preferences?
</summary>

Using [Export and Import](Functions-(Exporting-and-Importing))
</details>



<details><summary>

### How can multiple players share the keyboard or one gamepad between them?
</summary>

1. Set Source mode to `FIXED`
2. Use `input_source_share()`
3. Set bindings per player directly, or using profiles
</details>



<details><summary>

### How can I ensure gamepads work correctly when running the GM IDE through Steam?
</summary>

[Disable Steam Input](https://i.imgur.com/cGdlVJO.png) for Game Maker Studio 2 Desktop. Alternatively, [use the Steamworks extension](Steamworks) 
</details>



<details><summary>

### What platforms are extended gamepad features availble on?
</summary>

1. **Vibration:** Consoles, Windows (Xbox pads, PS and Switch through Steamworks)
2. **LED Patterns:** Consoles, iOS, and Windows through Steamworks
3. **Motion:** PS and Switch, Windows and Linux through Steamworks
4. **RGB:** PS Consoles, Windows and Linux through Steamworks
5. **Trigger Effects:** PS5, Windows through Steamworks
6. **Touchpad:** PlayStation Consoles
</details>



<details><summary>

### Input is impacting my game's FPS!
</summary>

Input is tested across platforms and we have yet to observe any scenario where it is the culprit for poor game performance. However, we recieve many false performance reports as a result of debugging confusion. 

If you believe Input is impacting performance based on profiler readings, examine Time (Ms) and ignore Step (%). Unless Input is significantly contributing to a total Time (Ms) that is greater than your frame target (eg 17ms) the problem is elsewhere. 

Some known culprits are shaders, driver issues (Xbox controller related), and debugger Watches, all of which impact FPS in ways unrelated to the library which the profiler may not make obvious. Feel free to pursue help for general performance problems, but do not rely on Step (%) for diagnosing or reporting library performance issues — Time (Ms) values only!
</details>



<details><summary>

### Input does a lot of logging, how can I suppress it while debugging?
</summary>

Set `__INPUT_SILENT` in `__input_macros()` to true to suppress most of Input's logging. Some critical messages will still be logged. Please note that we cannot provide any support for any issues you have with Input if you use this configuration. 
</details>



<details><summary>

### How can I ensure gamepads work correctly when running the GM IDE through Steam?
</summary>

Disable Steam Input for GameMaker Studio 2 Desktop. Alternatively, use the Steamworks extension.
</details>



<details><summary>

### How should I include Input in my game credits?
</summary>

Input Library: Juju Adams, Alynne Keith, and friends
</details>