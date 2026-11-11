# Nghiên cứu hệ thống phát hiện xâm nhập Suricata

Repository lưu trữ tài liệu, mã nguồn và dữ liệu thực nghiệm của đề tài.

## Cấu trúc
- [01_Moi-truong-thuc-nghiem](01_Moi-truong-thuc-nghiem/README.md) – Mô hình mạng, Attacker/Victim, cài đặt.
- [02_Cau-hinh-Suricata](02_Cau-hinh-Suricata/README.md) – Cấu hình và luật Suricata dùng chung.
- [03_Cac-kich-ban-thuc-nghiem](03_Cac-kich-ban-thuc-nghiem/README.md) – 13 kịch bản theo mã trong báo cáo Word.
- [04_Phan-tich-log-Suricata](04_Phan-tich-log-Suricata/README.md) – Mã nguồn, log và kết quả phân tích.
- [05_Mo-hinh-Decision-Tree](05_Mo-hinh-Decision-Tree/README.md) – Mã nguồn, dữ liệu và kết quả Decision Tree.
- [06_Tong-hop-ket-qua-thuc-nghiem](06_Tong-hop-ket-qua-thuc-nghiem/README.md) – Bảng tổng hợp và biểu đồ.
- [07_Tai-lieu-bao-cao](07_Tai-lieu-bao-cao/README.md) – Báo cáo và hướng dẫn.

## Danh sách kịch bản
- [KB01_Nmap_SYN_Scan – Nmap SYN Scan](03_Cac-kich-ban-thuc-nghiem/KB01_Nmap_SYN_Scan/README.md)
- [KB02_Nmap_UDP_Scan – Nmap UDP Scan](03_Cac-kich-ban-thuc-nghiem/KB02_Nmap_UDP_Scan/README.md)
- [KB03_Nmap_NSE_OS_Detection – Nmap NSE OS Detection](03_Cac-kich-ban-thuc-nghiem/KB03_Nmap_NSE_OS_Detection/README.md)
- [KB04_SSH_Brute_Force – SSH Brute Force](03_Cac-kich-ban-thuc-nghiem/KB04_SSH_Brute_Force/README.md)
- [KB05_FTP_Brute_Force – FTP Brute Force](03_Cac-kich-ban-thuc-nghiem/KB05_FTP_Brute_Force/README.md)
- [KB06_HTTP_Basic_Auth – HTTP Basic Auth Brute Force](03_Cac-kich-ban-thuc-nghiem/KB06_HTTP_Basic_Auth/README.md)
- [KB07_Telnet_Brute_Force – Telnet Brute Force](03_Cac-kich-ban-thuc-nghiem/KB07_Telnet_Brute_Force/README.md)
- [KB08_ICMP_Flood – ICMP Flood](03_Cac-kich-ban-thuc-nghiem/KB08_ICMP_Flood/README.md)
- [KB09_TCP_SYN_Flood – TCP SYN Flood](03_Cac-kich-ban-thuc-nghiem/KB09_TCP_SYN_Flood/README.md)
- [KB10_UDP_Flood – UDP Flood](03_Cac-kich-ban-thuc-nghiem/KB10_UDP_Flood/README.md)
- [KB11_SQL_Injection – SQL Injection](03_Cac-kich-ban-thuc-nghiem/KB11_SQL_Injection/README.md)
- [KB12_Reflected_XSS – Reflected XSS](03_Cac-kich-ban-thuc-nghiem/KB12_Reflected_XSS/README.md)
- [KB13_Directory_Enumeration – Directory Enumeration](03_Cac-kich-ban-thuc-nghiem/KB13_Directory_Enumeration/README.md)

## Quy ước bàn giao
Mỗi KB cần bổ sung README, lệnh thực tế trên Attacker, hướng dẫn cấu hình Victim, đúng luật Suricata đã chạy và minh chứng có thật (PCAP, EVE JSON, ảnh/kết quả nếu có).

**Nguyên tắc:** mã KB theo báo cáo Word; không tự tạo giả luật, log, PCAP, ảnh hoặc số liệu. Không commit mật khẩu, token hay thông tin đăng nhập. Ghi rõ thành phần còn thiếu.
