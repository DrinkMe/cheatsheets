
# get windows defender settings
Get-MpPreference
```

### exclude directory from real-time and scheduled scanning
```
Set-MpPreference -ExclusionPath <path>
```

### disable real-time protection
```
Set-MpPreference -DisableRealtimeMonitoring $true
```

### disable defender
```
Set-MpPreference -DisableIntrusionPreventionSystem $true -DisableIOAVProtection $true -DisableRealtimeMonitoring $true -DisableScriptScanning $true -EnableControlledFolderAccess Disabled -EnableNetworkProtection AuditMode -Force -MAPSReporting Disabled -SubmitSamplesConsent NeverSend
```

