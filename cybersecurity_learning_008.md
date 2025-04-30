Room Title: Windows Command Line
Difficulty: Easy
Time to Complete: 45 minutes
Skills Covered:

    Connecting through SSH
    Display System Information
    Network Commands
    File Management
    Task Management
    
🏛️ Key Concepts and Lessons Learned
🔹 Connecting to a Windows machine with SSH

     To connect to the target VM, issue the command ssh user@MACHINE_IP as user is the username in this case. Then enter the password.

🔹 Display System Information

    set, ver and systeminfo are commands where we can see system information as the Windows Version, Host Name, etc...
    
🔹 Network Commands

    You can check your network information using ipconfig. The terminal output below shows our IP address, subnet mask, and default gateway. You can use ipconfig /all for even more information.

    One common troubleshooting task is checking if the server can access a particular server on the Internet. The command syntax is ping target_name. 
    Inspired by ping-pong, we send a specific ICMP packet and listen for a response. If a response is received, we know that we can reach the target and that the target can reach us.

    Another valuable tool for troubleshooting is tracert, which stands for trace route. The command tracert target_name traces the network route traversed to reach the target. 
    Without getting into more details, it expects the routers on the path to notify us if they drop a packet because its time-to-live (TTL) has reached zero.

    One networking command worth knowing is nslookup. It looks up a host or domain and returns its IP address.

     A basic netstat command with no arguments will show you established connections.
    

🔹 File Management

    You can use cd without parameters to display the current drive and directory. It is the equivalent of asking the system, where am I?

    You can view the child directories using dir.
    Note that you can use the following options with dir:

    dir /a - Displays hidden and system files as well.
    dir /s - Displays files in the current directory and all subdirectories.

    You can type tree to visually represent the child directories and subdirectories.
    
    You can change to any directory by using the command cd target_directory; this is equivalent to double-clicking the target_directory on your desktop. Furthermore, you can use cd .. to go up one level.

    To create a directory, use mkdir directory_name; mkdir stands for make directory. To delete a directory, use rmdir directory_name; rmdir stands for remove directory.

    You are curious about the contents of a particular text file. You can easily view text files with the command type. This command will dump the contents of the text file on the screen; this is convenient for files that fit within your terminal window. 
    You might want to consider 'more' for longer text files. 

    You can move files using the move command. 

    Delete a file using del or erase.

🔹 Task Management

    We can list the running processes using tasklist.

    Some filtering is helpful because the output is expected to be very long. You can check all available filters by displaying the help page using tasklist /?. 
    Let’s say that we want to search for tasks related to sshd.exe, we can do that with the command tasklist /FI "imagename eq sshd.exe".

    With the process ID (PID) known, we can terminate any task using taskkill /PID target_pid. For example, if we want to kill the process with PID 4567, we would issue the command taskkill /PID 4567.

🔍 Reflection

This room helped me to know some more about the Windows Line Commands, those commands will help to build a base for complex tasks in Windows.
