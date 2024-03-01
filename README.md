# BootCon-Project
My Final Project for my Cyber Security course focusing on the Automation and Reusability of tasks.

# General Consensus

The Cyber Security world is a broad ever-expanding sphere with a constantly evolving technologcial population overseeing it. The result is cyber defenders performing daily monitoring for ensuring secure networking and system hardening whilst the contrast of network infiltration and system compromise by bad actors, continues to become more complex and pervasive.

Whilst there are numerous tools (SIEMs, Packet Sniffers, Firewalls, Ethical Hacking tools etc.), methodologies (Detect and protect, Secure Access, Advanced Threat Prevention etc.), and practices (Defence in Depth, CIA Triad, Password Policy implementation etc.) for blue teams cyber defence approach, the one resource that persists to be the main valuable component required for monitoring cyber crime is time. There is a general cocnensus that Cyber Security teams have an abundance of tasks required to optimally secure a company or clients network and system, many of these rote tasks have become habitual for cyber defenders as they are an, although often mundaine, staple for ensuring system security.

# The Necessity of Automation

This brings to light the value of system automation and shows the nessecity for a form of task management and execution within a cyber teams defensive arsenal, that does not require extensive time labour. Whether it be for the present or not to distant future, applications like SOAR's (Security Orchestration Automation and Response), IaM's (Identity and access Management), XDR's (eXtended Detection and Response) etc. all play a vital role in ensuring cyber teams can focus on tasks that take priority, require extensive monitoring and enlist the biggest risk to the company.

# Goal of my Bootcon Project

My goal is to display a form of automation for packet capturing that highlights specific protocols and client request data, that can accuratley display an attempted attack. To acheive this I will be using the Network Packet Analyser Wireshark's command line console Tshark, in conjunction with Bash Scripting.

The Process to acheive my outlined objective, involved opening an attack machine terminal that would perform a cross-site scripting attack on the DVWA Domain. At the same time the defending machine will run the Bash Script allowing for Tshark to capture the data and write specific information to specified files. From here it will create 3 seperate files all containing different data pertaining to the files requirements.

- 1 File for general Network Logs.
- 1 Filefor isolating data that would pertain to an attempted cyber attack.
- 1 File for importing directly into Splunk for further analysis.

# Ways to Improve the Process

This could, in a non simulated environment, be further enhanced to be more efficient within a Linux OS Terminal through the use of cronjobs and allowing for the Script/Task to automate routinely without the cyber professionals orchestration for the majority of the process.
