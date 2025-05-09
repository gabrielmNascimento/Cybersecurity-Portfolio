Room Title: Moniker Link (CVE-2024-21413)
Difficulty: Easy
Time to Complete: 30 minutes
Skills Covered:

    Main components of Metasploit
    Msfconsole
    Working with modules
    
🏛️ Key Concepts and Lessons Learned
🔹 Main components of Metasploit

    Exploit: A piece of code that uses a vulnerability present on the target system.
    Vulnerability: A design, coding, or logic flaw affecting the target system. The exploitation of a vulnerability can result in disclosing confidential information or allowing the attacker to execute code on the target system.
    Payload: An exploit will take advantage of a vulnerability. However, if we want the exploit to have the result we want (gaining access to the target system, read confidential information, etc.), we need to use a payload. 
    Payloads are the code that will run on the target system.

    ![image](https://github.com/user-attachments/assets/ef96bb9c-80cf-404d-b643-7b433dc7f316)

    ![image](https://github.com/user-attachments/assets/eae14963-ff2a-48e5-b74f-6fd950eb3615)

    ![image](https://github.com/user-attachments/assets/dc457845-d716-47c9-8741-1353ac838f47)

    ![image](https://github.com/user-attachments/assets/de6b9691-f1ab-449c-9cee-b1b7b44bd27a)

    ![image](https://github.com/user-attachments/assets/dc79f8fb-6fa6-4046-b32d-193efa02bdbe)

    ![image](https://github.com/user-attachments/assets/9f194936-0f0e-4b9b-bd9c-532f103c8bed)

🔹 Msfconsole

    ![image](https://github.com/user-attachments/assets/14b573c0-d077-4395-a4f5-1752cedde061)

    ![image](https://github.com/user-attachments/assets/bab7cc6d-7f5b-46a7-8e3a-2f1a9485152c)

    ![image](https://github.com/user-attachments/assets/6c9f7fab-92af-4458-845d-eed8be1198b5)

    ![image](https://github.com/user-attachments/assets/b80a4e43-1c44-4412-bc1b-9dbac1f64a65)
    
🔹 Working with modules

    ![image](https://github.com/user-attachments/assets/a65ba9f8-c3a7-48bd-99b1-408d067e641b)

     You can override any set parameter using the set command again with a different value. You can also clear any parameter value using the unset command or clear all set parameters with the unset all command. 

     You can use the setg command to set values that will be used for all modules. The setg command is used like the set command. 
     The difference is that if you use the set command to set a value using a module and you switch to another module, you will need to set the value again. 
     The setg command allows you to set the value so it can be used by default across different modules. You can clear any value set with setg using unsetg.

     Once all module parameters are set, you can launch the module using the exploit command. 
     Metasploit also supports the run command, which is an alias created for the exploit command as the word exploit did not make sense when using modules that were not exploits (port scanners, vulnerability scanners, etc.).
     The exploit command can be used without any parameters or using the “-z” parameter.  The exploit -z command will run the exploit and background the session as soon as it opens.

🔍 Reflection

This room helped me to know some more about the Metasploit tool and be able to study more about vulnerabilities.
