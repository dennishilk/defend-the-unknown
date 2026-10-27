# First Playable Prototype — Scope & Handoff

> **This is a proposal for the first experiment, not a feature list of an existing build.**  
> **Project:** DEFEND THE UNKNOWN · **Owner:** Dennis Hilk  
> **Deutsch:** [Kurzüberblick unten](#kurzüberblick-auf-deutsch)

## Why I am starting small

I want to find out whether a small, first-person desert outpost with a tactical command layer feels good **before** tackling convoys, aircraft, research, traders, huge maps, or a complex narrative.

I also want to test how reliably ChatGPT, Codex, and an Unreal Editor integration can help me create and maintain that experience. My results should be evidence-based, with a clear distinction between generated work, manual fixes, and failures.

## Target experience (one compact playable loop)

I'm standing inside my old desert base. I can move, look around, and recognize a few key places. I speak to Harris or Miller, give a simple guard command, open a tactical view, position a watchtower or turret, return to first person, and watch it exist in the world. I drive a jeep a short distance and witness a small attack that my personnel and defensive structure react to.

If this sequence makes me smile, I've learned something important.

### Prototype boundaries

| Area | First test | Explicitly not necessary yet |
| --- | --- | --- |
| **World** | Small desert test level, existing base shell, walkable area, a few landmarks | Huge open world, weather simulation, settlements |
| **Player** | First-person walk/look/interact, pause and basic save/load if feasible | Full inventory, complex weapons, RPG skill trees |
| **Personnel** | Around three named AI soldiers; basic position/hold/engage logic | Full personalities, careers, extensive dialogue, schedules |
| **Build view** | Toggle tactical overview, preview and place **one** defensive structure | Full base economy, roads, walls, arbitrary building catalogue |
| **Vehicle** | One simple drivable jeep | Physical drivetrain simulation, convoys, helicopters, tanks |
| **Threat** | One short, visible encounter with simple enemy behavior | Dynamic factions, military strategy AI, complex wave director |
| **Feedback** | Simple orders, alerts, soldier acknowledgements | Full radio acting, surveillance playback, smart deputy |
| **Tech validation** | Reliable project open/play loop and documented Codex/editor experiment | Promise of autonomous end-to-end game creation |

The first scope is deliberately a **target**, not a rigid implementation plan. If the basic technical validation demands an even smaller step, I can reduce it further.

## What I want to verify

- [ ] The Unreal project opens, runs, and closes cleanly on my Linux machine.
- [ ] I can walk around a recognizably military desert outpost in first person.
- [ ] The tactical view can place at least one defense, which appears in the FPS world.
- [ ] A named soldier can be given a visible, understandable assignment.
- [ ] The jeep can be entered, driven, and exited.
- [ ] A small enemy encounter produces sensible feedback and an understandable outcome.
- [ ] Pause works; save/load is tested before I claim it works.
- [ ] I have a written record of what Codex generated, what I changed myself, and what could not be automated.
- [ ] After repeated tests, I can still reopen the project without breakage or missing assets.

Nothing in this checklist is marked complete at this stage.

## Out of scope for the first milestone

The sealed bunker, story cutscenes, persistent character relationships, permanent death, sophisticated AI decision-making, research, research failures, aircraft, medevac, large-scale inventory, salvage chains, drone cameras, spotters, civilians, trading, and full logistics are **future design ideas**. I won't disguise an absence of those systems as a bug in prototype one.

I want to avoid a familiar trap: trying to build *the entire game* before I've proved the basic interaction is enjoyable.

## Experiment protocol for Codex + Unreal

Before implementation I will verify current Unreal Engine/Linux compatibility, the actual state and limits of Unreal MCP/editor-control tooling, and the simplest repeatable workflow. I will not assume a plugin can build gameplay Blueprints or assets unless I have tested it.

For each major experiment, I want to capture:

1. **Task** I gave to the agent.
2. **Tools/versions** actually used.
3. **Result**, including screenshots or logs where relevant.
4. **Manual changes** and errors encountered.
5. **Reproduction steps** for the next attempt.

My development computer is an AMD Ryzen 7 5800X3D / Radeon RX 9060 XT 16 GB / 32 GB RAM running Arch Linux, Xorg/dwm. GPU stability is being investigated separately. The prototype should stay modest until this environment is proven reliable.

**Terminal convention on my Linux machine: one command at a time.** I want to inspect each result before issuing the next command.

## Project structure at the concept stage

Currently I am keeping this repo for documentation and project identity. I do **not** want to add an empty Unreal project, fabricated benchmark, misleading automated badge, or screenshot of gameplay that does not exist.

Once the editor workflow is known, I can organize the actual project and decide what belongs in version control (including asset sizes and Git LFS needs).

## Kurzüberblick auf Deutsch

**Mein erster Test soll nicht das komplette Spiel werden.** Ich möchte in einer kleinen Wüstenbasis herumlaufen, drei benannte Soldaten sehen, einen einfachen Befehl geben, in die taktische Bauansicht wechseln, einen Wachturm oder eine Geschützstellung platzieren, einen Jeep fahren und einen überschaubaren Feindkontakt erleben.

Erst danach entscheide ich, welche Systeme sich wirklich lohnen. Für den nächsten Chat will ich zunächst **Unreal Engine unter Arch Linux**, die aktuelle praktische Editor-Automatisierung mit **Codex/MCP** und einen kleinen, wiederholbaren Testaufbau prüfen. Wir gehen auf meinem Rechner **immer nur einen Terminalbefehl nach dem anderen** durch.

---

*Designed as a lean, testable starting point by Dennis Hilk — not a release promise.*
