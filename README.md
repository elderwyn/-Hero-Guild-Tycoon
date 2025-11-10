# ⚔️ Hero Empire Tycoon – Empire System Design

## 🧭 Overview
**Hero Empire Tycoon** lets players manage an idle hero empire:  
Hire heroes, send them on quests, upgrade facilities, and grow stronger through **rebirths (prestiges).**

The **Empire System** adds depth and replayability:  
- **5 selectable factions** with unique bonuses, visuals, and hero themes  
- Strategic choices inspired by *Age of Empires II*  
- Enhances gameplay without overwhelming new players  

---

## 🌍 Empire System – Core Concept
At the start of a game (or after a prestige), players choose an **Empire** to align with:  
- Each Empire grants **unique buffs, hero visual themes, and Empire Hall designs**  
- Empires influence strategy: speed, power, loot, or automation  
- Players can **switch Empires** later via prestige or a premium “Empire Change Token”

---

## 🧩 Empire Selection Flow

### **New Game or Prestige**
Prompt: *“Choose your Empire to shape your empire’s destiny.”*

### **Selection Menu**
Carousel or banners displaying:  
- Icon + Name  
- Short tagline  
- Two key bonuses  
- Visual preview of Empire Hall  

### **Confirmation Prompt**
Each Empire has a unique confirmation prompt  
[List of prompts](empires/readme.md#Empire-Confirmation-Prompts)

---

## 🎮 Game Loop

### Tutorial
- Quick intro on running your empire  
- Highlights Empire choice and hero recruitment

### 1️⃣ Unit Recruitment System  
[More info](recruitment.md)  
- Recruit heroes to expand your empire and complete missions  

### 2️⃣ Mission Unlock System  
[More info](missions.md)  
- Missions reward **gold, resources, XP, and loot**  
- Predictable yet rewarding to maintain progression  
- Display recommended units and bonuses before missions  
- Include **auto-complete / AFK options** for idle play  
- Encourages **diverse unit collection**  

### 3️⃣ Reward System  
[More info](rewards.md)  
- Every mission guarantees at least one reward  
- Rewards scale by mission type and units used  
- Track success rates to balance economy and progression  

---

## 📝 Example Game Session
1. Player logs in → Chooses Empire → Completes tutorial  
2. Recruits 3 basic units → Starts first mission (Training Grounds)  
3. Completes mission → Earns gold & XP → Upgrades units and buildings  
4. Unlocks next mission (Bandit Raid) → Selects units strategically  
5. Repeat missions → Level up empire → Prestige when desired  
6. Participate in events → Recruit limited-time units → Collect cosmetics  
7. Loop continues with scaling difficulty and rewards  

---

## ✨ Interactivity & Feedback

### Mission Interaction
- Unit deployment animations  
- Particle effects and floating damage numbers  
- Progress bar / visual action map  
- Leaderboards / empire rankings  
- Optional co-op missions  

### Upgrades & Rewards
- Visually rewarding upgrades (glowing buildings, new gear)  
- Units grow visibly stronger  
- New areas unlock as empire expands  
- Special banners or cosmetic effects for events  
- **Prestige / Endgame Loop:** permanent bonuses for replayability  

### Player Control
- Click units to view stats  
- Drag-and-drop formations  
- Visit other players’ empires  
- **Idle Loop:** earn gold and XP offline  

---

## 💎 Monetization Integration

| Product                            | Description                                             | Price (Robux) |
| ---------------------------------- | ------------------------------------------------------- | ------------- |
| **Empire Change Token**            | Switch Empires without resetting                        | 149           |
| **Empire Starter Pack**            | Unique Empire & Hero skins + 2-hour boost             | 299           |
| **Premium Empire Access (Future)** | Unlock 6th exclusive Empire                             | 499           |

---

## 🏛️ Future Expansion Ideas

### 🌌 Celestial Empire (Premium)
- **Theme:** Divine energy, light, balance  
- **Bonuses:** +10% to all stats, special celestial heroes  
- **Unlock:** Premium Gamepass only  

### ⚔️ Empire Wars (Live Events)
- Weekly/monthly global competitions between empires  
- Rewards: bonus loot, exclusive titles, limited skins  

---

## 🏅 Empire Achievements
- **Master of Valor:** Reach Prestige 5 as Valor Empire  
- **Arcane Archmage:** Summon 50 Legendary Mages  
- Rewards include permanent titles or cosmetic auras  

---

## 🧠 Player-Friendly Design

### Simplified Choices for New Players
| Empire | Description |
|--------|------------|
| **Valor** | Strong heroes, solid income |
| **Arcane** | Faster quests, magic power |
| **Sylvan** | More loot, higher crits |
| **Iron** | Fast upgrades, better AFK gains |
| **Crimson** | Level up heroes quickly |

- Visual cues (color + symbol) make Empires easy to remember  
