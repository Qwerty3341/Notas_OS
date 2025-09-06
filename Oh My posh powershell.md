Para abrir la configuración = Notepad $PROFILE

En el notepad colocar
```
Import-Module Terminal-Icons

oh-my-posh init pwsh --config "$env:POSH_THEMES_PATH\jandedobbeleer.omp.json" | Invoke-Expression

Set-PSReadLineOption -PredictionViewStyle ListView
```
