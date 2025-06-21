# Combat Mechanics Design

## 🎯 Core Combat Philosophy

The combat system emphasizes **tactical decision-making** over pure reflexes, with clear cause-and-effect relationships that reward strategic thinking and character build optimization.

## ⚔️ Fundamental Mechanics

### Action Economy

#### Action Types
- **Primary Actions**: Main attacks, major abilities
- **Secondary Actions**: Movement, item use, simple abilities
- **Reactions**: Counters, blocks, interrupts
- **Free Actions**: Communication, stance changes

#### Action Point System
```
Turn Structure:
├── 3 Action Points per turn
├── Primary Action: 2 AP
├── Secondary Action: 1 AP
├── Reaction: 0 AP (limited uses)
└── Free Action: 0 AP (unlimited)
```

### Initiative and Timing

#### Initiative Calculation
```
Initiative = Base_Agility + Weapon_Speed_Modifier + Random(1-10)
```

#### Turn Order Rules
1. Highest initiative acts first
2. Ties broken by Agility score
3. Further ties resolved randomly
4. Initiative recalculated each round

### Range and Positioning

#### Distance Categories
- **Melee Range**: 0-1 meters
- **Close Range**: 1-3 meters
- **Medium Range**: 3-10 meters
- **Long Range**: 10-30 meters
- **Extreme Range**: 30+ meters

#### Positioning Effects
- **Flanking**: +15% damage when attacking from behind/sides
- **High Ground**: +10% accuracy, +5% damage
- **Cover**: -25% ranged accuracy against target
- **Engagement**: Moving away from melee range provokes opportunity attacks

## 🎲 Dice and Probability

### Core Resolution Mechanic

#### D20 System
```
Action Success = d20 + Attribute + Skill + Modifiers vs. Target Number
```

#### Success Tiers
- **Critical Failure**: Natural 1 (automatic failure)
- **Failure**: Total < Target Number
- **Success**: Total ≥ Target Number
- **Critical Success**: Natural 20 or exceeds TN by 10+

### Advantage/Disadvantage
- **Advantage**: Roll 2d20, take higher
- **Disadvantage**: Roll 2d20, take lower
- **Multiple sources**: Advantage and disadvantage cancel out

## ⚡ Action Resolution

### Attack Sequence

1. **Declare Target**: Select valid target within range
2. **Calculate Accuracy**: Base skill + modifiers vs. Defense
3. **Roll Attack**: d20 + accuracy modifiers
4. **Determine Hit**: Compare to target's Defense Value
5. **Calculate Damage**: Base damage + modifiers
6. **Apply Damage**: Reduce target's health
7. **Trigger Effects**: Apply on-hit effects, status changes

### Defense Mechanics

#### Defense Types
- **Armor Class (AC)**: Physical damage reduction
- **Evasion**: Chance to avoid attacks entirely
- **Magic Resistance**: Reduction of magical effects
- **Status Immunity**: Resistance to specific conditions

#### Defense Calculation
```
Total Defense = Base_Defense + Armor_Bonus + Agility_Modifier + Situational_Modifiers
```

## 💥 Damage System

### Damage Types

#### Physical Damage
- **Slashing**: Swords, axes, claws
- **Piercing**: Spears, arrows, stingers
- **Bludgeoning**: Hammers, clubs, fists

#### Elemental Damage
- **Fire**: Burning, heat effects
- **Ice**: Freezing, slowing effects
- **Lightning**: Shocking, stunning effects
- **Poison**: Damage over time, weakening

#### Special Damage
- **Psychic**: Mental attacks, fear effects
- **Necrotic**: Life drain, decay effects
- **Divine**: Holy damage, healing reversal
- **Force**: Pure magical energy

### Damage Calculation

#### Base Formula
```
Final_Damage = (Base_Damage + Attribute_Modifier + Weapon_Damage) × Multipliers - Resistances
```

#### Critical Hits
- **Critical Chance**: Base 5%, modified by stats/abilities
- **Critical Multiplier**: 2x damage (default)
- **Critical Effects**: May trigger special status effects

### Resistance and Immunity

#### Resistance Levels
- **Vulnerable**: +50% damage taken
- **Normal**: 100% damage taken
- **Resistant**: 50% damage taken
- **Highly Resistant**: 25% damage taken
- **Immune**: 0% damage taken

## 🌟 Status Effects

### Beneficial Effects (Buffs)

#### Combat Buffs
- **Blessed**: +2 to all rolls
- **Haste**: +1 action per turn
- **Strength**: +4 to damage rolls
- **Protection**: +2 AC
- **Regeneration**: Heal X HP per turn

### Harmful Effects (Debuffs)

#### Conditions
- **Poisoned**: X damage per turn
- **Stunned**: Cannot take actions
- **Slowed**: -1 action per turn
- **Weakened**: -4 to damage rolls
- **Bleeding**: Increasing damage per turn
- **Confused**: Random target selection

### Status Duration
- **Instant**: Immediate effect, no duration
- **Temporary**: Lasts X turns
- **Concentration**: Lasts while caster maintains focus
- **Permanent**: Until dispelled or cured

## 🎮 Special Mechanics

### Combo System

#### Combo Building
- Successful attacks build combo points
- Different attack types generate different combo amounts
- Combo points decay over time if not used

#### Combo Abilities
- **Light Combo** (3 points): Minor bonus effects
- **Medium Combo** (6 points): Significant abilities
- **Heavy Combo** (10 points): Powerful finishing moves

### Momentum System

#### Momentum Generation
- Gain momentum from successful actions
- Lose momentum from failures or taking damage
- High momentum provides action bonuses
- Low momentum applies penalties

### Environmental Interactions

#### Interactive Elements
- **Destructible Cover**: Can be destroyed to remove protection
- **Hazardous Terrain**: Causes damage or status effects
- **Elevated Positions**: Provide tactical advantages
- **Dynamic Elements**: Moving platforms, closing doors

## ⚖️ Balance Considerations

### Power Scaling

#### Linear Growth
- Attributes increase predictably
- Damage scales with character level
- New abilities supplement rather than replace

#### Diminishing Returns
- High stats become more expensive
- Extreme specialization has trade-offs
- Balanced builds remain viable

### Counter-Play

#### Rock-Paper-Scissors
- Every strategy has counters
- Multiple viable approaches to encounters
- Adaptability rewarded over optimization

#### Risk vs. Reward
- Powerful abilities have drawbacks
- High-risk maneuvers offer high rewards
- Safe strategies remain effective but slower

---

*This document defines the core mechanical interactions that drive combat gameplay. All numerical values are subject to balance testing and iteration.*