The goal of the project is to demonstrate how Fail2ban protects a Linux server from Brute-Force SSH login attempt by automatically banning attacker’s IP addresses after repeated failures.

#  STEPS I PERFORMED
1.	I installed and enable Fail2ban in my kali Linux.

2.	I checked the SSHD jail state to make sure it was running. Everything showed 0 at first because there were no fail attempt yet.


3.	From my window command prompt, I tried to SSH into Kali using the wrong password 3 times.

4.	Fail2ban picked those failed login attempt and eventually banned my windows IP after I exceeded the retry limit.

5.	I confirmed the ban by checking the jail status again and, IP showed up in the banned IP list

6.	I also looked at the fail2ban.log.file, which showed the exact time my IP was banned 

7.	So to test further, I manually unbanned the IP using the Fail2ban-Client command

8.	Also, I noticed that when I later removed my IP from the banned list, the total banned and total failed counters kept their history. So restarting the service reset those counters back to 0



