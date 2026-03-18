Q1 : Understanding the adversary helps defend against attacks. What is the name of the malware family that causes abnormal network traffic?

Tên đầy đủ của malware này là : Yellow Cockatoo RAT

Q2 : As part of our incident response, knowing common filenames the malware uses can help scan other workstations for potential infection. What is the common filename associated with the malware discovered on our workstations?

Truy cập phần Details của VirusTotal để tìm kiếm, có thể thấy tên tệp là : 111bc461-1ca8-43c6-97ed-911e0e69fdf8.dll

<img width="646" height="213" alt="{E396E6E9-5B8F-48DF-B736-94BACB828CFD}" src="https://github.com/user-attachments/assets/d77e36bd-33bc-4ff1-b87c-db47d4fce8a0" />


Q3 : Determining the compilation timestamp of malware can reveal insights into its development and deployment timeline. What is the compilation timestamp of the malware that infected our network?

Thời điểm báo cáo đầu tiên về malware này là : 2020-09-24 18:26:47

<img width="318" height="126" alt="{7793F80E-D4E7-4592-B68D-06D1894E58B2}" src="https://github.com/user-attachments/assets/b99bf76f-aee6-469a-b5f4-5e89f0dd1839" />


Q4 : Understanding when the broader cybersecurity community first identified the malware could help determine how long the malware might have been in the environment before detection. When was the malware first submitted to VirusTotal?

Từ phần History ta có thể biết được lần đầu tiên malware được phát hiện là : 2020-10-15 02:47:37

<img width="301" height="128" alt="{EB38DF6B-6CA6-4969-800A-D2C1C6ADDA58}" src="https://github.com/user-attachments/assets/99c76b52-880a-459d-b2c1-0d01e630a11d" />

Q5 : To completely eradicate the threat from Industries' systems, we need to identify all components dropped by the malware. What is the name of the .dat file that the malware dropped in the AppData folder?

Tìm kiếm thông tin trên internet ta có được : solarmarker.dat

<img width="278" height="50" alt="{93FB39C4-B45C-4A97-AFA7-5FDA0D35004B}" src="https://github.com/user-attachments/assets/45f47416-81d8-4ac2-8cda-60acdf6da3c8" />

Q6 : It is crucial to identify the C2 servers with which the malware communicates to block its communication and prevent further data exfiltration. What is the C2 server that the malware is communicating with?

Vào phần Network Communications để tìm kiếm xem máy đã kết nối với máy chủ C2 nào

<img width="649" height="605" alt="{DAAD2368-BA1F-492A-A27A-5F6579B46600}" src="https://github.com/user-attachments/assets/bc592924-a7a2-4bd2-8290-7a89d0d53dee" />

Ta có thể thấy phần mềm độc hại: 
https://gogohid.com

