# Begginer-Log-Analysis-Lab
This will be a beginner level lab focusing on analyzing logs found in Windows Event viewer. To follow along no paid services will be required, such as Splunk or other parsing tools.

# As a disclaimer, it is highly recomended that this and any other labs, be conducted on a Virtual Machine with a known good backup as we will be stopping certain startup tasks and utilizing the command prompt!

# Windows-Log-Analysis

## Objective

The Log Analysis Lab project aimed to allow individuals the opportunity to become more familiar with one of the most important tools related to Windows, Event Viewer. This lab is designed to be conducted in a safe at home environment and to be accessable to anyone with a Windows 10/11 operating system. The primary focus is to become familiar with the Event Viewer tool, attain a better understanding of the importance of Logs, and become accustomed to the Guided User Interface(GUI) of the tool. This hands on experience was designed to introduce a basic understanding of network security, digital forensic analysis, and detection measures. 

### Skills Learned

- Basic understanding of Log analysis concepts and practical application.
- Proficiency in analyzing and interpreting user/network logs.
- Ability to utilize the GUI of the Event Viewer Tool.
- Enhanced knowledge of cmd terminal and security vulnerabilities.
- Development of critical thinking and problem-solving skills in cybersecurity.

### Tools Used


- Event Viewer for log viewing and analysis.
- Command Line for creating and analyzing system functions.

## Steps
1. Right Click on the start button and select Run
   
   ![1 Run](https://github.com/Lantern76/Log-Analysis-Lab/assets/119342094/996f6ca0-1e47-46ae-8d89-ef7005714298)

2. In the Run Box, type cmd and then click ok.
   
   ![2 cmd](https://github.com/Lantern76/Log-Analysis-Lab/assets/119342094/45c95b7a-6688-4641-8f93-45db8cd07c56)

3. Type the following below to display the computer name of your system (It should
   match user name currently logged into the system). In my case it is my first name, Ryan.
   
   ![hostname](https://github.com/Lantern76/Log-Analysis-Lab/assets/119342094/c1b8e9fc-5516-4673-9124-bbe33e89a21a)

4. Type the following below, replacing my name with your First Name and Last Name.
   (No Spaces). This adds an account to your Windows operating system.
   
   ![2 - NetUser](https://github.com/Lantern76/Log-Analysis-Lab/assets/119342094/4b0457bd-6e6d-4f8f-b30e-7aecfd0697b4)

5. Right click on the start button and select Event Viewer.
    
    ![3 Event Viewer](https://github.com/Lantern76/Log-Analysis-Lab/assets/119342094/44c5d254-d836-4fe1-9db3-57f46fd44215)

6. After the Event Viewer opens, click Windows logs, and then click the Security log. We will be looking
   for events that fall under the category of User Account Management. Double Click on an User Account Management Event (In my case 4720)
   and then look for your first and last name. Click on the details tab.

    ![1 - User Account Creation ](https://github.com/Lantern76/Log-Analysis-Lab/assets/119342094/1fc2abca-5399-4ace-9bcc-0d023133d06d)

7. Switch back to the Command Prompt. Type the following command to enumerate all of the running
   services on Windows. net start
     - Quick Tip: Sometime hackers may stop services that interfere with their mischief, like Windows Update, the Firewall, or
       Antivirus. When they do stop a service, that action will be logged in the Windows event Viewer. This is a reason a
       Computer Forensic examiner might sift through the Event Viewer Logs.

       ![4 Net Start](https://github.com/Lantern76/Log-Analysis-Lab/assets/119342094/ed968149-3462-4b33-8839-abf6106bb499)


8. Type the following command to stop the chosen Service on Windows. net stop "name of service"(In my case it is the CodeMeter service)
    
    ![5 net stop](https://github.com/Lantern76/Log-Analysis-Lab/assets/119342094/1e9b9aab-0d5e-44b4-bf3b-21a8a7f70608)

9. Click back on the Windows Sever and go back into the Event Viewer. Click Windows logs, and then click
   the Application log. We will be looking for events that fall under the source of the previously chosen program for step 8.
   Double Click on the Event and then look for the previously chosen program "Service stopping" indicator(a message under the general tab of log).

![Code Meter Stop running](https://github.com/Lantern76/Log-Analysis-Lab/assets/119342094/622e02dd-b3db-4676-9532-ddda4fa78b46)

10. Type the following command to stop the Windows Update Service on Windows. net stop "Windows Update"
    
    ![6 net stop windows update](https://github.com/Lantern76/Log-Analysis-Lab/assets/119342094/7481b8f9-d75a-4f83-8f1d-e90723ce78f7)

11. Click back on the Windows Sever and go back into the Event Viewer. Click Windows logs, and then click
    the System log. We will be looking for events that fall under the category of Service Control Manager.
    Double Click on the Events and then look for the Windows Update Medic Service stopping.
    
    ![Windows Stop Update](https://github.com/Lantern76/Log-Analysis-Lab/assets/119342094/ec3b3d4e-42cb-4da2-b564-bea669b125f4)


### Congrats on completing a simple Event Log home lab! This is a small step into the field of digital forensics and log analysis and I encourage everyone to mess around and discover more about your own systems utlizing the Event Viewer:)  


