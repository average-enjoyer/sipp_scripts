<h2>Description of the test:</h2>
The scenario makes a call from the account specified in field 0 to the account specified in field 2 (see vars.csv).
The test had only one SIPp script - caller.xml (for caller). As a callee, you should register any UA and simply answer a call after start the caller's SIPp script.
Before start, please, change the path to the g711a.pcap file (use absolute path here!) in the caller.xml.

Scenario:
	0. Register 555000 using any UA;
	1. SIPp caller calls 555000 (field 2);
	2. 555000 answers the call;
	* SIPp caller and 555000 can hear each other;
	3. SIPp caller puts the call on hold;
	4. SIPp caller releases the call from holding;
	* SIPp caller and 555000 can hear each other;
	5. SIPp caller end hang up.

<h3>Command to start:</h3>
sudo sipp <PBX_IP or VIP> -sf caller.xml -inf vars.csv -m 1
