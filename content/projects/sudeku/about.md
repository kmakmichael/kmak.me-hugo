This was the final project for my Advanced Digital Design course in Fall of 2020.
School was fully remote that semester, which made it difficult to work in a team of three.
I worked on the display while my teammates worked on the keyboard input and the game logic.

A pair of 640x480 display buffers are used to display the game.
The framebuffers switch between being written to by the game logic and read from by the display logic.
To save space, pixels are represented by a 3-bit color code, which is exchanged for a proper RGB value before being sent along the VGA cable.

None of us had both a VGA monitor and PS/2 keyboard, so quarantine ended up preventing us from getting together and testing the system as a whole.
We could at least confirm that the display works with the game logic and the game logic works with the keyboard.
More details can be found in our report, found under the Files section.

(pictures will be here, i need to look through my old phone)