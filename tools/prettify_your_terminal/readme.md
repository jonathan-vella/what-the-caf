# How to prettify Windows Terminal with oh-my-posh



Install the latest version of Windows Terminal from the Store
Install oh-my-posh from the store
Create a new profile by typing; notepad $PROFILE
Add the following two lines:

```
oh-my-posh init pwsh | Invoke-Expression
oh-my-posh init pwsh --config ~/.paradox.omp.json | Invoke-Expression
```

Save and exit
Reload the profile by typing: $PROFILE



> Notes:
> paradox.omp.json is my theme name
> This theme uses Nerd Fonts.  You can install Nerd Fonts from the cmd line with  'oh-my-posh font install' or manually from https://www.nerdfonts.com/
> You need to configure your Terminal to use the required font e.g. CaskaydiaCove Nerd Font
> Themes are saved in '%userprofile%\AppData\Local\Programs\oh-my-posh\themes'



Happy prettifying!




