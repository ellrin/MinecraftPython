# MinecraftPython
This repository provides a tutorial for those who want to learn Python with Minecraft.

You will learn how to use Python to talk to Minecraft and do fun things like:
- Send chat messages
- Place blocks
- Build cool things

---

## ✨ What you need

- Minecraft Java Edition (version 1.12.2)
- Python 3 (we recommend 3.10)
- Forge 1.12.2 (to run mods)
- Raspberry Jam Mod (to connect Python and Minecraft)
- mcpi Python package
- Java 8 (only if you don’t have it yet)

---

## 📥 Download links

| Item              | Link                                                                                          |
|-------------------|-----------------------------------------------------------------------------------------------|
| Minecraft Java    | https://www.minecraft.net                                                                     |
| Forge 1.12.2      | https://files.minecraftforge.net/net/minecraftforge/forge/index_1.12.2.html                   |
| Raspberry Jam Mod | https://github.com/arpruss/raspberryjammod/tree/master                                        |
| Java 8            | https://www.oracle.com/java/technologies/javase/javase8-archive-downloads.html (need account) |

---

## 🍎 macOS install steps

1. **Install Minecraft Java**
   - Download and install Minecraft.
   - Open Minecraft and play version **1.12.2** once.

2. **Check if you have Java**
   - Open Terminal:
     ```
     java -version
     ```
   - If it shows `java version "1.8.x"` → you are good!
   - If you don’t have Java or have a newer version, install Java 8.

3. **Install Java 8 (if needed)**
   - Download and install `.dmg` file.
   - Check again:
     ```
     java -version
     ```

4. **Install Forge 1.12.2**
   - Download the `forge-1.12.2-xxx-installer.jar`.
   - Double-click → choose `Install client`.
   - Open Minecraft launcher → select **Forge** profile.

5. **Install Raspberry Jam Mod**
   - Download `.jar` file.
   - Copy it to:
     ```
     ~/Library/Application Support/minecraft/mods
     ```

6. **Install Python and mcpi**
   - Install Python 3.
   - Run in Terminal:
     ```
     pip install mcpi
     ```

7. **Start Minecraft**
   - Open Minecraft → select **Forge 1.12.2** → create a world (Creative mode).

8. **Run Python script**
   - Go to your script folder:
     ```
     cd ~/Desktop/minecraft-python
     python hello_minecraft.py
     ```

---

## 🪟 Windows install steps

1. **Install Minecraft Java**
   - Download and install Minecraft.
   - Open Minecraft and play version **1.12.2** once.

2. **Check if you have Java**
   - Open Command Prompt (cmd):
     ```
     java -version
     ```
   - If it shows `java version "1.8.x"` → you are good!
   - If you don’t have Java or have a newer version, install Java 8.

3. **Install Java 8 (if needed)**
   - Download and install `.exe` file.
   - Check again:
     ```
     java -version
     ```

4. **Install Forge 1.12.2**
   - Download the `forge-1.12.2-xxx-installer.jar`.
   - Double-click → choose `Install client`.
   - Open Minecraft launcher → select **Forge** profile.

5. **Install Raspberry Jam Mod**
   - Download `.jar` file.
   - Copy it to:
     ```
     C:\Users\<yourname>\AppData\Roaming\.minecraft\mods
     ```

6. **Install Python and mcpi**
   - Install Python 3 (check “Add to PATH” when installing).
   - Run in cmd:
     ```
     pip install mcpi
     ```

7. **Start Minecraft**
   - Open Minecraft → select **Forge 1.12.2** → create a world (Creative mode).

8. **Run Python script**
   - Go to your script folder:
     ```
     cd C:\Users\<yourname>\Desktop\minecraft-python
     python hello_minecraft.py
     ```

---

## 💬 Example Python script (`hello_minecraft.py`)

```python
from mcpi.minecraft import Minecraft

mc = Minecraft.create()
mc.postToChat("👋 Hello from Python!")

x, y, z = mc.player.getTilePos()
mc.setBlock(x + 1, y, z, 1)  # place a stone block
