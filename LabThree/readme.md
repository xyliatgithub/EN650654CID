# Lab 3 - Firewall

In this lab, you will study the firewall and its logs in Linux systems using a SEED lab module.


## Lab Instructions 
Please complete the lab tasks of 2.1, 2.3, and 2.4 in Section 2 (2.2 is not required so you only need to use UFW). of the Firewall.pdf file. You also need to finish the additional tasks described below.


### Additional Tasks
•	Please implement a UFW rule to block any incoming SSH requests to the server (wherever the UFW firewall resides).
•	Please describe the record format in the log file that UFW creates on the server. You should explain all the general data fields. Please include two example records generated by different rules. Note: the UFW log file may not appear at first, so you may have to invoke UFW rules to create this file. Also, raise the level of logging to "high" if UFW  log file doesn't show your logs.
•	Provide a small program coded in either python or c  to read the UFW logs, and raise an alert if three blocked SSH records within a minute are generated. The records are from the UFW rule that blocks SSH connections from anywhere to the server (as in the first additional task). 

**Something needs to be noticed whe you are working on this lab:**
- In this lab, you need to block a website. Many famous website use many IP addresses now. It might be too difficult to block these websites. However, you could just block a website with a static IP address, like www.syr.edu. 
- If you think your firewall settings are correct, but it still can not block the target website. This may be due to the principle of UFW. The matching of UFW rules is based on the order in which the rules appear, so once a rule is matched, the check stops. To fix this, you could edit /etc/ufw/before.rules file. Add your rule under "# End required lines". The rule should be look like "-A ufw-before-input -s <your vm's IP> -j DROP". Then, run the command "ufw reload".


## Report Submission
•	The lab is due on 3/20, Friday by 11:59 PM. 
•	You can work in a group up to two people. A list of current student email addresses is available in the Syllabus section for your reference.
•	Write a detailed report with adequate screenshots and explanations.
•	Each group can only submit one report. Please submit one PDF file.


## Grading 
•	Completeness (30 pts): All the steps as instructed in the lab manual must be included in the report with adequate evidence.
•	Presentation (20 pts): The report must be clear and correct in organization and writing with adequate explanation. 


## If You Need Help...
If there are any questions, feel free to send an email to Qingshan Zhang (qzhang68@jhu.edu).