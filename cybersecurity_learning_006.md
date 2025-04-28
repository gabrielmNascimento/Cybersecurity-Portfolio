Room Title: Windows Fundamentals 3
Difficulty: Easy
Time to Complete: 30 minutes
Skills Covered:

    Windows Update
    Windows Security
    Microsoft Defender
    Firewall
    Microsoft Defender SmartScreen
    BitLocker
    Volume Shadow Copy Service
    
🏛️ Key Concepts and Lessons Learned
🔹 Windows Updates

    Windows Update is a service provided by Microsoft to provide security updates, feature enhancements, and patches for the Windows operating system and other Microsoft products, such as Microsoft Defender. Updates are typically released on the 2nd Tuesday of each month. This day is called Patch Tuesday. That doesn't necessarily mean that a critical update/patch has to wait for the next Patch Tuesday to be released. If the update is urgent, then Microsoft will push the update via the Windows Update service to the Windows devices.

🔹 Windows Defender

    Manage settings 

    Real-time protection - Locates and stops malware from installing or running on your device.
    Cloud-delivered protection - Provides increased and faster protection with access to the latest protection data in the cloud.
    Automatic sample submission - Send sample files to Microsoft to help protect you and others from potential threats. 
    Controlled folder access - Protect files, folders, and memory areas on your device from unauthorized changes by unfriendly applications.
    Exclusions - Windows Defender Antivirus won't scan items that you've excluded.
    Notifications - Windows Defender Antivirus will send notifications with critical information about the health and security of your device. 

    Warning: Excluded items could contain threats that make your device vulnerable. Only use this option if you are 100% sure of what you are doing. 

    Virus & threat protection updates

    Check for updates - Manually check for updates to update Windows Defender Antivirus definitions.  

    Ransomware protection

    Controlled folder access - Ransomware protection requires this feature to be enabled, which in turn requires Real-time protection to be enabled.

    
🔹 Windows Firewall

    Per Microsoft, "Windows Firewall offers three firewall profiles: domain, private and public".

    Domain - The domain profile applies to networks where the host system can authenticate to a domain controller. 
    Private - The private profile is a user-assigned profile and is used to designate private or home networks.
    Public - The default profile is the public profile, used to designate public networks such as Wi-Fi hotspots at coffee shops, airports, and other locations.

🔹 BitLocker

    Per Microsoft, "BitLocker Drive Encryption is a data protection feature that integrates with the operating system and addresses the threats of data theft or exposure from lost, stolen, or inappropriately decommissioned computers".
    On devices with TPM installed, BitLocker offers the best protection.

    Per Microsoft, "BitLocker provides the most protection when used with a Trusted Platform Module (TPM) version 1.2 or later. The TPM is a hardware component installed in many newer computers by the computer manufacturers. It works with BitLocker to help protect user data and to ensure that a computer has not been tampered with while the system was offline".

🔹 Volume Shadow Copy Service

    If VSS is enabled (System Protection turned on), you can perform the following tasks from within advanced system settings. 

    Create a restore point
    Perform system restore
    Configure restore settings
    Delete restore points

    From a security perspective, malware writers know of this Windows feature and write code in their malware to look for these files and delete them. Doing so makes it impossible to recover from a ransomware attack unless you have an offline/off-site backup.
    
🔍 Reflection

This room helped me to know some more about the management resources in a Windows environment.
