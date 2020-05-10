# TA_Sigma_Searches
A Splunk app that contains rules from [Florian Roth](https://twitter.com/Cyb3rOps)'s [Sigma](https://github.com/Neo23x0/sigma) converted to Splunk searches with inspiration from [TA-Sigma-Searches](https://github.com/dstaulcu/TA-Sigma-Searches).
* Up to date with Sigma commit: fd7968d4f846d2e39d4af2b08afd63078ce0ea2d

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
