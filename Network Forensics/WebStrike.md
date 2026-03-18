Q1 : Identifying the geographical origin of the attack facilitates the implementation of geo-blocking measures and the analysis of threat intelligence. From which city did the attack originate?

Mở WebStrike.pcap và lọc GET bằng lệnh: http.request.method == GET từ đó ta có thể thấy hàng loạt repuest từ IP 117.11.88.124

<img width="610" height="435" alt="{4EBA8CDE-C92A-493B-8AD2-90245AA6032B}" src="https://github.com/user-attachments/assets/88c0dd85-c11a-4622-b07c-ba869fd7da78" />

Địa chỉ IP là ở Tianjin-China

<img width="534" height="554" alt="{748A587B-4943-4B3C-A7FE-3A966EFB3276}" src="https://github.com/user-attachments/assets/566536b0-8415-4023-b16d-aa1fdcbe4814" />

Q2 : Knowing the attacker's User-Agent assists in creating robust filtering rules. What's the attacker's Full User-Agent?

Follow một gói tin bất kì ta có thể tìm thấy User-Agent : Mozilla/5.0 (X11; Linux x86_64; rv:109.0) Gecko/20100101 Firefox/115.0

<img width="485" height="554" alt="{5D10FC42-7682-4047-B9F4-C85ED4CCA449}" src="https://github.com/user-attachments/assets/83113f7f-32a4-4c8d-9be2-2c5e8b0789a7" />

Q3 : We need to determine if any vulnerabilities were exploited. What is the name of the malicious web shell that was successfully uploaded?

Dùng lệnh http.request.method == POST để lọc toàn bộ POST giúp tìm gói mà tin tặc đã upload thành công

 <img width="786" height="248" alt="{03A7395B-357E-4DE8-805F-2A46F18C9FC0}" src="https://github.com/user-attachments/assets/9ebe9ad0-c544-4343-a7a7-227431b98825" />

Có thể thấy tin tặc đã upload 2 file nhưng có 1 file không upload thành công do sai định dạng, sau đó tin tặc đã upload thành công lần 2 với filename là: image.jpg.php

<img width="875" height="584" alt="{EB3CB532-C60C-442D-A8F5-7D45450B1A71}" src="https://github.com/user-attachments/assets/b3383140-3f33-4d07-8a82-ea86368dbc90" />

Q4 : Identifying the directory where uploaded files are stored is crucial for locating the vulnerable page and removing any malicious files. Which directory is used by the website to store the uploaded files?

Ngay trong gói POST đã có địa chỉ mà tin tặc đã tải lên : /reviews/uploads/

<img width="726" height="141" alt="{D627AD97-78E0-4E84-A1DF-697D85468E5E}" src="https://github.com/user-attachments/assets/3c7304a2-2752-45f3-a444-e9ba8a95e296" />

Q5 : Which port, opened on the attacker's machine, was targeted by the malicious web shell for establishing unauthorized outbound communication?

Trong gói POST tin tặc đã chèn lệnh PHP và giao tiếp ra ngoài nhờ cổng 8080

<img width="534" height="597" alt="{399CAAC7-722A-4DF1-A87C-440724C4731E}" src="https://github.com/user-attachments/assets/c1309bbc-d287-4a63-9d8c-c16491dacaa8" />

Q6 : Recognizing the significance of compromised data helps prioritize incident response actions. Which file was the attacker attempting to exfiltrate?

Bắt giữ lưu lượng truy cập đi ra từ máy chủ nạn nhân 24.49.63.79 đến máy của kẻ tấn công trên cổng 8080 bằng cách filter : (tcp.port==8080) && (ip.src==24.49.63.79)

<img width="487" height="598" alt="{D44E0D48-264B-4F0C-9BB1-71209E1D04EB}" src="https://github.com/user-attachments/assets/db904e0e-9269-4e73-aebd-f6986b44668d" />

Ta có thể thấy tin tặc đang lấy cắp tệp tin: passwd






