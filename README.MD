# PowerShell Super Config (Windows 11)

![Example](https://i.imgur.com/KM9z6cH.png)

1. Make sure the .NET Core version of PowerShell is installed (find in Microsoft Store). Once installed, open it in Terminal 

2. Find your powershell profile directory
   
   ```powershell
   echo $PROFILE
   ```

3. Open the folder
   
   ```powershell
   start "C:/PowerShellDirectory"
   ```

4. Remove all contents, then clone (or copy) all contents from this repo, including the Modules folder

5.  Install the font found here: [Caskaydia Cove Nerd Font](https://github.com/ryanoasis/nerd-fonts/releases/download/v2.1.0/CascadiaCode.zip). Once downloaded, drag/drop them into the C:\Windows\Fonts to install. 

6. Change the font in Terminal to "Caskaydia Cove NF", as well as in Visual Studio Code (so you can use this profile in the terminal emulator)

7. Install the ohmypsoh module. Support is found [here](https://ohmyposh.dev/docs/windows)
   
   ```powershell
    winget install JanDeDobbeleer.OhMyPosh
   ```

8. Change the OhMyPosh settings by opening **Microsoft.PowerShell_profile.ps1** and changing the config path on the second line to the json file included in **PowerShell/PoshSettings**.

    Example:
    ```powershell
    oh-my-posh --init --shell pwsh --config "C:\Powershell\PoshSettings\ohmyposhv3-v2.json" | Invoke-Expression
    ```

9.  Install the terminal icons (support [here](https://www.hanselman.com/blog/take-your-windows-terminal-and-powershell-to-the-next-level-with-terminal-icons)).

    ```powershell
    Install-Module -Name Terminal-Icons -Repository PSGallery
    ```

10. Install the ```"z"``` module (Support [here](https://www.powershellgallery.com/packages/z/1.1.13)). This lets you quickly navigate the powershell based on history by pressing tab to cycle through directories. It replaces the ```"cd"``` prompt

    ```powershell
    Install-Module z -AllowClobber
    ```

11. Finally, install the PSReadLine module (support [here](https://github.com/PowerShell/PSReadLine)). This module shows predictions based on your clipboard and history.

    ```powershell
    Install-Module -Name PSReadLine
    ```