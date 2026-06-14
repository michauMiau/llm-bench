# llm-bench

Subjective benchmark for Large Language Models, primarily focused on local ones.  
Tests LLM capabilities through complex creative tasks — generating self-contained web applications with physics-based mechanics and detailed game logic.

## Overview

This project evaluates how well different LLMs can:
- **Understand complex specifications** — translating detailed requirements into working code
- **Generate coherent, functional programs** — without hallucinating APIs or inventing non-existent libraries
- **Handle large contexts** — maintaining consistency across thousands of lines of generated code
- **Self-validate output** — detecting and fixing errors before delivery

Each test consists of a single prompt describing a complete application. The LLM generates the entire project in one go, which is then tested for correctness, functionality, and completeness.

## Prompts

### Prompt v1: WebXR Physics Sandbox Game

A complex game specification requiring physics-based interactions, weapon systems, enemy AI, and VR controller support — all implemented as a single HTML file playable on Quest 2 browser.

```
Create a WebXR physics sandbox game, similar to games like BONEWORKS and BONELAB. The testing chamber where the player is should feature several props like desks, chair, bullseye target to aim and shoot at, ladder located on a wall that the player can climb, buttons that spawn enemies and breakable crates and weapons

The weapons should be: 2 Different Rifles, Submachine Gun, Pistol and a Special Gun that features a special ability, that can be physics related, but is not limited to it. All weapons should feature the appropriate magazines that go with them, the weapons have to be physics based, they can be grabbed at the appropriate spot to shoot them, along with a second spot that can be grabbed that minimizes the recoil the weapon has and also makes it easier to aim, the reloading action cannot be automatically done, the player has to take the appropriate magazine for the gun, and insert it into the appropriate slot, then the player has to pull the reloading mechanism for the gun to be able to shoot

The player rig also has to be physics based, the arms must move realistically to the position where the hands are, the hand must be an actual physics object that can move things, have all 5 fingers that can be moved, the locomotion can be done by a locomotion ball, but it doesn't have to be, the player has to always be upright, the player can also crouch by crouching in real life, on the waist there should be an ammo holster that the player can grab ammo from, the ammo type is automatically chosen from the weapon the player is holding or the latest weapon the player held

The physics need to have sounds, if a weapon is dropped the appropriate sound has to be made, things like impacts have to have the appropriate particles along with sounds that differ depending on the object's material

There should also be melee weapons like: Crowbar, knife that can be stabbed into materials like wood and enemies, and a sledge hammer

The enemies also have to be fully physics based, the animations should either be nonexistent or guide the physics. The enemies have to ragdoll when they die. The game should feature the following enemies: A NullBody (an orange with white stripes enemy that slaps the player to hurt them — low health, releases orange blood particles on impact), a Corrupted NullBody (blue variant with more health and blue particles), and an Omni Projector (a SMG-wielding enemy that runs away when approached, pauses shooting periodically, its gun cannot be picked up and disappears with a red fizzle effect). All objects when removed should have a red fizzle effect

The controls (based on Quest 2 controllers) should be:
- A button: Jump — height depends on how long the button is held (with a limit)
- B button: Drops magazine from currently held gun
- Right Stick: Walk in direction player's head is facing
- X button: Special ability — can include bullet time, Spiderman line, super speed, or super jump
- Left Stick: Change facing direction; push up/down for crouching with adjustable height
- Triggers (both controllers): Shoot the gun held in that hand
- Grip buttons: Grab objects

The player has limited strength — they cannot move a crate with one hand alone. Holding a heavy gun with only one hand results in wobbling and increased recoil; gripping the second part of the gun limits recoil, reduces wobbling, and improves maneuverability

The game should be playable on Quest 2 using the built-in Chromium-based web browser. The entire game must fit into a single HTML file — test for JavaScript errors before finishing
```

## Evaluation Criteria

Each LLM output is scored based on:

| Criterion | Description |
|-----------|-------------|
| **Code Quality** | Clean, well-structured code without obvious bugs or dead imports |
| **Completeness** | All features from the prompt are implemented (weapons, enemies, physics, etc.) |
| **Functionality** | The generated game actually runs and is playable |
| **Self-Correction** | LLM detects and fixes its own errors before delivery |

## Results

### TEST_MODEL

**Harness:** OpenCode  
**Results:** [TEST_MODEL results](https://michaumiau.github.io/llm-bench/results/TEST_MODEL.html)  

*Additional Notes:* (Insert any additional settings, context size, changes, reasoning or other observations made here)

---

## Contribution

You can contribute to this project in several ways:

1. **Run a benchmark** — Test an LLM on the existing prompt and document your results
2. **Add new prompts** — Create more complex/fun test scenarios for other LLMs  
3. **Submit results via PR** — Open a pull request with your findings added to the Results section
4. **Create issues** — Report bugs, suggest improvements, or propose new benchmark ideas

If you want to test an LLM, run it, and document the results either in an issue or open a PR directly adding them here.
