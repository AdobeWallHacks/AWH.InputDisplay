# AWH.InputDisplay
A little in-game input display.
Keys light up when you press them.

## Settings
vector Position
- Position on the screen as a ratio of screen size

bool horizontal
- Whether the text is inline horizontally or stacked vertically

bool renderOnCockpit
- Determines the UI topography.
- Enabling this makes the UI curved, and lets it bob with player movement.
- Disabling this make the UI flat, and static.

- My reccomendation is if you plan to place this next to other ui (such as the bottom left corner),
- enable it so that it blends well together.

float size
- Size of the text

bool justifyLeft
- Determines whether the text is justified to the left or to the right of the Position
- Disable this if you are going to place this on the right-edge of your screen

float padding
- Distance between keys as a ratio of screen size
- To avoid having an unintuitively small number here, this number is in hundredths. (padding 1 = a 0.01% gap between keys)

float textAlpha
- Transparency of the display as a percentage
- 0 = Invisible, 1 = Fully Opaque

vector onColor
- Text color when the key is pressed, as RGB

vector offColor
- Text color when the key is not pressed, as RGB

array<int> keyListeners
- These are the commands the script checks with the engine to determine whether an input is pressed.
- The effect of this is that it is bind-independent. 
- When you croutch, the script doesnt know what key you pressed to get there, just that you did.
- The keyDisplays settings exists as a result.

array<string> keyDisplays
- These are the strings that will actually appear on the UI.
- You can set them to the actual keys you're pressing, or simply the names of the commands themselves.
- The script will automatically resize everything based on the text length.

In regards to the Listener Display array pair, I've included every command I feel someone would want.
By default, listeners for movement keys are enabled. 
To enable more, uncomment (remove the // from the front of) the command and display text from both arrays.
Just make sure that theres the same amount in both.

TODO:
- A 'compact' mode where only keys that are pressed are displayed
