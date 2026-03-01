# Techguns 2 (Completion Update) - Draconic Evolution Compatibility Fix

This is a fork of the **Techguns 2 (1.12.2)** mod, specifically patched to resolve long-standing issues with external energy shields.

## 🛠 What's Fixed?
The main goal of this fork is to fix the conflict where Techguns bullets would completely bypass **Draconic Evolution** energy shields, damaging the player's health directly.

### Technical Changes:
* **Event Priority Adjustment:** Changed `OnLivingAttack` and `onLivingHurt` event priorities in `TGEventHandler` from `HIGH` to `LOWEST`.
* **Shield Recognition:** This change allows Draconic Evolution (and potentially other shield mods like Matter Overdrive or Modular Turrets) to intercept damage before the Techguns internal damage system processes it.
* **Standard Damage Preserved:** Verified that normal damage (without armor/shields) still functions correctly for both players and NPCs.

## 🚀 How to Install
1. Go to the [Releases](https://github.com/GitNell/Techguns2-CE-Draconic-Evo-Compability/releases) tab.
2. Download the latest `.jar` file.
3. Replace the original Techguns JAR in your Minecraft `mods` folder with this patched version.

## 🏗 For Developers
If you want to build this from source:
1. Clone the repository: `git clone https://github.com/GitNell/Techguns2-CE-Draconic-Evo-Compability.git`
2. Run `./gradlew build` (or `gradle build` if using system Gradle).
3. Find the output in `build/libs/`.

---
*Based on the Completion Update by TheSlize. Original mod by Techguns Team.*
