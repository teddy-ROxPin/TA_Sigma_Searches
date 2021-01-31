# TA_Sigma_Searches
A Splunk app that contains [Florian Roth](https://twitter.com/Cyb3rOps)'s [Sigma](https://github.com/Neo23x0/sigma) rules converted to Splunk searches.
* Up-to-date as of 1-31-21 with Sigma commit: 6b9eef58da7ab74be2373562851fe32e59e0bbe5

Inspiration from [TA-Sigma-Searches](https://github.com/dstaulcu/TA-Sigma-Searches).
### Currently includes the rules from: sigma/rules/windows/
* builtin
* powershell
* process_creation
* sysmon

The rules that were previously in the 'sysmon' folder seem to have spread throughout the following new folders, though some still remain in 'sysmon':
* driver_load
* file_event
* image_load
* network_connection
* process_access
* registry_event

For now, I'm treating them as if they were still in the 'sysmon' folder so the search name will still have the postfix '- sysmon'

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
