# World Ablaze Multiplayer Fix (Submod)

Small balance/QoL submod for **World Ablaze** multiplayer games.  
Focus: smoothing out a few MP pain points with lightweight scripted effects (startup + monthly checks, no heavy polling).

## Requirements
- **World Ablaze (main mod)** must be enabled.
- All players in MP must run the **same mod list and load order**.

## What this submod changes

### 1) Axis land doctrine mastery boost (GER / ITA / JAP)
From **1939 onward** (scripted date gate), **Germany, Italy, and Japan** receive a national spirit that:
- **+200% Land Doctrine Mastery Gain**

Applied once, automatically.

---

### 2) Germany (GER): manpower on France capitulation
When **France capitulates** while **Germany is at war with France**, Germany gains:
- **+500,000 manpower**

One-time effect.

---

### 3) Japan (JAP): starting convoys
At game start, Japan receives:
- **+200 convoys** (added to stockpile)

One-time effect.

---

### 4) Soviet Union (SOV): focus-gated industry + infrastructure
These effects trigger **once** after the listed focuses are completed.

#### A) “Evolve Our Urban Centres”
Adds **civilian factories** to western hubs:
- **Kyiv (state 202): +10 Civs +10 slots**
- **Minsk (state 206): +10 Civs +10 slots**
- **Riga (state 966): +10 Civs +10 slots**

**Total:** **+30 civilian factories** and **+30 building slots**

#### B) “Extend the Working Week”
Adds **military factories** to the same hubs:
- **Kyiv (state 202): +10 Mils +10 slots**
- **Minsk (state 206): +10 Mils +10 slots**
- **Riga (state 966): +10 Mils +10 slots**

**Total:** **+30 military factories** and **+30 building slots**

#### C) “A Secure Industrial Base”
Adds **infrastructure** across a set of rear/resource states:
- **+2 Infrastructure** in **22 states**  
  (IDs: 653, 572, 876, 402, 583, 586, 589, 588, 40, 570, 579, 577, 578, 569, 564, 565, 563, 561, 657, 560, 409, 408)

**Total:** 22 × 2 = **+44 infrastructure levels**

---

### 5) Italy (ITA): resources + focus-linked construction + naval armor rebalance

#### A) Steel boost (state-based, control-dependent)
- **State Northern Sicily:** **+150 Steel**
- Active **only while Italy controls the state** (removed if control is lost).

#### B) Libya oil program (focus-dependent, control-dependent)
After completing **“Develop the Empire”**, Libya oil modifiers activate:
- **7 Libyan states:** **+10 Oil each** (total **+70 Oil**)  
- Active while controlled by **Italy / Italian Libya**.  
- If Italy loses control **after** the focus, the modifier is removed.

#### C) Instant buildings from Italian focuses
When the relevant focus is completed (and Italy controls the required state), buildings are added instantly:

- After **“Italian Army”**:
  - **State Northern Sicily:** **+20 Military Factories** + **+20 slots**

- After **“Italian Highways”**:
  - **State Northern Sicily:** **+20 Civilian Factories** + **+20 slots**

- After **“Italian Navy”**:
  - **State Southern Sicily:** **+15 Dockyards** + **+15 slots**

Anti-snipe behavior:
- If Italy later **loses control of state 115**, any granted factories tied to that state are removed (prevents an opponent from inheriting free industry there).

#### D) Naval armor module for battleships (Littorio)
The heavy ship armor module **ship_armor_370_140** is buffed:
- **Armor: was 323 become 395**

Net effect: heavy armor is meaningfully stronger, but comes with real cost/speed trade-offs.

---

## Notes / Status
- A “German torpedo crisis” idea exists in the files, but it is **currently disabled** (no gameplay effect).

## Installation
Enable:
1) **World Ablaze**
2) **World Ablaze Multiplayer Fix (this submod)**

Place the submod **after** World Ablaze in load order.

---
