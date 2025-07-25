# AutoStartDisabler

A simple Windows tool to automatically deactivate all auto-start programs for all users.

## Features

- Removes all program shortcuts from Startup folders (user and system-wide)
- Deletes all auto-start registry entries (Current User and Local Machine)
- Compatible with **Windows 10** and **Windows 11**
- Console application for easy use and auditing

## How to Use

1. **Build the application:**
   - Open `AutoStartDisabler.cs` in Visual Studio or VS Code.
   - Target `.NET 6` or later for best compatibility.
   - Build the project.

2. **Run the application:**
   - Right-click the executable and select **Run as administrator** for full effect (required to remove system-wide startup entries).
   - The app will display what it removes.
   - After completion, restart your computer.

## What does this program do?

- Deletes all files (shortcuts, scripts, etc.) from:
  - Your user Startup folder
  - The common (all users) Startup folder
- Removes all entries from:
  - `HKCU\Software\Microsoft\Windows\CurrentVersion\Run`
  - `HKLM\Software\Microsoft\Windows\CurrentVersion\Run` (requires admin rights)

## Why do I need to run as Administrator?

- To remove auto-start entries for all users, including system services, administrator rights are required.
- Running without admin rights will only affect your personal startup programs.

## Safety Notes

- This app **removes all auto-start programs**. Do not use on machines where you want to keep some startup programs enabled!
- Back up important registry settings or shortcuts before running, if needed.
- Use at your own risk.

## License

MIT License. See [LICENSE](LICENSE) for details.
