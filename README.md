# 📢 Lifeinvader Script for ESX FiveM 📢

**Version:** 2.0.1
**Developer:** Novek  
**Discord:** [Join Support Discord](https://discord.gg/8q8BnmgXq2)  
**Tebex Store:** [Buy Here](https://noveks-workspace.tebex.io/package/6527061)

---

## 📄 **Overview**

Transform your FiveM server into a dynamic advertising platform with the **Lifeinvader Script**. This script allows players to create, post, and interact with in-game advertisements. From promoting businesses to hosting events, Lifeinvader integrates seamlessly into your roleplay server. It comes with powerful features like Discord integration for logging, flexible pricing, and customizable locations.

---

## ✨ **Features:**

- 🎨 **Custom UI:**  
  A modern and stylish design tailored to your server’s aesthetics, making the ad creation process intuitive for players.

- 🛡️ **Discord Integration:**  
  Lifeinvader logs all ads to Discord via webhooks. Admins can monitor ad activity in real time, ensuring transparency and control.

- 🔐 **Anonymous Ads:**  
  Players can choose to place ads either with their in-game name or anonymously for privacy.

- ⚡ **Efficient Database Management:**  
  The script uses **oxmysql** for fast, secure, and scalable database management, ensuring minimal impact on server performance.

- 🏷️ **Pricing Flexibility:**  
  Charge players for posting ads based on the number of characters, adding an economic layer to your server.

- 📍 **Interactive Map Locations:**  
  Players can interact with designated Lifeinvader spots on the map to post or view ads. Markers and blips guide players to these locations.

---

## 📑 **Requirements:**

- **ESX 1.2** or **ESX Legacy**
- **oxmysql** (for database integration)

---

## 🛠️ **Installation:**

1. **Download the Script:**  
   Place the script files in your **`resources`** folder.

2. **Add to `server.cfg`:**  
   Add the following line to ensure the script is loaded:
   ```lua
   ensure cfx_lifeinvader
   ```

3. **Set Up Database:**  
   Ensure **oxmysql** is set up for your server. The script uses **oxmysql** for managing ads and related data.

4. **Configuration:**  
   Open the **`config.lua`** file to set up custom locations, prices, Discord webhooks, and other preferences.

---

## 📝 **Configuration Example:**

```lua
Noveks_CFG = {}

-- ================================================
-- Discord Webhook for Admin Logs
Noveks_CFG.Log = {
    name = "LifeInvader",  -- Name of the bot for the Discord webhook
    color = "16711686",    -- Color for the embed in Discord (decimal)
    title = "LifeInvader", -- Title for the embed
    user = "https://discord.com/api/webhooks/YOUR_WEBHOOK_ID",  -- User log webhook URL
    admin = "https://discord.com/api/webhooks/YOUR_WEBHOOK_ID", -- Admin log webhook URL
}

-- ================================================
-- Lifeinvader Positions on the Map
Noveks_CFG.Positions = {
    vector3(-1082.4315, -247.6796, 36.7632),  -- Add more locations as needed
}

-- ================================================
-- Advertisement Settings
Noveks_CFG.MaxLetters = 150  -- Max characters allowed per ad
Noveks_CFG.MinLetters = 3    -- Minimum characters for an ad
Noveks_CFG.PricePerLetter = 2  -- Price per character
Noveks_CFG.MoneyAccount = "money"  -- Account from which the money is deducted
Noveks_CFG.LastVisibleAds = 10  -- Number of recent ads shown

-- ================================================
-- Marker Settings for LifeInvader Locations
Noveks_CFG.Marker = {
    type = 1,  -- Type of the marker
    scale = vector3(1.0, 1.0, 1.0),  -- Marker size
    rgba = {r = 255, g = 0, b = 0, a = 255},  -- Marker color (Red)
    bobUpAndDown = false,  -- Does the marker move?
    faceCamera = false,  -- Should the marker face the camera?
    rotate = false,  -- Should the marker rotate?
    distance = 50.0,  -- Distance at which marker becomes visible
    interactDistance = 2.0,  -- Distance at which players can interact
}

-- ================================================
-- Blip Settings on Map
Noveks_CFG.Blip = {
    sprite = 77,  -- Icon displayed for LifeInvader blip on the map
    color = 2,    -- Blip color (Green)
    label = "LifeInvader",  -- Text displayed for the blip
    scale = 0.6   -- Scale of the blip
}
```

---

## 🚀 **How It Works:**

1. **Ad Creation:**  
   Players can visit any of the marked Lifeinvader locations on the map and create ads by interacting with a designated marker.

2. **Ad Payment:**  
   Players pay for the ad based on the number of characters they use. The script automatically deducts the correct amount from the player's balance.

3. **Discord Logs:**  
   Every ad posted is logged in Discord via webhooks. Admins can easily track all ad activity and ensure everything is in order.

4. **Advertising Locations:**  
   The Lifeinvader locations are marked with a customizable marker. Players can easily find these spots on the map using the **blips** and **markers**.

5. **Anonymity Options:**  
   Players have the option to post ads anonymously or with their in-game name, offering flexibility in how ads are displayed.

---

## 💬 **Support:**

If you have any questions or need support, feel free to join our **Support Discord**:  
[Noveks Support Discord](https://discord.gg/8q8BnmgXq2)

---

### 📑 **License:**

This script is **not open-source** and is licensed under the following terms:
- **Usage:** You may use this script only on your own server. Redistribution or resale is prohibited unless explicitly authorized by the developer.
- **Modifications:** You are not permitted to modify or distribute the script unless granted permission by the developer.
- **Commercial Use:** The script may not be used for commercial purposes without express consent from the developer.
