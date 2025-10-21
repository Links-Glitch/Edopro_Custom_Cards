# 🃏 Links-Glitch's Custom EDOPro Cards

Welcome to the official repository for custom Yu-Gi-Oh! cards designed by **Links-Glitch**.

These cards are created using **DataEditorX** and **Lua scripting** for use with the **EDOPro** simulator (formerly YGOPro).

---

## 🐲 Featured Card: Greed Lizard

### Card ID: `55500001`

| Attribute | Detail |
| :--- | :--- |
| **Name** | Greed Lizard |
| **Type** | Monster (Effect) |
| **Attribute** | DARK |
| **Level** | 3 |
| **ATK / DEF** | 1000 / 1000 |
| **Effect** | If this card is Normal Summoned or Special Summoned: You can shuffle 1 card from your hand into the Deck, and if you do, draw 1 card. You can only use this effect of "Greed Lizard" once per turn. |

---

## 🛠️ How to Install These Cards

To use these custom cards in your EDOPro client, follow these simple steps.

### 1. Download the Files

You can clone this repository or simply download the necessary files:

* **Database Data:** `cards.cdb` (Contains the card's name, stats, and effect text).
* **Script Logic:** The `script/` folder (Contains the `55500001.lua` file, which makes the effect work).
* **Card Image (Optional):** The `pics/` folder (Contains the card's artwork image).

### 2. Move the Files into EDOPro

Navigate to your main **EDOPro installation folder** (e.g., `C:/Program Files/EDOPro/`).

| File Type | Source Folder | EDOPro Destination | Notes |
| :--- | :--- | :--- | :--- |
| **Database** | `cards.cdb` | Place directly into the **`deck`** folder | This file contains the card's data. |
| **Script** | `script/55500001.lua` | Place into the **`script`** folder | This file enables the card's effects. |
| **Image** | `pics/55500001.png` | Place into the **`pics/card/`** folder | Recommended for visual quality. |

### 3. Restart EDOPro

Close and reopen EDOPro. You should now be able to find **Greed Lizard** in the deck editor by searching for its name or Card ID (`55500001`).

---

## 🤝 Contribution & Feedback

This is my first custom card! I appreciate any feedback on balance, card design, or script functionality.

* Feel free to open an **Issue** if you find a bug.
* Suggestions for future cards are welcome!

---

**Made with 🦎 by Links-Glitch**
