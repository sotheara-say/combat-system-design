# Abilities & Skills Design

## 🌟 Ability Framework

### Ability Categories

#### **Active Abilities**
- **Instant**: Immediate effect, no duration
- **Channeled**: Continuous effect while active
- **Persistent**: Ongoing effect for set duration
- **Toggle**: Can be turned on/off at will

#### **Passive Abilities**
- **Permanent**: Always active
- **Conditional**: Active under specific circumstances
- **Triggered**: Activate on certain events
- **Aura**: Affect nearby allies/enemies

### Resource Costs

#### Cost Types
- **Mana**: Magical energy consumption
- **Stamina**: Physical energy consumption
- **Health**: Life force expenditure
- **Combo Points**: Built-up combat momentum
- **Cooldown**: Time-based limitation

## ⚔️ Combat Abilities

### Warrior Abilities

#### **Power Attack**
- **Type**: Active, Instant
- **Cost**: 2 Stamina
- **Effect**: +50% damage, -10% accuracy
- **Cooldown**: None
- **Description**: Sacrifice accuracy for raw power

#### **Shield Bash**
- **Type**: Active, Instant
- **Cost**: 3 Stamina
- **Effect**: Moderate damage + Stun (1 turn)
- **Cooldown**: 3 turns
- **Requirements**: Shield equipped
- **Description**: Stunning attack that opens enemies to follow-up

#### **Berserker Rage**
- **Type**: Active, Persistent
- **Cost**: 5 Stamina per turn
- **Effect**: +25% damage, +15% attack speed, -20% defense
- **Duration**: Until cancelled or stamina depleted
- **Description**: Uncontrolled fury increases offense at cost of defense

#### **Whirlwind**
- **Type**: Active, Instant
- **Cost**: 8 Stamina
- **Effect**: Attack all adjacent enemies
- **Cooldown**: 5 turns
- **Description**: Spinning attack hits multiple foes

### Rogue Abilities

#### **Backstab**
- **Type**: Active, Instant
- **Cost**: 4 Stamina
- **Effect**: +100% damage if attacking from behind
- **Cooldown**: 2 turns
- **Description**: Devastating attack on unsuspecting enemies

#### **Stealth**
- **Type**: Active, Persistent
- **Cost**: 3 Stamina per turn
- **Effect**: Invisible to enemies, +50% crit chance on first attack
- **Duration**: Until attacking or stamina depleted
- **Description**: Become invisible to set up surprise attacks

#### **Poison Blade**
- **Type**: Active, Toggle
- **Cost**: 2 Mana per attack
- **Effect**: Attacks apply poison (3 damage/turn for 5 turns)
- **Description**: Coat weapons with deadly toxins

#### **Evasion**
- **Type**: Passive, Triggered
- **Effect**: 15% chance to avoid any attack
- **Description**: Natural agility allows dodging some attacks

### Mage Abilities

#### **Fireball**
- **Type**: Active, Instant
- **Cost**: 8 Mana
- **Effect**: High fire damage, small area effect
- **Range**: Long
- **Cooldown**: None
- **Description**: Classic destructive spell

#### **Ice Storm**
- **Type**: Active, Persistent
- **Cost**: 12 Mana
- **Effect**: Moderate cold damage over large area for 3 turns
- **Range**: Long
- **Cooldown**: 8 turns
- **Description**: Devastating area control spell

#### **Magic Shield**
- **Type**: Active, Persistent
- **Cost**: 6 Mana + 2 Mana per turn
- **Effect**: Absorbs next 20 damage
- **Duration**: Until broken or cancelled
- **Description**: Protective barrier of magical energy

#### **Mana Burn**
- **Type**: Active, Instant
- **Cost**: 5 Mana
- **Effect**: Drain 10 enemy mana, deal damage equal to mana drained
- **Range**: Medium
- **Description**: Attack enemy's magical reserves

### Support Abilities

#### **Heal**
- **Type**: Active, Instant
- **Cost**: 6 Mana
- **Effect**: Restore 25 HP to target
- **Range**: Medium
- **Cooldown**: None
- **Description**: Basic healing magic

#### **Blessing**
- **Type**: Active, Persistent
- **Cost**: 8 Mana
- **Effect**: +2 to all rolls for 10 turns
- **Range**: Touch
- **Description**: Divine favor enhances all actions

#### **Dispel Magic**
- **Type**: Active, Instant
- **Cost**: 4 Mana
- **Effect**: Remove all magical effects from target
- **Range**: Medium
- **Description**: Neutralize magical enhancements and curses

## 🌳 Skill Trees

### Tree Design Philosophy

#### **Horizontal Progression**
- Multiple paths at each tier
- Specialization vs. generalization choices
- Synergies between different branches

#### **Vertical Progression**
- Clear power progression
- Prerequisites create meaningful choices
- Capstone abilities as ultimate goals

### Example: Warrior Skill Tree

```
                    [Weapon Master]
                           |
        ┌───────────────────────┐
        |                     |
   [Berserker]           [Guardian]
        |                     |
   ┌─────┴─────┐           ┌─────┴─────┐
   |         |           |         |
[Rage]   [Frenzy]   [Taunt]  [Shield Wall]
   |         |           |         |
[Rampage] [Fury]    [Protect] [Fortress]
```

#### Skill Point Investment
- **Total Points**: 3 per level
- **Prerequisites**: Must invest in lower tiers first
- **Specialization**: Bonus points for focusing on one branch
- **Respec Options**: Limited ability to redistribute points

### Cross-Class Skills

#### **Universal Skills**
- Available to all classes
- General combat improvements
- Utility abilities

#### **Multiclass Synergies**
- Abilities that combine class features
- Require investment in multiple trees
- Unique hybrid capabilities

## ⚡ Ability Mechanics

### Scaling Systems

#### **Attribute Scaling**
```
Damage = Base_Damage + (Primary_Attribute × Scaling_Factor)
```

#### **Level Scaling**
- Base effects improve with character level
- New effects unlock at specific levels
- Efficiency increases reduce resource costs

### Combo System

#### **Combo Points**
- Generated by basic attacks and certain abilities
- Consumed by special "finisher" abilities
- Different abilities generate different amounts

#### **Combo Abilities**
- **Light Finishers** (3 points): Quick, efficient abilities
- **Heavy Finishers** (6 points): Powerful, dramatic effects
- **Ultimate Finishers** (10 points): Game-changing abilities

### Synergy Mechanics

#### **Elemental Combinations**
- Fire + Ice = Steam (area damage)
- Lightning + Water = Electrocution (chain damage)
- Earth + Fire = Lava (persistent damage zones)

#### **Status Combinations**
- Wet + Lightning = Increased shock damage
- Poisoned + Fire = Toxic flames (enhanced DoT)
- Bleeding + Ice = Slower healing

## 🔄 Resource Management

### Mana System

#### **Mana Pool**
- Base pool determined by Intelligence and class
- Regeneration rate based on Wisdom
- Maximum efficiency at 50%+ mana

#### **Mana States**
- **Full** (80-100%): Bonus to spell effectiveness
- **Normal** (30-79%): Standard performance
- **Low** (10-29%): Reduced spell power
- **Critical** (0-9%): Risk of spell failure

### Stamina System

#### **Stamina Pool**
- Base pool from Constitution and Strength
- Fast regeneration during non-combat
- Slower regeneration during combat

#### **Fatigue Mechanics**
- Overexertion causes temporary stamina reduction
- Recovery requires rest or specific abilities
- Persistent fatigue affects all physical actions

### Cooldown Management

#### **Cooldown Types**
- **Global Cooldown**: Affects all abilities briefly
- **Ability Cooldown**: Specific to individual abilities
- **Category Cooldown**: Affects groups of similar abilities

#### **Cooldown Reduction**
- Attribute bonuses reduce cooldowns
- Equipment provides cooldown reduction
- Some abilities reset others' cooldowns

## 🎯 Ability Balance

### Power Budget

#### **Resource Cost**
- More powerful effects cost more resources
- Efficient abilities have limitations
- High-cost abilities provide proportional benefit

#### **Opportunity Cost**
- Using one ability prevents using others
- Turn economy creates meaningful choices
- Preparation abilities require setup time

### Risk vs. Reward

#### **High-Risk Abilities**
- Powerful effects with significant drawbacks
- Chance of failure or backfire
- Self-damage or vulnerability windows

#### **Safe Abilities**
- Reliable but moderate effects
- Low resource costs
- Minimal risk of failure

### Situational Design

#### **Contextual Effectiveness**
- Some abilities excel against specific enemy types
- Environmental factors affect ability performance
- Party composition influences ability value

#### **Scaling Relevance**
- Early-game abilities remain useful
- End-game abilities aren't always superior
- Niche abilities have their moments to shine

---

*This document outlines the ability and skill systems that provide depth and customization to character development. All values are subject to balance testing.*