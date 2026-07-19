# Troubleshoot Suspected DNS Issue

## Objective

This lab simulates a suspected DNS issue at a company. Multiple users are complaining that they are unable to access the new company website at `http://www.ips.com`. We gathered previous information, and have concluded that it can be a netwrok connectivity or DNS issue.

### Skills Learned

- Understanding of troubleshooting DNS issues
- Proficiency in writing DNS commands to resolve possible errors
- Enhanced knowledge of network protocols and security vulnerabilities.
- Development of critical thinking and problem-solving skills in connectivity issues.

### Tools Used

- Two internal Windows 2008 R2 Servers
- Ping command
- Ipconfig command
- Nslookup command

### Machines Used

- Internal DNS Server One: Windows Server 2008 R2 | IP Address: 192.168.12.10
- Internal User Machine Two: Windows Server 2008 R2 | IP Address: 192.168.12.11



## Steps
<br><br>
Step 1. Log into the first internal machine as admin
<br><br>
<img width="985" height="713" alt="SS1_login_admin" src="https://github.com/user-attachments/assets/d028ddce-777e-4219-9098-91ff437df41f" />
<br><br>

Step 2. Open the command line
<br><br>
<img width="1010" height="711" alt="SS2_open_cmd" src="https://github.com/user-attachments/assets/5d1902af-2495-43b9-b5bb-f40e85cceb36" />
<br><br>

Step 3. Issue a ping command to the loopback address to verify the TCP socket is on the local machine
   - C:\Users\Administrator> ping 127.0.0.1
<img width="1012" height="713" alt="SS3_ping_loopback_address" src="https://github.com/user-attachments/assets/21c678ef-c73e-45e7-98bc-58ecbb3e79b6" />
<br><br>

Step 4. Issue a ping command to the host IP address. This is to test the IP configurations of the local host.
   - C:\Users\Administrator> ping 192.168.12.10
<img width="1010" height="720" alt="SS4_ping_local_host" src="https://github.com/user-attachments/assets/8b45ce55-d163-4b52-9d6e-a654dd1317ba" />
<br><br>

Step 5. Now, issue an ipconfig command to look for the default gateway IP address.
   - C:\Users\Administrator> ipconfig /all
<img width="1007" height="721" alt="SS5_ipcong_all" src="https://github.com/user-attachments/assets/656003d5-6191-4109-8001-f73ef9df2493" />
<br><br>

Step 6. Ping the default gateway to see if we can reach it.
   - C:\Users\Administrator> ping 192.168.12.1
<img width="1016" height="717" alt="SS6_ping_default_gateway" src="https://github.com/user-attachments/assets/800f2eb3-cf65-4307-99f9-9364e0b8d58c" />
<br><br>

Step 7. Run the ipconfig command again to take not of the DNS address.
   - C:\Users\Administrator> ipconfig /all
<img width="1012" height="713" alt="SS7_second_DNS_ip" src="https://github.com/user-attachments/assets/8eb98623-e5bf-44eb-bdae-0deb5df68d2a" />
<br><br>

Step 8. Now, ping the DNS address.
   - C:\Users\Administrator> ping 192.168.12.10
<img width="1010" height="714" alt="SS8_ping_to_DNS" src="https://github.com/user-attachments/assets/814c19e4-daad-4982-884e-d3385a7a8575" />
<br><br>

Step 9. Run nslookup command to query the DNS
   - C:\Users\Administrator> nslookup ?
<img width="1010" height="715" alt="SS9_nslookup" src="https://github.com/user-attachments/assets/e1bc66ee-3f9d-43c3-8bb3-82ebec6d35ac" />
<br><br>

Step 10. run nslookup but add the users machine to the end of the command.
   - C:\Users\Administrator> nslookup 192.168.12.11
<img width="997" height="711" alt="SS10_nslookup_local_machine" src="https://github.com/user-attachments/assets/86f824a5-1f03-4c08-a78a-7f622653e41e" />
<br><br>

Step 11. We have concluded that the DNS is not the issue. Based our findings, we could have been provided with the wrong URL. Open a webpage and type the website into the URL.
   - Contact the department to see if you were given the correct URL.
<img width="1014" height="715" alt="SS11_ips_website_not_found" src="https://github.com/user-attachments/assets/83ab22c6-4888-4285-8a13-2a93668e7502" />
<br><br>

Step 12. After contacting the department, we have been provided with the wrong URL.
   - The URL is `http://www.ips.com`. Type the new URL into the search box to see the results.
<br><br>
<img width="1004" height="715" alt="SS12_webpage_successful" src="https://github.com/user-attachments/assets/2b588f8a-2de9-4e18-b53f-80a7a3001674" />
<br><br>

## Lessons Learned
This project provided valuable hands-on experience troubleshooting DNS and internal connectivity. While the troubleshooting process did not fully resolve the problem, it reinforced the importance of following a structured methodology and improved my confidence in diagnosing network related issues that I may encounter in future IT and cybersecurity roles.




