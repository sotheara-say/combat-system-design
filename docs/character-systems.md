# Character Systems Design

## 🧬 Character Foundation

### Core Attributes

#### Primary Stats
- **Strength (STR)**: Physical power, melee damage, carrying capacity
- **Dexterity (DEX)**: Agility, ranged accuracy, initiative, evasion
- **Constitution (CON)**: Health, stamina, resistance to effects
- **Intelligence (INT)**: Magical power, spell accuracy, mana pool
- **Wisdom (WIS)**: Perception, magical resistance, healing power
- **Charisma (CHA)**: Leadership, social abilities, some magical effects

#### Derived Stats
```
Health Points = (CON × 10) + Class_Bonus + Level_Bonus
Mana Points = (INT × 8) + (WIS × 2) + Class_Bonus
Stamina = (CON × 5) + (STR × 3) + Class_Bonus
Initiative = DEX + Equipment_Modifier
Armor Class = 10 + DEX_Modifier + Armor_Bonus
```

### Attribute Modifiers
```
Attribute Score | Modifier
1-3             | -4
4-5             | -3
6-7             | -2
8-9             | -1
10-11           | 0
12-13           | +1
14-15           | +2
16-17           | +3
18-19           | +4
20+             | +5
```

## 🎭 Character Classes

### Warrior Archetype

#### **Guardian**
- **Role**: Tank, damage mitigation
- **Primary Stats**: CON, STR
- **Abilities**: Taunt, Shield Bash, Damage Reduction
- **Playstyle**: Front-line defender, draws enemy attention

#### **Berserker**
- **Role**: High-damage melee DPS
- **Primary Stats**: STR, CON
- **Abilities**: Rage, Reckless Attack, Intimidation
- **Playstyle**: Aggressive attacker, high risk/reward

### Rogue Archetype

#### **Assassin**
- **Role**: Single-target burst damage
- **Primary Stats**: DEX, STR
- **Abilities**: Stealth, Backstab, Poison Use
- **Playstyle**: Hit-and-run tactics, critical strikes

#### **Scout**
- **Role**: Ranged damage, utility
- **Primary Stats**: DEX, WIS
- **Abilities**: Tracking, Precise Shot, Trap Detection
- **Playstyle**: Ranged support, battlefield awareness

### Mage Archetype

#### **Elementalist**
- **Role**: Area damage, elemental effects
- **Primary Stats**: INT, WIS
- **Abilities**: Fireball, Ice Storm, Lightning Bolt
- **Playstyle**: Powerful spells, resource management

#### **Healer**
- **Role**: Support, healing, buffs
- **Primary Stats**: WIS, CHA
- **Abilities**: Heal, Blessing, Dispel Magic
- **Playstyle**: Team support, strategic positioning

### Hybrid Classes

#### **Paladin**
- **Role**: Tanky support, moderate healing
- **Primary Stats**: STR, WIS, CHA
- **Abilities**: Lay on Hands, Divine Strike, Aura effects
- **Playstyle**: Balanced offense/defense with divine magic

#### **Battlemage**
- **Role**: Magical melee combat
- **Primary Stats**: INT, STR
- **Abilities**: Weapon Enchantment, Spell-sword techniques
- **Playstyle**: Close-range magic combat

## 📈 Character Progression

### Experience and Leveling

#### Experience Sources
- **Combat Victory**: Defeating enemies
- **Quest Completion**: Achieving objectives
- **Discovery**: Finding new areas, secrets
- **Social Success**: Successful negotiations, etc.

#### Level Benefits
- **Attribute Points**: +2 points per level to distribute
- **Skill Points**: +3 points per level for abilities
- **Health/Mana**: Automatic increases based on class
- **New Abilities**: Unlock higher-tier skills

### Skill Trees

#### Tree Structure
```
Skill Tree Example (Warrior)
├── Tier 1: Basic Combat
│   ├── Power Attack
│   ├── Defensive Stance
│   └── Weapon Mastery
├── Tier 2: Advanced Techniques
│   ├── Whirlwind (requires Power Attack)
│   ├── Shield Wall (requires Defensive Stance)
│   └── Weapon Specialization (requires Weapon Mastery)
└── Tier 3: Master Abilities
    ├── Berserker Rage (requires Whirlwind)
    ├── Fortress (requires Shield Wall)
    └── Grandmaster (requires Weapon Specialization)
```

#### Skill Point Allocation
- **Linear Costs**: Each rank costs the same
- **Progressive Costs**: Higher ranks cost more
- **Prerequisite System**: Must meet requirements to unlock
- **Branching Paths**: Multiple viable build options

## 🛡️ Equipment System

### Equipment Slots
- **Main Hand**: Primary weapon
- **Off Hand**: Secondary weapon, shield, or focus
- **Armor**: Body protection
- **Helmet**: Head protection
- **Boots**: Foot protection
- **Gloves**: Hand protection
- **Accessories**: Rings, amulets (multiple slots)

### Equipment Tiers

#### Quality Levels
- **Common** (White): Basic equipment
- **Uncommon** (Green): Enhanced stats
- **Rare** (Blue): Significant bonuses
- **Epic** (Purple): Powerful effects
- **Legendary** (Orange): Unique abilities
- **Artifact** (Red): Game-changing powers

#### Equipment Properties
- **Base Stats**: Core attribute bonuses
- **Special Properties**: Unique effects
- **Set Bonuses**: Benefits for wearing matching pieces
- **Enchantments**: Magical enhancements
- **Durability**: Equipment degradation over time

### Customization Options

#### Enchanting
- **Stat Enhancement**: Boost existing properties
- **New Properties**: Add completely new effects
- **Elemental Damage**: Add fire, ice, lightning damage
- **Resistance**: Add protection against damage types

#### Crafting
- **Material Quality**: Better materials = better equipment
- **Crafting Skills**: Player skill affects results
- **Recipe Discovery**: Find new crafting patterns
- **Modification**: Alter existing equipment

## 🎯 Character Builds

### Build Archetypes

#### Glass Cannon
- **Focus**: Maximum damage output
- **Trade-offs**: Low survivability
- **Stats**: High STR/DEX/INT, low CON
- **Playstyle**: High risk, high reward

#### Tank
- **Focus**: Maximum survivability
- **Trade-offs**: Lower damage
- **Stats**: High CON, moderate STR
- **Playstyle**: Defensive, team-oriented

#### Balanced
- **Focus**: Well-rounded capabilities
- **Trade-offs**: Not exceptional in any area
- **Stats**: Even distribution
- **Playstyle**: Adaptable, reliable

#### Support
- **Focus**: Team enhancement
- **Trade-offs**: Limited solo capability
- **Stats**: High WIS/CHA, moderate others
- **Playstyle**: Team-dependent, strategic

### Build Viability

#### Design Goals
- **Multiple Solutions**: Different builds can solve the same challenges
- **Situational Advantages**: Each build excels in specific scenarios
- **Player Expression**: Builds reflect player preferences
- **Evolution**: Builds can change as characters progress

## 🔄 Character States

### Health Management

#### Health States
- **Healthy** (75-100%): No penalties
- **Injured** (50-74%): Minor accuracy penalty
- **Wounded** (25-49%): Reduced movement speed
- **Critical** (1-24%): Severe penalties to all actions
- **Unconscious** (0%): Cannot act, making death saves

#### Recovery Methods
- **Natural Healing**: Slow recovery over time
- **Magical Healing**: Instant recovery via spells
- **Potions/Items**: Consumable healing items
- **Rest**: Accelerated healing during downtime

### Resource Management

#### Mana System
- **Spell Costs**: Each spell consumes mana
- **Regeneration**: Slow natural recovery
- **Overcast**: Spend health when mana is depleted
- **Mana Burn**: Some abilities drain enemy mana

#### Stamina System
- **Physical Actions**: Attacks, movement consume stamina
- **Exhaustion**: Low stamina reduces effectiveness
- **Recovery**: Fast natural regeneration
- **Fatigue**: Temporary stamina reduction from overexertion

---

*This document defines the character systems that form the foundation of player progression and customization. Balance values are subject to testing and iteration.*