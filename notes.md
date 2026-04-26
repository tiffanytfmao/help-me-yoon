'/Users/yushiang/Programs/tiff_game/assets/ajia sad.PNG' '/Users/yushiang/Programs/tiff_game/assets/ajia happy.PNG'

Issue 14:
The end screen doesn't look right
- I see Screenshot 2026-04-26 at 12.24.32 AM
- It should be ./references/Frame 12.png
- The tada effects are still mirrored incorrectly

---

Issue 10:
Currently, the alert animation for the hotspots blinks even when the user has not hovered over a hotspot.
What should happen is:
- When the user hovers over a hotspot, the cursor should become "pixel hand pointer.png" This does not seem to be happening
- Ignore "alert animation.png" for now

Issue 11:
- The hotspots are generally too big and some aren't quite in the right spot
- hotspot-ajia should be
    left: 32%;
    top: 59%;
    width: 6%;
    height: 13%;
- hotspot-isabella should be
    left: 77%;
    top: 53%;
    width: 6%;
    height: 11%;
- hotspot-olivia should be
    left: 0;
    top: 42%;
    width: 50px;
    height: 75px;
- hotspot-joy should be
    left: 60%;
    top: 25%;
    width: 30px;
    height: 40px;
- hotspot-tiff should be
    left: 29%;
    top: 84%;
    width: 62px;
    height: 15%;
- hotspot-empty1 should be
    left: 41%;
    top: 3%;
    width: 14%;
    height: 14%;
- hotspot-empty2 should be
    left: 15%;
    top: 14%;
    width: 30px;
    height: 40px;
- hotspot-empty3 should be
    left: 64%;
    top: 57%;
    width: 8%;
    height: 15%;
- New empty hotspot at
    left: 27%;
    top: 10%;
    width: 100px;
    height: 100px;
- New empty hotspot at
    left: 80%;
    top: 2%;
    width: 70px;
    height: 90px;
- New empty hotspot at
    left: 88%;
    top: 30%;
    width: 30px;
    height: 35px;
- New empty hotspot at
    left: 10%;
    top: 82%;
    width: 70px;
    height: 80px;

Issue 12:
- I see '/Users/yushiang/Desktop/Screenshot 2026-04-25 at 11.57.52 PM.png'
- It should be ./references/Frame 7.png
- The tada effects are mirrored incorrectly
- The person sprite is too small

Issue 13:
- I see '/Users/yushiang/Desktop/Screenshot 2026-04-26 at 12.01.12 AM.png'
- It should be ./references/Frame 11.png
- Person sprites are too small
- Text box is dark and unclickable
- The user cannot advance from this scene

---

Issue 6:
Apologies for issue 1, I uploaded the wrong reference image.
- I see '/Users/yushiang/Desktop/Screenshot 2026-04-25 at 11.26.57 PM.png'
- It should be '/Users/yushiang/Downloads/intro screen 2.png'
- Font is not quite correct
- Missing white outline around "Start Game" button

Issue 7:
The screen immediately after starting the game still doesn't look quite right
- I see '/Users/yushiang/Desktop/Screenshot 2026-04-25 at 11.40.09 PM.png'
- It should be ./references/Frame 1.png
- "Press A To Start" button should not be part of the beige background
- Background should be tinted dark
- Yoon sprite should have shadow

Issue 8:
- I see '/Users/yushiang/Desktop/Screenshot 2026-04-25 at 11.41.29 PM.png'
- It should be ./references/Frame 2.png
- The font for "Yoon" in the dialog box is not correct

Issue 9:
- I see '/Users/yushiang/Desktop/Screenshot 2026-04-25 at 11.42.54 PM.png'
- The "0/5" tab should be moved a bit to the right so that it's not flush against the left edge of the screen

---

Issue 1:
Start doesn't look quite right:
- I see '/Users/yushiang/Desktop/Screenshot 2026-04-25 at 11.26.57 PM.png'
- It should be '/Users/yushiang/Downloads/intro screen.png'

Issue 2:
The screen immediately after starting the game doesn't look quite right
- I see '/Users/yushiang/Desktop/Screenshot 2026-04-25 at 11.28.21 PM.png'
- It should be ./references/Frame 1.png

Issue 3:
The first dialog screen doesn't look quite right
- I see '/Users/yushiang/Desktop/Screenshot 2026-04-25 at 11.28.51 PM.png'
- It should be ./references/Frame 2.png
- Photo and dialog box should be larger
- Missing gap between photo and dialog box

Issue 4:
The 0/5 box at the top doesn't look quite right
- I see '/Users/yushiang/Desktop/Screenshot 2026-04-25 at 11.29.59 PM.png'
- It should be flush against the top of the screen
- The text is a bit hard to read

Issue 5:
When a student is found, this frame looks wrong
- I see '/Users/yushiang/Desktop/Screenshot 2026-04-25 at 11.26.04 PM.png'
- It should be: ./references/Frame 11.png

---

Let's make a game called <game_name>

This is a very simple 2D game that can be implemented as a simple with web app with HTML/CSS and vanilla JS.

The game should begin with a start screen:
- This should show the name of the game, <game_name>
- This should have a button called "Start game"
- This should have use background image <start_game_background_image>

Intro stage:
- The background should transition to <classroom_background>
- After a short delay, the teacher NPC should appear in the background with <teacher_sprite>.
- Clicking on the teacher NPC should start a start a dialog (in a visual novel style)
    - The teacher will say: "<teacher_dialog>"
    - The player can proceed with either "OK" or "No"
        - Clicking "OK" allows the game to proceed
        - Clicking "No" results in:
            - The teacher will say: "<teacher_dialog2>"
            - The player can only proceed with "OK" after this dialog

Student search stage:
- Now the player must use their mouse to search for clickable items in the screen
    - Clicking on the <object1> should show <student1> with dialog: "<student1_dialog>"
    - Clicking on the <object2> should show <student2> with dialog: "<student2_dialog>"
    - Clicking on the <object3> should show <student3> with dialog: "<student3_dialog>"
    - Note: Maybe try to require the objects to be clicks in a certain order? For example, when student1 is found, they give you a key. And object2 can only be obtained with a key
- Once all students are found, the the teacher should say: "<techer_dialog3>"
    - Now the game is complete

Finish screen:
- Show a confetti animation
- Show text like "Congratulations!"
- Show a button called "Restart game"
