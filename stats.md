# Hero Guild Tycoon – Unit Stats & Empire Balancing

## ⚙️ Base Unit Stats
| Stat | Description |
|------|-------------|
| HP | Hit points, how much damage the unit can take |
| Attack | Base damage dealt per hit |
| Attack Speed | How fast the unit attacks (hits per second) |
| Movement Speed | How fast the unit moves on the map |
| Crit Chance | Chance to deal critical damage (bonus damage) |
| Defense | Reduces incoming damage |
| Ability Strength | Power of the unit’s special ability |
| Special Cooldown | Time between ability uses |

---

## 🏰 Empire-Specific Stat Multipliers

| Empire | Unique Balance | Explanation |
|--------|----------------|-------------|
| Kingdom of Valor | +10% HP, +5% Attack | Valor units are tanky and durable; frontliners survive longer. Their attacks are reliable but not overpowered. |
| Arcane Dominion | +15% Ability Strength, -10% Ability Cooldown | Arcane units rely on spells; they deal higher burst damage and cast abilities faster. Their basic attacks are weaker. |
| Sylvan Alliance | +10% Crit Chance, +10% Loot Drop | Sylvan units are agile, dealing occasional high damage and increasing rewards from quests. Weaker defenses balance them. |
| Iron Legion | +20% Build/Repair Speed, +5% Idle Gain | Iron units are slower but boost guild productivity. They excel in mechanics and automation rather than raw combat. |
| Crimson Horde | +25% XP Gain, -15% Defense | Crimson units level up faster and deal huge damage but are fragile. Aggressive play is rewarded but mistakes are costly. |

---

## 💡 Suggested Stat Ranges for Units (Level 1)
| Unit Role | HP | Attack | Attack Speed | Movement | Crit Chance | Defense | Ability Strength |
|-----------|----|--------|--------------|----------|-------------|--------|----------------|
| Tank | 1500-2500 | 50-80 | 0.5-1 | 3-4 | 5% | 15-25 | 50-100 |
| DPS | 800-1200 | 100-150 | 1-1.5 | 4-5 | 10-20% | 5-10 | 50-120 |
| Support | 700-1000 | 50-80 | 0.8-1 | 4 | 5-10% | 5-10 | 60-150 |
| Hybrid | 1000-1500 | 80-120 | 0.8-1 | 3-4 | 5-15% | 10-15 | 70-130 |
| Utility | 600-1000 | 40-70 | 0.7-1 | 4-5 | 5% | 5-10 | 40-100 |

---

## 🧩 Empire-Specific Unit Flavor

| Empire | Unit Role | Unique Trait / Modifier |
|--------|----------|------------------------|
| Kingdom of Valor | Tank/DPS | +10% HP and minor attack boost; long-lasting frontline units |
| Arcane Dominion | DPS/Support | +15% ability power, faster cooldowns; weaker basic attacks |
| Sylvan Alliance | DPS/Utility | +10% crit, +10% loot; lower HP to balance agility and rewards |
| Iron Legion | Tank/Support | +20% building speed, small idle income bonus; mechanically-oriented support units |
| Crimson Horde | DPS/Hybrid | +25% XP gain, -15% defense; high-risk, high-reward aggressive units |

---

## 🔹 Implementation Tips
1. Store empire multipliers in a **Lua table** for easy scaling:
```lua
local EmpireStats = {
  Valor = {HP=1.10, Attack=1.05},
  Arcane = {Ability=1.15, Cooldown=0.90},
  Sylvan = {Crit=1.10, Loot=1.10},
  Iron = {BuildSpeed=1.20, Idle=1.05},
  Crimson = {XP=1.25, Defense=0.85}
}
