# 03. Các kịch bản thực nghiệm – Hướng dẫn lựa chọn và chạy

Thư mục gồm 13 kịch bản theo đúng mã trong báo cáo Word. Mỗi thư mục KB có README hướng dẫn người đọc: mục tiêu, môi trường, bước chuẩn bị, lệnh chạy và cách kiểm tra kết quả.

## Quy trình chung khi chạy một KB

1. Mở README của KB và đọc kỹ phần **Môi trường**. Xác định Attacker, Victim, địa chỉ IP và interface.
2. Trên cả hai máy, xác minh IP bằng `ip -br addr`; kiểm tra kết nối bằng `ping` nếu phù hợp.
3. Trên Victim, chuẩn bị dịch vụ cần thiết và bắt PCAP theo lệnh trong README (nếu kịch bản có bước bắt gói).
4. Trên Attacker, đọc `attack.sh`, sửa IP/biến cấu hình nếu README yêu cầu, sau đó chạy:
   ```bash
   chmod +x attack.sh
   ./attack.sh
   ```
5. Dừng tcpdump đúng thời điểm; kiểm tra PCAP bằng `tcpdump -nn -r <file.pcap>` hoặc công cụ được README chỉ dẫn.
6. Chạy Suricata theo đúng Run 1/Run 2 và đúng ruleset, cấu hình, interface/PCAP được mô tả trong README. Không dùng chung thư mục log giữa các lần chạy.
7. Đọc `eve.json`, tệp summary và ảnh minh chứng; đối chiếu SID, IP nguồn/đích và thời điểm.

**Quan trọng:** Không phải mọi KB đều có cùng kiểu chạy. Có KB dùng Suricata offline với `-r`; có KB có script `capture.sh`, `normal.sh` hoặc `run-tests.sh`. Chỉ chạy các script có trong KB và theo đúng thứ tự mô tả ở README của KB đó.

## Danh sách kịch bản

- [KB01_Nmap_SYN_Scan – Nmap SYN Scan](KB01_Nmap_SYN_Scan/README.md)
- [KB02_Nmap_UDP_Scan – Nmap UDP Scan](KB02_Nmap_UDP_Scan/README.md)
- [KB03_Nmap_NSE_OS_Detection – Nmap NSE OS Detection](KB03_Nmap_NSE_OS_Detection/README.md)
- [KB04_SSH_Brute_Force – SSH Brute Force](KB04_SSH_Brute_Force/README.md)
- [KB05_FTP_Brute_Force – FTP Brute Force](KB05_FTP_Brute_Force/README.md)
- [KB06_HTTP_Basic_Auth – HTTP Basic Auth](KB06_HTTP_Basic_Auth/README.md)
- [KB07_Telnet_Brute_Force – Telnet Brute Force](KB07_Telnet_Brute_Force/README.md)
- [KB08_ICMP_Flood – ICMP Flood](KB08_ICMP_Flood/README.md)
- [KB09_TCP_SYN_Flood – TCP SYN Flood](KB09_TCP_SYN_Flood/README.md)
- [KB10_UDP_Flood – UDP Flood](KB10_UDP_Flood/README.md)
- [KB11_SQL_Injection – SQL Injection](KB11_SQL_Injection/README.md)
- [KB12_Reflected_XSS – Reflected XSS](KB12_Reflected_XSS/README.md)
- [KB13_Directory_Enumeration – Directory Enumeration](KB13_Directory_Enumeration/README.md)

## Lưu ý về tệp minh chứng

PCAP, ảnh chụp, TAR.GZ và DOCX gốc hiện vẫn được giữ ở [repository Suricata ban đầu](https://github.com/phanyen206/Suricata/tree/main/scenarios). README trong từng KB có liên kết tới thư mục nguồn tương ứng. Các file nhị phân này chưa được nhân bản sang repository mới; không nên coi một liên kết nguồn là bản sao đã được chuyển.
