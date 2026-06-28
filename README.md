# Firewalls-LAB(allow Internet Control Message Protocol) "ICMP"
Configure firewall rules to allow or block protocols/ports/services


•	Select ZYWIN02 from the drop-down menu in the right pane and click Connect to VMs.

•	The following steps create a firewall inbound rule on ZYWIN02 for allowing Internet Control Message Protocol (ICMP) packets.

•	Click Windows Start and select Server Manager.

<img width="626" height="417" alt="Screenshot" src="https://github.com/user-attachments/assets/7fa407c5-0dad-4253-821b-aa42879eb601" />

•	In Server Manager, select Tools → Windows Defender Firewall with Advanced Security

<img width="975" height="552" alt="image" src="https://github.com/user-attachments/assets/593d2c28-5451-4448-a6e3-5b184b7197aa" />

•	Windows Defender Firewall with Advanced Security allows for the management of inbound or outbound firewall rules.

 <img width="975" height="691" alt="image" src="https://github.com/user-attachments/assets/62662e8f-b55b-4f04-bc13-26ac094a3245" />

•	Click on Inbound Rules. Right-click Inbound Rules and select New Rule….

 <img width="955" height="528" alt="image" src="https://github.com/user-attachments/assets/e4cacc51-57ab-4ddf-9a27-db5ae1a73318" />

•	Select Custom and click Next.

 <img width="975" height="794" alt="image" src="https://github.com/user-attachments/assets/1c035021-c9bd-49c8-9093-e891fd6f5613" />

•	Select All Programs and click Next.

<img width="975" height="794" alt="image" src="https://github.com/user-attachments/assets/0284c849-8443-4a39-a8f3-a4485b82d047" />

•	Select ICMPv4 for protocol type.

<img width="975" height="794" alt="image" src="https://github.com/user-attachments/assets/68d46564-618a-48c4-ad26-92ccb36f5217" />

•	Click Next.

<img width="975" height="794" alt="image" src="https://github.com/user-attachments/assets/6bf70320-0318-4cdd-8da3-a421a8648a07" />

•	Click Next.

<img width="975" height="794" alt="image" src="https://github.com/user-attachments/assets/dc94d8f8-24fb-41b4-a598-88a47e3c1872" />

•	Select Allow the connection and click Next.

<img width="975" height="794" alt="image" src="https://github.com/user-attachments/assets/4e66edcb-a410-439e-ac93-cf84c875383e" />

•	Click Next.

<img width="975" height="794" alt="image" src="https://github.com/user-attachments/assets/8ecd1b30-c4f6-4c2e-a50b-ff3502460baa" />

•	Enter ICMP in the Name field and click Finish.

<img width="975" height="794" alt="image" src="https://github.com/user-attachments/assets/a08e97f3-2f24-4292-838a-1668f657db46" />

•	The ICMP rule is displayed in inbound rules.

<img width="975" height="309" alt="image" src="https://github.com/user-attachments/assets/b5543683-ef00-4a1b-8bd1-c252d71228b1" />

ICMP inbound rule created and enabled.

•	In the right pane select ZYWIN01. In ZYWIN01, click Windows Start and select Windows PowerShell.

<img width="975" height="648" alt="image" src="https://github.com/user-attachments/assets/022cd3c7-4f8c-4863-91ba-d363cf3a96e0" />

•	Run the ping command with destination device ZYWIN02.

•	ping ZYWIN02

•	ping is successful because the ICMP inbound rule on ZYWIN02 allows ICMP messages.

<img width="975" height="340" alt="image" src="https://github.com/user-attachments/assets/fa9e6fd1-cee7-43a4-9336-787e6f9d27b5" />

•	Select ZYWIN02 in the right pane, and return to Windows Defender Firewall with Advanced Security.

•	Disable the inbound ICMP rule by right-clicking on inbound rule ICMP and selecting Disable Rule.

<img width="975" height="700" alt="image" src="https://github.com/user-attachments/assets/3a4732c3-61c3-483e-bc04-7ccc2bd81ea5" />

•	In a PowerShell window on ZYWIN01, run the ping command with destination device ZYWIN02.

•	ping ZYWIN02

•	ping is unsuccessful because the ICMP inbound rule on ZYWIN02 is disabled, not allowing ICMP messages.

<img width="975" height="239" alt="image" src="https://github.com/user-attachments/assets/8e5ab3cc-5d3f-4c5c-956e-f7d6cd08bc68" />

•	ping ZYWIN02 executed.



