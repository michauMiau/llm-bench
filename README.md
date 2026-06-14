# llm-bench
Benchmark for LLM's, primarily focused on local ones. 

## PROMPT v1
```
Create a WebXR physics sandbox game, similar to games like BONEWORKS and BONELAB. The testing chamber where the player is should feature several props like desks, chair, bullseye target to aim and shoot at, ladder located on a wall that the player can climb, buttons that spawn enemies and breakable crates and weapons
The weapons should be: 2 Different Rifles, Submachine Gun, Pistol and a Special Gun that features a special ability, that can be physics related, but is not limited to it. All weapons should feature the apropriate magazines that go with them, the weapons have to be physics based, they can be grabbed at the apriopriate spot to shoot them, along with a second spot that can be grabbed that minimizes the recoil the weapons has and also makes it easier to aim, the reloading action cannot be automatically done, the player has to take the apropriate magazine for the gun, and insert it into the apropriate slot, then the player has to pull the reloading mechanism for the gun to be able to shoot
The player rig also has to be physics based, the arms must move realistically to the position where the hands are, the hand must be an actual physics object that can move things, have all 5 fingers that can be moved, the locomotion can be done by a locomotion ball, but it doesn't have to be, the player has to  always be upright, the player can also crouch by crouching in real life, on the waist there should be a ammo holster that the player can grab ammo from, the ammo type is automatically chosen from the weapon the player is holding or the latest weapon the player held,
The physics need to have sounds, aka if a weapon is dropped the apropriate sound has to be made, things like impacts have to have the apropriate particles along with sounds that differ depending on the objects material.
There should also be melee weapons like: Crowbar, knife that can be stabbed into materials like wood and enemies, and a sledge hammer.
The enemies also have to be fully physics based, the animations should either be nonexistent or guide the physics. The enemies have to ragdoll when they die. The game should feature the following enemies, A NullBody, a orange with white stripes enemy that slaps the player to hurt them, they don't have a lot of health, they release orange (blood) particles when and where they are hit. The second enemy is the corrupted NullBody, they are like the normal nullbody, but they are blue, release blue particles and have a bit more health, the third enemy is the omni projector, they have a SMG that they aim and shoot at the player, they run away when the player gets close, they don't have to reload but they pause their shooting every once in a while, their gun cannot be picked up and it disappears with a red fizzle effect, all objects when removed have to have a red fizzle effect when being removed.
The controls (based off the quest 2 controller) should be: A: Jump button, the jump height is dependent on how long the player holds the jump button (with a limit), B: drops the magazine from the currently held gun, Right Stick: Walk in the direction the player's head is facing, with walking left, right and back when these directions are held on the stick X: Special ability button, the abilities can be one of the following but are not limited to, bullet time, spiderman line, super speed, super jump. The left stick can be used to change the direction the player is facing, by going right and left on it, the player can also crouch by pushing the sitck up and down, with adjustable crouch height. The triggers on both controllers are used to shoot the guns that are held in their respective hands, the grip buttons grab objects and things.
The player has limited strength, the player can't just move a whole crate with one hand, they will need to use 2 hands, holding a heavy gun with only one hand wil result in wobble up and down and increased recoil, they need to grip the second part on the gun to limit recoil, decrease wobbling and improve the manuverability of the gun.
The game should be playable on the Quest 2 in the built in chromium based web browser, the whole game has to be in a single html file, test the file for any js errors before finishing
```
## Results


#### TEST_MODEL
Harness: OpenCode ; [Results](https://michaumiau.github.io/llm-bench/results/TEST_MODEL.html)
Additional Notes: (Insert any additional settings,  the context size, changes, reasoning or else you made here)


## Contribution
You can contribute to this project however you want, if you want to test a llm then test it and document the results in an issue or open a pr and write the results here directly
