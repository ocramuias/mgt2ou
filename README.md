# Mad Games Tycoon 2 – Mod Collection

A set of mods that expand and customize core simulation mechanics in **Mad Games Tycoon 2**.

---

## **DevPubMapperMod**

Dynamically remap **Developer → Publisher** relationships over time using simple configuration.

### 📘 Example (`dev_pub_map.txt`)
```
# DeveloperID=PublisherID
12,1976=3
12,1977=4
12,1978=14
8=3
```

### ✅ What It Does
- Developer ID `12` switches publisher depending on year: `3 → 4 → 14`
- Developer ID `8` is always mapped to publisher `3`

---

## **PublisherNameChangeMod**

Customize a publisher’s **name and logo** over the years for storytelling or historical branding.

### 📘 Example (`publisher_name_map.txt`)
```
16,1977=This was Microsoft|0
16,1985=Microsoft|0
16,2000=Xbox Studios|0
16=Microsoft|0
```

### ✅ What It Does
- Publisher ID `16` shows different names over time
- The `|0` sets the logo ID (optional)
- Unspecified years fall back to the last defined name

> ⚠️ Subsidiaries owned by the player are not renamed.

---

## **Fusion Mod**

Define company mergers with ownership and IP transfers via a text file.

### 📘 Example (`fusion_map.txt`)
```
125=126,1978
```

### ✅ What It Does
- In `1978`, company `125` merges into `126`
- All IPs/games transfer to the new owner
- Company `125` is hidden (not deleted)
- Supports multiple fusions in chronological order

> 💡 Combine with `PublisherNameChangeMod` to rename the merged company.

---

## **GamePilot Mod**

Inject fully custom AI-generated games into the simulation, controlled via text.

> ✅ Version: `0.0.92`  
> 🛠 Requires: BepInEx  
> 🎯 Compatible with: Mad Games Tycoon 2 (Steam)

### 📘 Example (`gamepilot.txt`)
```
GTA: San Andreas <Y2004><G1><T4><D3><P2><O1><PL1><PL3><SEQ:GTA: Vice City><%90><TG2>
```

Define genre, theme, year, platforms, relationships (sequel, remaster, etc.) and more.

---

## **Installation**

1. **Install BepInEx**  
   https://github.com/BepInEx/BepInEx/releases  
   Extract into your game folder.

2. **Place mod DLLs** into:  
   `BepInEx/plugins/`

3. **Place config files** into:  
   `BepInEx/config/`

4. *(Optional)* Enable debug mode in code:  
   `GamePilotMod.debugMode = true;`

5. **Launch the game**  
   If successful, logs will show:  
   `[GamePilot] Mod successfully loaded.`

---

## **Files Overview**

| File                    | Description                                |
|-------------------------|--------------------------------------------|
| `gamepilot.txt`         | Defines injected AI games                  |
| `dev_pub_map.txt`       | Dynamic developer → publisher mapping      |
| `publisher_name_map.txt`| Name/logo changes for publishers over time |
| `fusion_map.txt`        | Merges companies and transfers IPs         |

---

## **Requirements**

- ✅ BepInEx installed correctly
- ✅ Game loads mods automatically
- ✅ Compatible with latest Steam version

---

## **Author**

Created by **Ocram Uias**  
Feedback, suggestions and pull requests are welcome!



