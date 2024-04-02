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

3. In the Run Box, type cmd and then click ok.
4. Type the following below to display the computer name of your system (It should
   match your first name)
5. Type the following below, replacing my name with your First Name and Last Name.
   (No Spaces). This adds an account to your Windows operating system.
6. Right click on the start button and select Event Viewer.
7. After the Event Viewer opens, click Windows logs, and then click the Security log. We will be looking
   for events that fall under the category of User Account Management. Double Click on an User Account Management Event (In my case 4720)
   and then look for your first and last name. Click on the details tab. Make sure that the Date and Time
   stamp, provided with the Event Viewer views, is displayed in your screenshot.
   Event Viewer.
8. Switch back to the Command Prompt. Type the following command to enumerate all of the running
   services on Windows.
     - Quick Tip: Sometime hackers may stop services that interfere with their mischief, like Windows Update, the Firewall, or
       Antivirus. When they do stop a service, that action will be logged in the Windows event Viewer. This is a reason a
       Computer Forensic examiner might sift through the Event Viewer Logs.

9. Type the following command to stop the chosen Service on Windows. net stop "name of service"
10. Click back on the Windows Sever and go back into the Event Viewer. Click Windows logs, and then click
   the Application log. We will be looking for events that fall under the source of the previously chosen program for step 8.
   Double Click on the Event and then look for the Codemeter Runtime Server Service stopping.
11. Type the following command to stop the Windows Update Service on Windows. net stop "Windows Update"
12. Click back on the Windows Sever and go back into the Event Viewer. Click Windows logs, and then click
    the System log. We will be looking for events that fall under the category of Service Control Manager.
    Double Click on the Events and then look for the Windows Update Medic Service stopping.

### Congrats on completing a simple Event Log home lab! This is a small step into the field of digital forensics and log analysis and I encourage everyone to mess around and discover more about your own systems utlizing the Event Viewer:)  


