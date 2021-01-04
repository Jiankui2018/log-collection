# SharePoint ULS Log

## Do not merge

1. Update the windows hosts file(c:\Windows\System32\Drivers\etc\hosts) to redirect the client's request to the specified SharePoint server if you have more than one Web front end servers.
2. Log on the SharePoint server as administrator and run PowerShell in the elevated mode.
    - Add-PSSnapin Microsoft.SharePoint.PowerShell -EA 0
3. Enable verbose logging level and create a new log file starting from now.
    - Set-SPLogLevel -TraceSeverity VerboseEX
    - New-SPLogFile
4. Reproduce the issue
5. End current log file and restore the logging level to default.
    - New-SPLogFile
    - Clear-SPLogLevel
6. Find the log, it should cover the time range when the issue happened.
    - The format of the file name: `<SERVER_NAME>-<DATE>-<StartTimeOfLog>.log`
    - Get the log directory via the following PowerShell command:
        - Get-SPDiagnosticConfig | select LogLocation
        
## Do not merge(Together with Client Request using Browser Develop Tool)

1. Update the windows hosts file(c:\Windows\System32\Drivers\etc\hosts) to redirect the client's request to the specified SharePoint server if you have more than one Web front end servers.
2. Log on the SharePoint server as administrator and run PowerShell in the elevated mode.
    - Add-PSSnapin Microsoft.SharePoint.PowerShell -EA 0
3. Enable verbose logging level and create a new log file starting from now.
    - Set-SPLogLevel -TraceSeverity VerboseEX
    - New-SPLogFile
4. Take Edge/Chrome as example, press **CTRL+SHIFT+I** to open develop tool in the browser, switch to the **Network** tab, tick **Preserve log** and **Disable cache**.
5. Reproduce the issue, network activities should be recored in the develop tool pannel. 
5. End current log file and restore the logging level to default.
    - New-SPLogFile
    - Clear-SPLogLevel
6. Find the log, it should cover the time range when the issue happened.
    - The format of the file name: `<SERVER_NAME>-<DATE>-<StartTimeOfLog>.log`
    - Get the log directory via the following PowerShell command:
        - Get-SPDiagnosticConfig | select LogLocation
7. Go to the network pannel in the browser develop tool, right click any network activity and click **Save all as HAR with content** to save and then close the develop tool.
8. Provide the *.log file and *.har file.
