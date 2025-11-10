# ⚔️ Hero Guild Tycoon – Empire System Design Document

**Version:** 1.0  
**Author:** [Your Studio Name]  
**Date:** [Insert Date]

---

## 🧭 Overview

**Hero Guild Tycoon** allows players to manage an idle hero guild — hiring heroes, sending them on quests, upgrading their facilities, and building power through rebirths (prestiges).

To increase replayability and depth, the **Empire System** introduces 5 selectable factions, each with unique bonuses, visuals, and hero themes. Inspired by *Age of Empires II*, it adds strategic flavor without overwhelming new players.

---

## 🌍 Empire System Core Concept

At the start of a new game (or after a prestige), the player selects an **Empire** to align with.  
Each Empire grants **unique buffs**, **hero visual themes**, and **Guild Hall designs**.

Empires shape a player’s strategy — whether they favor speed, power, loot, or automation.

Players can later **switch empires** after a prestige or by purchasing a premium “Empire Change Token.”

---

## 🏰 Starter Empires

### 🛡️ Kingdom of Valor
- **Theme:** Medieval knights, courage, honor  
- **Hero Focus:** Warriors  
- **Bonuses:**
  - +10% Hero HP  
  - +5% Gold from quests  
- **Visual Style:** Stone castle halls, blue banners, gold shields  
- **Tagline:** “Steel and honor forge victory.”

---

### 🧙 Arcane Dominion
- **Theme:** Magic, knowledge, mystical power  
- **Hero Focus:** Mages and spellcasters  
- **Bonuses:**
  - +15% Spell Damage  
  - -10% Quest Duration  
- **Visual Style:** Floating runes, glowing crystals, purple auras  
- **Tagline:** “Time and wisdom bend to your will.”

---

### 🏹 Sylvan Alliance
- **Theme:** Forest, agility, nature’s guardians  
- **Hero Focus:** Archers, Rogues  
- **Bonuses:**
  - +10% Critical Chance  
  - +10% Loot Drop Rate  
- **Visual Style:** Wooden platforms, vines, green energy glow  
- **Tagline:** “Swift as the wind, silent as the leaves.”

---

### ⚙️ Iron Legion
- **Theme:** Steam, technology, automation  
- **Hero Focus:** Tanks, Builders, Mechanics  
- **Bonuses:**
  - +20% Building Speed  
  - +5% Idle Income  
- **Visual Style:** Bronze gears, smoke, blacksmith forges  
- **Tagline:** “Progress never sleeps.”

---

### 🔥 Crimson Horde
- **Theme:** Demonic energy, chaos, raw strength  
- **Hero Focus:** Mixed attack units, berserkers  
- **Bonuses:**
  - +25% Hero XP Gain  
  - -15% Hero Defense  
- **Visual Style:** Volcanic fortress, red crystals, molten floors  
- **Tagline:** “Power demands sacrifice.”

---

## 🧩 Empire Selection Flow

1. **New Game or Prestige:**  
   Prompt: *“Choose your Empire to shape your Guild’s destiny.”*

2. **Selection Menu:**  
   Carousel or banners showing each empire:
   - Icon + Name  
   - Short tagline  
   - Two key bonuses  
   - Visual preview of Guild Hall style

3. **Confirmation Prompt:**  
   *“You have sworn allegiance to the Arcane Dominion. Their wisdom flows through your heroes.”*

4. **Effect Application:**  
   Apply global stat modifiers:
   ```lua
   local Empires = {
     Valor = {GoldMult = 1.05, HP = 1.10},
     Arcane = {Damage = 1.15, QuestSpeed = 1.10},
     Sylvan = {Crit = 1.10, Loot = 1.10},
     Iron = {BuildSpeed = 1.20, Idle = 1.05},
     Crimson = {XP = 1.25, Defense = 0.85},
   }
