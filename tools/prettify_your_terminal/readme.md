# How to prettify Windows Terminal with oh-my-posh

![Prettify Windows Terminal](/images/prettify_windows_terminal.jpg)


- Install the latest version of Windows Terminal from the Store
- Install oh-my-posh from the store
- Create a new profile by typing; notepad $PROFILE
- Add the following two lines:

```
# Start Oh My Posh CLI helper with paradox enabled
oh-my-posh init pwsh --config ~/.config/ohmyposh/paradox.omp.json | Invoke-Expression

# Add icons to `ls` and `dir` file lists
# Don't have it? Install using this command:
# Install-Module -Name Terminal-Icons -Repository PSGallery
Import-Module -Name Terminal-Icons

# Add auto complete (requires PSReadline 2.2.0-beta1+ prerelease)
# Don't have it? Install using this command:
# Install-Module -Name PSReadLine -AllowPrerelease -Scope CurrentUser -Force -SkipPublisherCheck
Set-PSReadLineOption -PredictionSource History
Set-PSReadLineOption -PredictionViewStyle ListView
Set-PSReadLineOption -EditMode Windows
```

- Save and exit
- Reload the profile by typing: $PROFILE



> Notes:
> - paradox.omp.json is my theme name
> - This theme uses Nerd Fonts.  You can install Nerd Fonts from the cmd line with  'oh-my-posh font install' or manually from https://www.nerdfonts.com/
> - You need to configure your Terminal to use the required font e.g. CaskaydiaCove Nerd Font
> - Themes are saved in '%userprofile%\AppData\Local\Programs\oh-my-posh\themes'

## Happy prettifying!




