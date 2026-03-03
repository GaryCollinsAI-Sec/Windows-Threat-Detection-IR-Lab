# Windows Threat Detection IR Lab

<h2>Objective</h2>
<p>
This lab builds a functional SOC environment to simulate real-world attacks, monitor endpoint telemetry, and practice incident response. By integrating Windows (Sysmon) for telemetry, Splunk for analysis, and Kali Linux for adversarial simulation, you create a full-stack laboratory to hunt for threats and develop high-fidelity detection rules.
</p>

<hr>

<h2>Skills Developed</h2>
<ul>
  <li>SIEM Administration: Installing and configuring Splunk Enterprise and Universal Forwarders.</li>
  <li>Endpoint Visibility: Deploying SwiftOnSecurity-style Sysmon configurations for advanced threat hunting.</li>
  <li>Adversarial Emulation: Utilizing Metasploit/Nmap on Kali to simulate attacker behavior.</li>
  <li>Assessed attack surfaces under different network configurations</li>
  <li>Query Crafting: Writing SPL (Splunk Processing Language) to correlate disparate events.</li>
  <li>Threat Detection: Identifying "Living off the Land" (LotL) binaries and obfuscated PowerShell execution.</li>
</ul>

<hr>

<h2>Tools</h2>
<ul>
  <li>Splunk Enterprise: The "Brain" (SIEM) for data indexing and visualization.</li>
  <li>Windows 10/11 VM: The "Target" workstation for monitoring.</li>
  <li>Sysmon: Advanced Windows host logging tool.</li>
  <li>Kali Linux: The "Attacker" machine.</li>
  <li>Splunk Universal Forwarder: For shipping logs from Windows to Splunk.</li>
 
</ul>

<hr>

<h2>Implementation Steps</h2>


Ref 1 – Splunk & Sysmon Installation
<p>Installed Splunk Enterprise to act as the SIEM and deployed Sysmon on the Windows target using a customized configuration file to capture deep endpoint telemetry.</p>


Ref 2 – Ingesting Windows Logs
<p>Configured the Splunk Universal Forwarder to ship Sysmon (Event ID 1, 3, and 11) and Windows Security logs into a dedicated index for real-time monitoring.</p>


Ref 3 – Kali Adversarial Activity
<p>Used Kali Linux to execute a Metasploit reverse shell payload against the Windows VM, establishing a command-and-control (C2) session over the network.</p>


Ref 4 – Splunk Detection Query
<p>Ran a Splunk Search Processing Language (SPL) query to identify the malicious process tree and the specific Kali IP address associated with the network connection.</p>


Ref 5 – Incident Analysis Dashboard
<p>Created a security dashboard visualizing telemetry spikes, such as unauthorized PowerShell execution and suspicious network beacons from the Windows host.</p>

