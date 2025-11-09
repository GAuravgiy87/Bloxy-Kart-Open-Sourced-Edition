<!-- BLOXY KART README -->
<h1 align="center">🏎️ Bloxy Kart — Publishing Guide</h1>

<p align="center">
  <img src="https://img.shields.io/badge/Game%20Engine-Roblox%20Studio-blue?style=for-the-badge&logo=roblox" />
  <img src="https://img.shields.io/badge/Language-Lua-orange?style=for-the-badge&logo=lua" />
  <img src="https://img.shields.io/badge/Developer-Gaurav%20Chauhan%20(VenomVolt)-purple?style=for-the-badge" />
</p>

---

<p align="center">
  <img src="https://media.giphy.com/media/l0MYEqEzwMWFCg8rm/giphy.gif" width="80%" alt="Bloxy Kart Animation"/>
</p>

> 🏁 **Bloxy Kart** is a high-speed Roblox racing experience — built with passion, code, and caffeine ☕.  
> Follow this guide to **publish and link your Lobby and Race Engine** the right way!

---

## ⚙️ Step-by-Step Publishing Guide

### 🏁 1. Open the Lobby  
- Open your **Lobby** file in Roblox Studio.  
- This is your **main entry point** — the central hub where players gather before the race.

---

### 🌐 2. Publish the Lobby as a Separate Universe  
- Go to **File → Publish to Roblox As...**  
- Create a **new game universe** for the Lobby.  
> 💡 The Lobby must be its own game universe because your Race Engine will be a sub-place inside it.

---

### 🧠 3. Open the Race Engine  
- Next, open your **Race Engine** file.  
- This contains the racing logic, checkpoints, vehicles, and race flow.

---

### 🔗 4. Publish the Race Engine Inside the Lobby  
- Publish this as a **new Place inside your Lobby’s universe**.  
> 🎯 Think of it like a portal: Lobby → Race Engine.

---

### 🆔 5. Get the Place IDs  
After both are published, copy:
- 🪪 **Lobby Place ID**
- 🪪 **Race Engine Place ID**

You’ll use these in the next step.

---

### 🧩 6. Configure `BloxyKartService`
1. Inside **ReplicatedStorage**, open the file:  
   `ModuleScript → BloxyKartService`
2. Find these lines:
   ```lua
   Lobby = 0,
replace
   Lobby = 1234567890,
RaceGame = 9876543210

   RaceGame = 0
