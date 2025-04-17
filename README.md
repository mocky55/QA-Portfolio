# QA-Portfolio
My bug reports and testing work for Toby's Island



# QA Portfolio – Peter Langmayr (Broockle)

## Toby's Island – Volunteer QA

QA Portfolio Entry #1
Softlock & Progression Block: Teleporter Logic Break
Game: Toby’s Island
Type: Game-breaking bug
Summary:
Player was unable to reach a major boss (Asmodeus) due to teleport logic breaking after using a fast-travel point.

Reported Behavior:

“There’s no way to redo the boat ride in the lava tubes. You can’t reach Asmodeus if you teleport back and change the teleporter.”

Follow-up:
Later discovered a secondary teleporter bug:

“The teleporter in the desert didn’t anchor the position. When I used the village teleporter it brought me back to the teleporter I used before the desert.”

Impact:
Highlighted multiple edge cases in the game's teleportation system. Dev flagged it as a priority to patch.

✅ Portfolio Value: Shows how you think about progression systems, player access, and how bugs can cascade.



QA Portfolio Entry #2
Crash During Boss Battle: Counterattack Logic Failure
Game: Toby’s Island
Type: Crash / Scripting logic
Summary:
During a boss battle against the “Prince,” a crash occurred when using a character with counterattack abilities.

Reported Behavior:

“I think I KOed the defending Marl just as it crashed. The prince was still full HP.”

Technical Insight:

Crash was traced to a nil error in a large custom battle script (>3000 lines)

Dev identified faulty line turn_end if @subject.dead? as cause

Bug occurred when a subject died mid-action, leading to null reference

Dev response:

“That error just gave you a glimpse into how huge the battle engine is... I think snipping that line out fixes it.”

Impact:
Bug was identified, recreated, and fixed collaboratively. You even suggested other mechanics like "rage abilities" while reviewing balance.

✅ Portfolio Value: Demonstrates debugging support, system thinking, and collaborative problem-solving.




QA Portfolio Entry #3
Data Loss from Debug Function: Ignarius Character Overwrite
Game: Toby’s Island
Type: Save corruption / Dev tool conflict
Summary:
The debug NPC "Bug Bunny" unintentionally overwrote a player's character when certain save conditions were met.

Reported Behavior:

“I can't pick up my Ignarius Marl anymore. I stashed him earlier to avoid the evolution... now I can’t retrieve him.”

Discovery Path:

Recreated the bug using a save from 20 minutes prior

Traced issue to interaction with dev tool character

“It's the debug bunny. It adds Ignarius for some reason. I think it replaces mine or something.”

Dev response:

“That would have been a really tough one to solve if you didn’t figure it out. The conditions are super specific.”

Impact:
Identified a highly niche but critical data overwrite bug caused by legacy debug tools.

✅ Portfolio Value: Highlights investigative QA, save testing, and rare bug discovery under real conditions.



QA Portfolio Entry #4
Elevator Softlock + Evolution Crash Chain
Game: Toby’s Island
Type: Environment softlock & post-evolution crash
Summary:
While revisiting Trogus’s temple, I encountered two separate game-breaking issues:

Elevator malfunction: After riding the elevator back down, the door failed to open and left me stuck.

Battle softlock: Shortly after, in a Marl encounter, enemy AI failed to act after their turn began.

Evolution crash: Later, after evolving a level 7 Jemjell into Athanel and continuing to the next boss encounter, selecting AlphaRay triggered a crash.

Elevator Softlock (Environment bug):

“Elevator doesn’t open if you go back the way you came... played the animation but then nothing — I’m stuck.”
![image](https://github.com/user-attachments/assets/2a399dba-361f-44e7-9290-3f1800ab7aba)


Battle AI Hang (Softlock):

“Completed my turn, the Marls get their turn and they don’t do anything. Forever.”
![image](https://github.com/user-attachments/assets/1ebff1d2-463e-4a6d-a7bd-253b58d64275)


Evolution Bug (Crash):

“Had a level 7 Jemjell, evolved into Athanel, then chose AlphaRay and got this crash…”
![image](https://github.com/user-attachments/assets/598d0207-2121-4f70-90fe-f7e5939ccaf9)
![image](https://github.com/user-attachments/assets/fd65a84a-4727-4619-80ca-78f3c5fb15b7)


Dev responses:

“You’re the only player to make it that far... well, take a break and I’ll fix everything you showed me so far.”


Other Notes You Can Use as Highlights or Quotes
Caught outdated label "SP" and suggested updated naming

Recommended stat changes and move balancing for Shellpup

Helped test and confirm counterattack mechanics fix with visual validation

Reported crashes during crafting system usage and empty inventory handling (chariotte1 bug)








---

(Keep adding more like this)
