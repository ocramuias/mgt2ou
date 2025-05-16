🔁 DevPubMapperMod
This mod allows you to dynamically remap Developer-to-Publisher relationships over time. You can define mappings by ID, with optional year-based conditions.

📘 Example configuration (dev_pub_map.txt)
```txt
# DeveloperID=PublisherID
# Year-based mapping
12,1976=3
12,1977=4
12,1978=14
# Permanent mapping without year
8=3
```

✅ What it does:
Developer ID 12 changes publisher across different years: from 3 to 4 to 14.
Developer 8 is always mapped to publisher 3.

🎨 PublisherNameChangeMod
This mod lets you customize a publisher's name and logo over time based on the current year. You can reflect brand evolution, historical naming, or internal storytelling.

📘 Example configuration (publisher_name_map.txt)
```txt
16,1977=This was Microsoft|0
16,1985=Microsoft|0
16,2000=Xbox Studios|0
16=Microsoft|0
```

✅ What it does:
Publisher ID 16 will display different names over time:
1977: “This was Microsoft”
1985: “Microsoft”
2000: “Xbox Studios”
For unspecified years: “Microsoft”
The |0 sets the logo ID (optional).

🚫 Note: Custom names do not apply to subsidiaries owned by the player—they retain their original names for consistency.

📄 fusion_map.txt Format – Fusion Mod
This file defines company mergers by mapping an old company ID to a new owner ID starting from a specific year. Each line represents one fusion event.

```txt
[OLD_ID]=[NEW_ID],[YEAR]
Example:
125=126,1978
```

Explanation:
In 1978, company with ID 125 (e.g., Test Slave) is merged into company with ID 126 (e.g., Test Master).

All IPs and games owned by 125 are transferred to 126.
Company 125 is hidden after the merger (not deleted, just deactivated).
You can define multiple fusions for the same company if needed, in chronological order.


📦 Compatibility
The two mods are fully optional and work independently or together.
Easily configurable via .txt files located in BepInEx/config.

🛠️ Requirements
Requires BepInEx installed in your game.
Automatically loaded at game start.


