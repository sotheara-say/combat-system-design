# Damage System Design

## 💥 Damage Framework

### Core Damage Types

#### **Physical Damage**

##### **Slashing**
- **Sources**: Swords, axes, claws, bladed weapons
- **Characteristics**: High base damage, good critical hit potential
- **Resistances**: Heavy armor, thick hides
- **Special Effects**: Bleeding, limb damage

##### **Piercing**
- **Sources**: Spears, arrows, stabbing weapons
- **Characteristics**: Armor penetration, precise targeting
- **Resistances**: Deflective armor, thick skin
- **Special Effects**: Deep wounds, organ damage

##### **Bludgeoning**
- **Sources**: Hammers, clubs, fists, blunt weapons
- **Characteristics**: Consistent damage, knockback effects
- **Resistances**: Padded armor, elastic defenses
- **Special Effects**: Stunning, bone breaking

#### **Elemental Damage**

##### **Fire**
- **Characteristics**: High damage, area effects, ignition
- **Resistances**: Fire immunity, wet conditions
- **Special Effects**: Burning (DoT), fear, light source
- **Environmental**: Spreads to flammable objects

##### **Ice/Cold**
- **Characteristics**: Moderate damage, slowing effects
- **Resistances**: Cold immunity, warm environments
- **Special Effects**: Freezing, slowing, brittle state
- **Environmental**: Creates ice surfaces, extinguishes fires

##### **Lightning**
- **Characteristics**: Fast, chain effects, stunning
- **Resistances**: Electrical immunity, grounding
- **Special Effects**: Paralysis, chain lightning, EMP
- **Environmental**: Conducts through water and metal

##### **Poison**
- **Characteristics**: Damage over time, weakening effects
- **Resistances**: Poison immunity, constitution saves
- **Special Effects**: Stat reduction, nausea, toxicity buildup
- **Environmental**: Persistent area denial

#### **Exotic Damage Types**

##### **Psychic**
- **Sources**: Mental attacks, fear effects, psionics
- **Characteristics**: Bypasses physical defenses
- **Resistances**: Mental fortitude, psychic wards
- **Special Effects**: Confusion, mind control, madness

##### **Necrotic**
- **Sources**: Undead attacks, life drain, decay magic
- **Characteristics**: Life force damage, healing prevention
- **Resistances**: Divine protection, life force strength
- **Special Effects**: Healing reduction, temporary HP loss

##### **Divine/Radiant**
- **Sources**: Holy magic, blessed weapons, divine intervention
- **Characteristics**: Extra damage vs. undead/evil
- **Resistances**: Divine immunity, holy protection
- **Special Effects**: Undead turning, evil banishment

##### **Force**
- **Sources**: Pure magical energy, telekinetic attacks
- **Characteristics**: Untyped damage, knockback
- **Resistances**: Very rare, usually partial
- **Special Effects**: Displacement, magical disruption

## 📈 Damage Calculation

### Base Damage Formula

#### **Standard Calculation**
```
Base_Damage = Weapon_Damage + Attribute_Modifier + Skill_Bonus
Final_Damage = (Base_Damage × Multipliers) - Resistances
```

#### **Attribute Scaling**
- **Strength**: Melee weapon damage
- **Dexterity**: Ranged weapon damage, finesse weapons
- **Intelligence**: Spell damage
- **Wisdom**: Healing, some spell damage

### Damage Multipliers

#### **Critical Hits**
- **Base Critical**: 5% chance, 2x damage multiplier
- **Critical Range**: Some weapons/abilities expand crit range
- **Critical Multiplier**: Can be increased through abilities/equipment
- **Critical Effects**: May trigger additional status effects

#### **Situational Modifiers**
- **Flanking**: +25% damage when attacking from behind/sides
- **Height Advantage**: +15% damage when attacking from above
- **Surprise Attack**: +50% damage on completely unaware targets
- **Vulnerability**: Target takes +50% damage from specific types

#### **Combat State Modifiers**
- **Bloodied** (below 50% HP): Some abilities deal bonus damage
- **Near Death** (below 25% HP): Desperation bonuses
- **Full Health**: Certain abilities only work at full health
- **Status Effects**: Various buffs/debuffs affect damage

### Resistance System

#### **Resistance Levels**
```
Vulnerable:      × 1.5 damage (take 50% more)
Normal:          × 1.0 damage (standard)
Resistant:       × 0.5 damage (take half)
Highly Resistant: × 0.25 damage (take quarter)
Immune:          × 0.0 damage (take none)
```

#### **Armor System**

##### **Damage Reduction (DR)**
```
Final_Damage = max(0, Raw_Damage - Damage_Reduction)
```

##### **Armor Types**
- **Light Armor**: Low DR, high mobility
- **Medium Armor**: Balanced DR and mobility
- **Heavy Armor**: High DR, reduced mobility
- **Magical Armor**: Special resistances, unique properties

##### **Armor Penetration**
- **Piercing weapons**: Ignore portion of armor
- **Magic weapons**: Bypass certain armor types
- **Critical hits**: May ignore armor entirely
- **Special abilities**: Various armor-bypassing effects

## ❄️ Status Effects and DoT

### Damage Over Time (DoT)

#### **Burning**
- **Source**: Fire damage, certain abilities
- **Effect**: X fire damage per turn
- **Duration**: 3-5 turns (varies by source)
- **Stacking**: Multiple applications extend duration
- **Removal**: Water effects, healing magic, specific items

#### **Bleeding**
- **Source**: Slashing/piercing criticals, certain abilities
- **Effect**: Increasing damage each turn (1, 2, 3, 4...)
- **Duration**: Until healed or combat ends
- **Stacking**: Multiple wounds increase rate
- **Removal**: Healing magic, medical treatment, bandages

#### **Poison**
- **Source**: Poison weapons, toxic abilities, environmental
- **Effect**: X poison damage per turn + stat penalties
- **Duration**: Long (8-10 turns)
- **Stacking**: Different poisons can stack
- **Removal**: Antidotes, cure magic, high constitution saves

### Damage Enhancement Effects

#### **Vulnerability**
- **Effect**: +50% damage from specific damage type
- **Sources**: Certain spells, environmental effects
- **Duration**: Temporary (3-5 turns)
- **Strategy**: Combo with matching damage types

#### **Marked for Death**
- **Effect**: Next attack deals maximum damage
- **Sources**: Rogue abilities, certain spells
- **Duration**: Until next attack hits target
- **Strategy**: Combo with powerful abilities

#### **Weakness**
- **Effect**: -4 to damage rolls
- **Sources**: Curses, disease, exhaustion
- **Duration**: Long-term until cured
- **Removal**: Restoration magic, rest, specific treatments

## 🎮 Advanced Damage Mechanics

### Penetration and Mitigation

#### **Percentage Penetration**
```
Effective_Armor = Armor_Value × (1 - Penetration_Percentage)
```

#### **Flat Penetration**
```
Effective_Armor = max(0, Armor_Value - Flat_Penetration)
```

#### **True Damage**
- Bypasses all resistances and armor
- Very rare, usually from ultimate abilities
- Cannot be reduced or prevented

### Overkill Mechanics

#### **Cleave Damage**
- Excess damage carries to nearby enemies
- Percentage of overkill applies to adjacent targets
- Chain effects for satisfying multi-kills

#### **Execution Thresholds**
- Some abilities instantly kill below certain HP
- Usually percentage-based ("below 25% HP")
- Powerful but situational effects

### Environmental Damage

#### **Hazard Types**
- **Lava/Fire**: High damage, burning effect
- **Acid Pools**: DoT, equipment damage
- **Electricity**: Stunning, chain effects
- **Crushing**: High bludgeoning, knockdown
- **Falling**: Based on distance, can be lethal

#### **Interactive Elements**
- **Explosive Barrels**: Area fire damage
- **Collapsing Structures**: Massive bludgeoning
- **Magical Traps**: Various elemental effects
- **Environmental Combos**: Player-triggered hazards

## ⚖️ Damage Balance

### Power Scaling

#### **Linear Scaling**
- Damage increases predictably with level/stats
- Maintains relative effectiveness of different builds
- Prevents power creep from making early content trivial

#### **Breakpoint Design**
- Certain thresholds unlock new effectiveness levels
- Creates meaningful upgrade moments
- Encourages specific stat investments

### Damage Type Distribution

#### **Physical vs. Magical**
- Roughly 60% physical, 40% magical in typical encounters
- Varies by enemy type and environment
- Players should face diverse resistance challenges

#### **Single vs. Area Damage**
- Single-target: Higher damage per target
- Area damage: Lower per-target but hits multiple
- Situational advantages for both approaches

### Risk vs. Reward

#### **High-Damage Abilities**
- Long cooldowns or high resource costs
- Positioning requirements or setup time
- Potential for counterplay or failure

#### **Consistent Damage**
- Lower peak damage but reliable
- Lower resource requirements
- Available more frequently

### Defensive Options

#### **Active Defense**
- Player abilities that reduce incoming damage
- Timing-based damage reduction
- Resource costs for defensive actions

#### **Passive Defense**
- Equipment-based damage reduction
- Stat-based resistances
- Always-active but limited effectiveness

---

*This document defines the damage systems that create tactical depth and meaningful combat choices. All numerical values are baseline suggestions for testing and balance iteration.*