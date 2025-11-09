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

> 🏁 **Bloxy Kart** is a high-speed, open-source Roblox racing experience — built with creativity, code, and caffeine ☕.  
> Follow this guide to set up, link, and publish your **Lobby** and **Race Engine** correctly.

---

## ⚙️ Step-by-Step Publishing Guide

### 🏁 1. Open the Lobby  
- Launch Roblox Studio.  
- Open your **Lobby** file.  
- This is the **main entry point** where players spawn and wait before racing.

---

### 🌐 2. Publish the Lobby as a Separate Universe  
- Go to **File → Publish to Roblox As...**  
- Create a **new Game Universe** for the Lobby.  
> 💡 The Lobby must be its own universe — the Race Engine will become a sub-place inside it.

---

### 🧠 3. Open the Race Engine  
- Open your **Race Engine** file.  
- It contains all core racing logic, checkpoints, vehicles, and mechanics.

---

### 🔗 4. Publish the Race Engine *Inside the Lobby*  
- Publish the Race Engine as a **new Place** within your Lobby’s universe.  
> 🎯 Think of it as a portal: **Lobby ➜ Race Engine**  

---

### 🆔 5. Get the Place IDs  
Once published, copy these IDs:
- 🪪 **Lobby Place ID**
- 🪪 **Race Engine Place ID**

> You’ll need these in the next step.

---

### 🧩 6. Configure `BloxyKartService`
Inside **ReplicatedStorage**, open the file:  
`ModuleScript → BloxyKartService`

Find this code block:
```lua
Lobby = 0,
RaceGame = 0

Replace the zeros with your actual Place IDs:

Lobby = 1234567890,
RaceGame = 9876543210


🔁 Do this in both the Lobby and Race Engine projects.


---

### 💾 7. Save & Publish  
- Save your changes in **both** files (Lobby & Race Engine).  
- Go to **File → Publish to Roblox** for each project.  

✅ That’s it! Your Bloxy Kart system is now **linked and live** 🚀  

---

### 🎮 8. Enjoy the Ride!  
You’ve successfully connected your Lobby and Race Engine!  
Now invite your friends, customize your tracks, and **race like a pro** 🏆  

<p align="center">
  <img src="https://media.giphy.com/media/3ohhwJL0G6Qx3xM2l6/giphy.gif" width="70%" alt="Racing Animation"/>
</p>

> 🏎️ Tip: Try adding new vehicles, custom sounds, or lighting effects for a more dynamic race!

---

## 🧱 Credits  

👨‍💻 **Developer:** Gaurav Chauhan *(VenomVolt)*  
🛠️ **Built With:** Roblox Studio + Lua  
📦 **Repository:** [github.com/GAuravgiy87/Bloxy-Kart-Open-Sourced-Edition](https://github.com/GAuravgiy87/Bloxy-Kart-Open-Sourced-Edition)  

---

<p align="center">
  <img src="https://media.giphy.com/media/l0MYEqEzwMWFCg8rm/giphy.gif" width="80%" alt="Bloxy Kart Banner"/>
</p>

<p align="center">
  Made with ❤️ by <b>Gaurav Chauhan (VenomVolt)</b>  
  <br>
  <sub>“Racing is life. Everything else is just waiting.” 🏎️</sub>
</p>
