# Suit Builder Spreadsheet

An Excel workbook for planning and tracking equipment suits in **Ultima Online**. You enter each gear slot's item properties, and the sheet adds them up across the suit. It also works out the character's final stats, including race and mastery bonuses.

## File

| File | Description |
| --- | --- |
| `UO_Suit_Builder.xlsx` | The suit builder workbook |

Requires Excel 2019 or Microsoft 365. The bonus formulas use `SWITCH`, which older versions don't support.

## Worksheets

| Sheet | Purpose |
| --- | --- |
| **Suit Template** | Blank suit. Copy it to start a new character. |
| **Chart1** | Bar chart comparing item properties across Cork's gear slots |
| **Cork (Chesapeake)** | Suit for the character Cork on the Chesapeake shard |
| **Penthesilea (Chesapeake)** | Suit for the character Penthesilea on the Chesapeake shard |
| **Ghanima (Atlantic)** | Suit for the character Ghanima on the Atlantic shard |
| **Mondain Event Items** | Collection tracker for Mondain event rewards |

## Suit sheet layout

### Equipment grid (rows 3–20)

Each row is one gear slot. Enter the item name in column A and its properties in the columns to the right. Row 20 (**TOTAL**) sums every column.

Slots: Head, Earrings, Neck, Talisman, Chest, Arms, Hands, Apron/Belt, Sash, Cloak, Robe, Legs, Feet, Ring, Bracelet, Weapon, Shield.

| Group | Columns |
| --- | --- |
| Resistances | PHY, FIRE, COLD, POISON, ENERGY |
| Stats | STR, DEX, INT, HP, STA, MANA |
| Regens | HPR (hit point regen), SR (stamina regen), MR (mana regen) |
| Combat | HCI, DCI, DI, SSI, HLD (hit lower defense), HLA (hit lower attack) |
| Magic | FC, FCR, SDI, LMC, LRC, CF (casting focus), SC (spell channeling) |
| Misc | SoulCh (Soul Charge), EP (enhance potions), Luck, RP (reflect physical) |
| Eaters | DMG, KIN, FIR, COL, POI, ENY |

### Base stats and totals (rows 21–22)

- **Row 21, BASE STATS (No Gear):** enter the character's unbuffed stats by hand.
- **Row 22, STAT TOTAL (Geared):** calculated from base stats, gear and bonuses.
  - **HP** = STR ÷ 2 + 50 + HP bonus from gear. The gear bonus is capped at 25.
  - **STA** = DEX + stamina from gear.

### Mastery and race (column P)

Pick the character's **Mastery** (P22) and **Race** (P24) from the dropdowns. The sheet applies these bonuses on its own:

| Selection | Bonus |
| --- | --- |
| Archery, Fencing, Mace Fighting, Swordsmanship or Throwing mastery | +5 HCI, +5 DCI, +5 DI, +5 STR |
| Bushido, Chivalry or Ninjitsu mastery | +15 Mana |
| Human | +2 HPR |
| Elf | +20 Mana |

### Skills (rows 25–35)

Choose up to eight skills from the dropdown in column C. For each one, enter the **REAL** (trained) value and the **ITEMS** bonus from gear. **SUM** adds the two, and the **TOTAL** row gives the overall skill point totals.

## Adding a new character

1. Right-click the **Suit Template** tab and choose **Move or Copy → Create a copy**.
2. Rename the copy `Name (Shard)`, matching the existing sheets.
3. Pick the mastery and race, then enter base stats, gear and skills.

## Mondain Event Items

Tracks how many of each Mondain event reward you've collected, broken down by variant number:

- Scrolls (An, Corp, Hur, In, Kal, Mani, Tym, Vas)
- Obelisks, grouped by rarity (Common to Uber Rare)
- Skull of Mondain
- Black Compendium
- Bust of Mondain
