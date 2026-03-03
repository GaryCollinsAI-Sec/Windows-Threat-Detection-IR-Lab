# Windows Threat Detection IR Lab

<h2>Objective</h2>
<p>

</p>
<ul>
  <li>Scanned multiple Linux VMs (Ubuntu and Metasploitable 2) for vulnerabilities</li>
  <li>Analyzed and prioritized findings by severity (Critical → Low)</li>
  <li>Developed remediation plans based on scan results</li>
  <li>Tested network segmentation and exposure scenarios using Host-Only and NAT adapters</li>
</ul>

<hr>

<h2>Skills Developed</h2>
<ul>
  <li>Configured and executed Nessus scans (credentialed and non-credentialed)</li>
  <li>Managed virtual lab environments in VirtualBox</li>
  <li>Isolated high-risk targets using Host-Only networking</li>
  <li>Assessed attack surfaces under different network configurations</li>
  <li>Triage and categorize vulnerabilities by severity</li>
  <li>Developed remediation strategies: patching, service deactivation, configuration hardening</li>
</ul>

<hr>

<h2>Tools</h2>
<ul>
  <li>Nessus Essentials (scanner)</li>
  <li>Ubuntu VM</li>
  <li>Metasploitable 2 VM (vulnerable target)</li>
  <li>Oracle VM VirtualBox</li>
  <li>Host-Only and NAT networking</li>
 
</ul>

<hr>

<h2>Implementation Steps</h2>

<h3>Ref 1 – Initial Scan</h3>
<p>Configured and launched a basic network scan in Nessus for the Ubuntu VM.</p>
<img width="1342" height="622" src="https://github.com/user-attachments/assets/504cd364-c08b-41eb-8090-7d99ccdcbd48" />

<h3>Ref 2 – Ubuntu Scan Results</h3>
<p>Dashboard shows 19 findings, including a Medium-severity SMB signing vulnerability. Other results map services like HTTP, SSL/TLS, and SMB.</p>
<img width="1319" height="670" src="https://github.com/user-attachments/assets/c6511caf-9ea5-43a1-84b9-269bd4edad2a" />

<h3>Ref 3 – Metasploitable Deployment</h3>
<p>Deployed Metasploitable 2 VM on Host-Only network. Verified connectivity from host to allow Nessus scans.</p>
<img width="767" height="466" src="https://github.com/user-attachments/assets/093aa790-2261-4d07-8d90-6643258a095f" />

<h3>Ref 4 – Active Scan</h3>
<p>Ran Basic Network Scan policy on Metasploitable 2. Confirmed scan active and performing discovery within isolated lab.</p>
<img width="1430" height="653" src="https://github.com/user-attachments/assets/ef84ebd5-8ed7-400a-a250-c6067d402ded" />

<h3>Ref 5 – Vulnerability Findings</h3>
<p>Metasploitable 2 scan identified dozens of Critical-severity issues, including default credentials and unpatched services. Ubuntu VM scan only revealed a single Medium-severity finding.</p>
<img width="1086" height="438" src="https://github.com/user-attachments/assets/2c71112c-1c79-4ac4-b9d1-ecd61a310c50" />

<h3>Ref 6 – Attack Surface Overview</h3>
<p>Metasploitable 2 exposed over 100 vulnerabilities: Critical backdoors, Telnet, FTP, and other legacy services.</p>
<img width="1474" height="688" src="https://github.com/user-attachments/assets/88e6594a-6719-4323-858f-b878516653a6" />

<h3>Ref 7 – Remediation Focus</h3>
<p>Final scan emphasized remediation: disable legacy services, patch known backdoors, and secure default credentials. Validated potential exploits via Metasploit.</p>
<img width="1571" height="501" src="https://github.com/user-attachments/assets/75d8ea0f-e755-48fe-aaa0-e26bc828b216" />

