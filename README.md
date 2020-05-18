# TA_Sigma_Searches
A Splunk app that contains rules from [Florian Roth](https://twitter.com/Cyb3rOps)'s [Sigma](https://github.com/Neo23x0/sigma) converted to Splunk searches with inspiration from [TA-Sigma-Searches](https://github.com/dstaulcu/TA-Sigma-Searches).
* Up-to-date as of 5-18-20 with Sigma commit: 5d1605bba23d4844f19fe3053508c395f13a90bc

### Currently includes the rules from: sigma/rules/windows/
* builtin
* powershell
* process_creation
* sysmon

### Search Naming Convention -> $SigmaTitle - source
* Examples:
    * builtin
        * Security Eventlog Cleared - builtin
    * powershell
        * Alternate PowerShell Hosts - powershell
    * process_creation
        * Application Whitelisting Bypass via Bginfo - winevent
        * Application Whitelisting Bypass via Bginfo - sysmon
    * sysmon
        * Executable in ADS - sysmon

### Can access the searches from 'Reports' within the app
* default time of -24 hours
### OR 
### via a savedsearch:
```
| savedsearch "Security Eventlog Cleared - builtin"
```
