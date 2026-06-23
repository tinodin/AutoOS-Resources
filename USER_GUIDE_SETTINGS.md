# 📘 AutoOS Settings User Guide

<details>
<summary>What <b>NOT</b> to do on AutoOS, click to expand</summary>
<br/>

- Run any other `tweaks` or `optimizers` for obvious reasons.
- Use `timer resolution` or `memory cleaners` because they do more harm than good.
- Use `external frame rate limiters` like `NVCP` or `RTSS` because they trade `better 1% lows` for `added latency` (unless non-competitive).
- Set `visual effects` to `Best Performance`.
- Disable `animations`, `transparency` or `paging file`.
- `Uninstall` `MSI Afterburner, OBS, Everything, Windhawk, StartAllBack` or any of the `runtimes`.
- `Install` `7-Zip` or `WinRAR` because `NanaZip` is already installed.
- `Uninstall` more AppX Packages like `Xbox Game Bar` or `Microsoft Edge` because it **breaks functionality**.

</details>

---

<details>
<summary>If you want to merge the space of your old Windows partition with the AutoOS partition, click to expand</summary>
<br/>

**Step 1:**
- Copy your Games to the same path but on the AutoOS partition.
- Open all the manifest files from the game launchers, then use `Ctrl + H` to replace the drive letters, click `Replace All` and save the file.
  - Epic Games
    - `C:\ProgramData\Epic\UnrealEngineLauncher\LauncherInstalled.dat`
    - `C:\ProgramData\Epic\EpicGamesLauncher\Data\Manifests`
    - `C:\ProgramData\Epic\EpicOnlineServicesShared\InstallHelper\InstalledItems`
  - Riot Games
    - `C:\ProgramData\Riot Games\Metadata\<your game>\<your game>.live.product_settings.yaml`
  - Steam
    - `C:\Program Files (x86)\Steam\steamapps\libraryfolders.vdf`

**Step 2:**
- Install `Minitool Partition Wizard` from the `Applications` tab.
- Right click on the `old Windows partition` and select `Delete`.
- Right click on the `AutoOS partition` and select `Extend`, select the `old Windows partition` and `max out the slider`.
- Click `Apply` and then `Restart Now`.

  ---

  <details>
  <summary>If you are on an <b>ASUS Motherboard</b> and get <b>GPT header corruption has been detected</b> message, click to expand</summary>
  <br/>

  - Press `F1` to get into `BIOS`.
  - Press `F7` to get into `advanced mode`.
  - Go to `Boot` tab, then select `Boot Configuration`.
  - Change `Next Boot Recovery Action` to `Recovery`.
  - Change `Boot Sector (MBR/GPT) Recovery Policy` to `Auto Recovery` if it exists.

  </details>

  ---

  <details>
  <summary>If the <b>old Windows entry</b> is still <b>showing up</b> on boot, click to expand</summary>
  <br/>

  - Open Command Prompt and paste:
  ```
  bcdedit /enum
  ```

  - Find the entry of your old Windows partition, copy its `identifier` value and then run:

  ```
  bcdedit /delete {identifier}
  ```
  </details>
</details>

---

### Home
Quick access for links:
- Open AutoOS User Guide
- Open AutoOS Contribution Guide
- Join AutoOS Discord Server
- Donate

![Home](https://raw.githubusercontent.com/tinodin/AutoOS-Resources/main/AutoOS%20Settings/Home.png)

### Sound
Adjust Volume, Format and Buffer Size of your current input and output device:
- If your audio output device supports a lower `buffer size`, you can lower it in exchange for `higher CPU usage`.

![Sound](https://raw.githubusercontent.com/tinodin/AutoOS-Resources/main/AutoOS%20Settings/Sound.png)

### Displays
Manually adjust or import a Custom Resolution Utility (CRU) profile:
- CRU Guide coming soon...

![Displays](https://raw.githubusercontent.com/tinodin/AutoOS-Resources/main/AutoOS%20Settings/Displays.png)

### Graphics Cards
Select your Graphics Card preferences:
- Click `Update` if available, which updates your GPU driver while keeping your current settings.
- Enable `High-Bandwidth Digital Content Protection (HDCP)` if you watch `DRM protected content` like `Netflix` etc.
- Disable `High-Definition Multimedia Interface (HDMI)/DisplayPort (DP) Audio` if you don't use headphones or speakers connected to your monitor or audio receiver.
- Manually adjust or import an `MSI Afterburner Profile`.
- Enable the `OBS Studio` toggle if you want to have `clips` (`30sec`, `Alt + F10`).

![Graphics Cards](https://raw.githubusercontent.com/tinodin/AutoOS-Resources/main/AutoOS%20Settings/Graphics%20Cards.png)
![Graphics Cards2](https://raw.githubusercontent.com/tinodin/AutoOS-Resources/main/AutoOS%20Settings/Graphics%20Cards2.png)

### Per-CPU Scheduling
Manually adjust or automatically optimize Audio, GPU, XHCI and NIC Affinities:
- Click `Optimize Affinities` to reapply Affinities to all devices after `manual driver reinstalls` or after toggling `Hyper-Threading` / `SMT`.

![Per-CPU Scheduling](https://raw.githubusercontent.com/tinodin/AutoOS-Resources/main/AutoOS%20Settings/Per-CPU%20Scheduling.png)
![Per-CPU Scheduling2](https://raw.githubusercontent.com/tinodin/AutoOS-Resources/main/AutoOS%20Settings/Per-CPU%20Scheduling2.png)

### Bluetooth & Devices
Toggle Bluetooth Services & Drivers and XHCI Interrupt Moderation (IMOD) per controller:
- Keep XHCI Interrupt Moderation (IMOD) disabled for all USB controllers.

![Bluetooth & Devices](https://raw.githubusercontent.com/tinodin/AutoOS-Resources/main/AutoOS%20Settings/Bluetooth%20&%20Devices.png)

### Network & Internet
Manually adjust or automatically optimize advanced network adapter settings:
- Click `Optimize Adapter` to reapply settings after `driver reinstalls`.

![Network & Internet](https://raw.githubusercontent.com/tinodin/AutoOS-Resources/main/AutoOS%20Settings/Network%20&%20Internet.png)

### Energy & Power
Adjust, Edit, Duplicate, Delete, Restore, Export, Import Power plans and compare them:
- Keep using the AutoOS Power Plan.
- If you have issues with the AutoOS Power Plan, leave a message on the [Discord Server](https://discord.gg/bZU4dMMWpg).
- Select another power plan in the 2nd combobox to `compare` it to the active power plan.
- Right click on the active power plan combobox to `Edit, Duplicate, Delete or Export` it.

![Energy & Power](https://raw.githubusercontent.com/tinodin/AutoOS-Resources/main/AutoOS%20Settings/Energy%20&%20Power.png)
![Energy & Power2](https://raw.githubusercontent.com/tinodin/AutoOS-Resources/main/AutoOS%20Settings/Energy%20&%20Power2.png)

### Services & Drivers
Toggle Services & Drivers states with configured functionality:
- `Enable` the `WiFi Support` checkbox if you are using `WiFi while Gaming`.
- `Enable` the `Bluetooth Support` checkbox if you are using `Bluetooth while Gaming`.
- `Disable` the `toggle` at the top and restart whenever you are `Gaming` competitively.
- `Enable` it again and restart if you need `functionality` for `Work` or installing applications / drivers.

![Services & Drivers](https://raw.githubusercontent.com/tinodin/AutoOS-Resources/main/AutoOS%20Settings/Services%20&%20Drivers.png)

### BIOS Settings
Manually adjust or merge recommended BIOS Settings:
- In the `Recommended Changes` field click `Merge` and `Import to NVRAM` on the top right, then restart your PC.

  **If no internet:**
  - Enable the `toggle` in the `Services & Drivers` tab and restart your PC.
  - Click `Optimize` in the `Per-CPU Scheduling` and in the `Network & Internet` tab.

  **If not booting:**
  - Reset CMOS using the `button` on your `motherboard` (if yours has one) or by `removing the CMOS battery` for 5 minutes.
  - After that, `lower the amount` to merge using the `numberbox` on the left until you `find the setting` that causes your PC to not boot.
  - Once you find the setting, please leave a message on the [Discord Server](https://discord.gg/bZU4dMMWpg).

  **If crashing, freezing or worse performance:**
  - Option 1 (Easier): Click `Restore from Backup` and select the oldest or previous `nvram.txt`.
  - Option 2 (Harder):
    - **Intel:**
      - Lower `Max Turbo Ratios`
      - Enable `Hyper-Threading`
      - Disable `E-Cores` (Active E-Cores, Active Efficient Cores, Active Efficient-cores, No. of CPU E-Cores Enabled)
    - **AMD:**
      - Lower `All Core Curve Optimizer Magnitude`

![BIOS Settings](https://raw.githubusercontent.com/tinodin/AutoOS-Resources/main/AutoOS%20Settings/BIOS%20Settings.png)

### Disk Cleanup
Clean up your drives:
- Click `Clean up disks` to run disk cleanup to free up some space.

![Disk Cleanup](https://raw.githubusercontent.com/tinodin/AutoOS-Resources/main/AutoOS%20Settings/Disk%20Cleanup.png)

### Windows Security
Toggle Windows Security Options:
- Enable `HVCI` if you play `Valorant`.
- Enable `HVCI` and `VBS` if you play `FACEIT`.

![Windows Security](https://raw.githubusercontent.com/tinodin/AutoOS-Resources/main/AutoOS%20Settings/Windows%20Security.png)

### Windows Update
Toggle Windows Updates and set target version:
- Enable `Windows Updates` to get the `latest features` and `security updates`.
- All `optimizations will be kept`.
- `Drivers` are `excluded by default`.

![Windows Update](https://raw.githubusercontent.com/tinodin/AutoOS-Resources/main/AutoOS%20Settings/Windows%20Update.png)

### Browsers
Post-install your Browsers and Browser Extensions:
- Use `Thorium` or `Helium` over `Chrome`.
- Use `Zen` for best `productivity` and `design`.
- Use `uBlock Origin` and other extensions like in `my selection`.

![Browsers](https://raw.githubusercontent.com/tinodin/AutoOS-Resources/main/AutoOS%20Settings/Browsers.png)

### Applications
Post-install your Applications:
- Select `Discord`, which comes `preconfigured` with `Vencord`, `OpenAsar` and `all settings`.
- Use `Logitech Onboard Memory Manager` over `Logitech G HUB` if you have a `Logitech Mouse`.

![Applications](https://raw.githubusercontent.com/tinodin/AutoOS-Resources/main/AutoOS%20Settings/Applications.png)
![Applications2](https://raw.githubusercontent.com/tinodin/AutoOS-Resources/main/AutoOS%20Settings/Applications2.png)

### Games
View your Game Library (Supports Epic Games, Riot Games, EA, Ubisoft Connect, Steam, Eden, Citron and Ryujinx):
- Switch between Epic Games and Steam Accounts on the top right.
- Press the `Play` button to launch any Game.

  **If Services & Drivers toggle disabled:**
  - Once you are in the `Game`, press the `Stop Processes` button.
  - Use `Alt+Tab` to switch between apps in this state.
  - Press the `Restart Processes` button to restore the taskbar etc.

  **Adding Games:**
  - For `Riot Games` titles to show up in the `Games` tab, install them through the `Epic Games Launcher` as well.
  - For `EA` or `Ubisoft Connect` titles to show up in the `Games` tab, add them to your `Epic Games Launcher` library.
  - To add custom games, add the game as a `non-steam game` in `Steam`.
  - The name has to be the same as found on [IGDB](https://www.igdb.com/).

  **Notes:**
  - Cap your Game's `frame rate limit` to `a multiple` of your monitor's `refresh rate` (eg. 144hz -> 72/144/288fps).

![Games](https://raw.githubusercontent.com/tinodin/AutoOS-Resources/main/AutoOS%20Settings/Games.png)

### Settings
Configure AutoOS window and theme preferences:
- Enable `Hide AutoOS Startup` if you don't want to see the `AutoOS Startup`.
- Change `Material` to customize the window appearance.
- Select paths for `Switch Emulator data` to make them show up in the `Games` tab.

![Settings](https://raw.githubusercontent.com/tinodin/AutoOS-Resources/main/AutoOS%20Settings/Settings.png)