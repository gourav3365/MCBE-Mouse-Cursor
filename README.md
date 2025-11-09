# Swim Mouse Cursor

A lightweight Windows utility to fix Minecraft Bedrock Edition's 1.21.121 mouse cursor escaping issues by keeping it confined to the game window.

## 🎮 What Does This Do?

This program automatically clips your mouse cursor to the Minecraft Bedrock window when the game is focused, preventing the cursor from escaping to other monitors or areas of your screen during gameplay. Works in both fullscreen and windowed modes!

## 📥 Installation

1. Download the latest release from the [Releases](../../releases) page.
2. Extract the `.exe` file to a folder of your choice.
3. Run `SwimMouseCursor.exe`

## 🚀 Usage

### Basic Usage
- Simply run the program and launch Minecraft Bedrock.
- Your cursor will automatically be confined to the Minecraft window when it's focused.
- The program runs in the background with a console window showing status updates.

### Hotkeys
- **Configurable Key** (default: `E`) - Recenter cursor to middle of window, intended for your in-game inventory keybind.
- **Escape** - Also recenters cursor, such as when opening a pause menu.
- **Ctrl+Shift+C** - Toggle cursor clipping on/off.

### Configuration
The program will create a `config.txt` file. You can edit this file to change and save the recenter key:
- Open `config.txt`
- Replace the letter with any key from A-Z or 0-9.
- Save and restart the SwimMouseCursor program.

Example `config.txt`:
```
E
```

## 🔧 Troubleshooting

### Windows Defender or Antivirus Blocking

If Windows Defender or your antivirus software blocks the program:

1. **Windows Defender SmartScreen:**
   - Click "More info" when the warning appears
   - Click "Run anyway"
   
2. **Antivirus Software:**
   - Add an exception for the program in your antivirus settings.
   - The program uses low-level keyboard hooks and mouse cursor manipulation, which can trigger false positives.

**Why does this happen?** The program uses Windows API hooks to monitor keyboard input and control the cursor, which are techniques sometimes used by malware. This is a false positive - the source code is available for review.

### Program Not Working / Not Clipping Cursor

**Solution:** Run the program as Administrator
- Right-click on `SwimMouseCursor.exe`
- Select "Run as administrator"
- This gives the program the necessary permissions to hook into system-level events.

### Runtime Error / Program Won't Start

If you get an error like "The code execution cannot proceed because MSVCP140.dll was not found" or similar:

**Solution:** Install Microsoft Visual C++ Redistributable
1. Download from Microsoft: [VC++ Redistributable Latest](https://aka.ms/vs/17/release/vc_redist.x64.exe)
2. Run the installer
3. Restart your computer
4. Try running the program again

### Cursor Still Escaping

- Make sure the program is running (check for the console window)
- Verify Minecraft Bedrock is the focused window
- Check that clipping is enabled (should say "ENABLED" in console)
- Try pressing the recenter hotkey (default: E)
- If all else fails, press `Ctrl+Shift+C` to toggle clipping off and on again

## 🎯 Features

- ✅ Automatic cursor clipping when Minecraft is focused
- ✅ Works in fullscreen AND windowed modes
- ✅ Non-intrusive hotkey system (doesn't consume keypresses)
- ✅ Configurable recenter key
- ✅ Safety toggle to disable clipping
- ✅ Minimal CPU usage/overhead
- ✅ Clean console interface with status updates

## 💬 Support

Join our Discord: [discord.gg/swim](https://discord.gg/swim)

Play our MCPE Server: **swimgg.club**

## 📝 Credits

Created by Swedeachu, aka Swimfan72

## ⚠️ Notes

- This program is designed specifically for Minecraft Bedrock Edition (Windows 10/11).
- The program must remain running in the background while you play.
- Close the program or use `Ctrl+Shift+C` to release the cursor when done playing.
