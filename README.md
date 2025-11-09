# 🏎️ Bloxy Kart — Publishing Guide
**Developer:** Gaurav Chauhan (VenomVolt)  
**Built with:** Roblox Studio + Lua

![Bloxy Kart Banner](https://media.giphy.com/media/l0MYEqEzwMWFCg8rm/giphy.gif)

---

## Quick Badges
![Roblox Studio](https://img.shields.io/badge/Game%20Engine-Roblox%20Studio-blue?style=for-the-badge&logo=roblox)
![Lua](https://img.shields.io/badge/Language-Lua-orange?style=for-the-badge&logo=lua)

---

## Step-by-step Publishing Guide (1 → 9, continuous)

1. **Open the Lobby**  
   - Launch **Roblox Studio** and open your **Lobby** file.  
   - This is the main hub where players gather before a race.

2. **Publish the Lobby as a Separate Universe**  
   - In Roblox Studio: **File → Publish to Roblox As...**  
   - Create a **new Game Universe** for the Lobby.  
   - The Lobby must be its own universe because the Race Engine will be a sub-place inside it.

3. **Open the Race Engine**  
   - Open your **Race Engine** project/file.  
   - This contains racing logic: checkpoints, vehicles, lap detection, etc.

4. **Publish the Race Engine inside the Lobby Universe**  
   - Publish the Race Engine as a **new Place** under the Lobby’s universe (so the Lobby can teleport players into it).
   - Conceptually: **Lobby → Race Engine** (Lobby is the parent universe; Race is a place inside it).

5. **Get the Place IDs**  
   - After publishing both, copy the two Place IDs:  
     - **Lobby Place ID**  
     - **Race Engine Place ID**

6. **Configure `BloxyKartService` and finalize (continued steps 7, 8, 9 are part of this flow)**  
   - Inside **ReplicatedStorage**, open the `ModuleScript` named `BloxyKartService`.  
   - Find this code block:
     ```lua
     Lobby = 0,
     RaceGame = 0
     ```
   - Replace the `0` values with your **actual Place IDs**, for example:
     ```lua
     Lobby = 1234567890,
     RaceGame = 9876543210
     ```
   - **Make this change in both the Lobby project and the Race Engine project** so both know each other's IDs.
   - **7. Save & Publish:**  
     - Save the changes in both projects (Lobby and Race Engine).  
     - In each project: **File → Publish to Roblox**.  
     - ✅ Now the Lobby and Race Engine are linked and live.
   - **8. Test & Enjoy the Ride:**  
     - Open the Lobby in Roblox (play/test) and verify it teleports to the Race Engine as expected.  
     - Invite friends and run a few test races. Adjust spawn points, checkpoints, or kart settings if needed.  
   - **9. Credits & Next Steps:**  
     - Developer: **Gaurav Chauhan (VenomVolt)**  
     - Repo: `github.com/GAuravgiy87/Bloxy-Kart-Open-Sourced-Edition` (replace with your real repo link if different)  
     - Pro tips: add tracks, particles, custom karts, a leaderboard, and extra game modes. Consider packaging screenshots in `images/` and linking them below.

---

## Optional: Screenshots (add images/ folder to repo)
```markdown
![Bloxy Kart Lobby](images/lobby.png)
![Bloxy Kart Race Engine](images/race.png)
![Bloxy Kart Gameplay](images/gameplay.png)
