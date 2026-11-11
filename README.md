# Nghiên cứu hệ thống phát hiện xâm nhập Suricata

Kho mã lưu trữ tài liệu hướng dẫn tái lập, script, luật và kết quả thực nghiệm Suricata IDS cùng mô hình Decision Tree.

## Bắt đầu từ đâu?

1. Đọc [môi trường thực nghiệm](01_Moi-truong-thuc-nghiem/README.md) để hiểu sơ đồ mạng, vai trò Attacker/Victim và phiên bản phần mềm.
2. Đọc [cấu hình Suricata](02_Cau-hinh-Suricata/README.md) trước khi chạy các kịch bản.
3. Chọn một KB trong [13 kịch bản](03_Cac-kich-ban-thuc-nghiem/README.md). README trong mỗi KB là hướng dẫn cho người chạy lại thí nghiệm: yêu cầu, chuẩn bị, lệnh chạy, cách đọc log và kết quả đã ghi nhận.
4. Xem [phân tích log](04_Phan-tich-log-Suricata/README.md), [Decision Tree](05_Mo-hinh-Decision-Tree/README.md) và [tổng hợp kết quả](06_Tong-hop-ket-qua-thuc-nghiem/README.md).

## Cấu trúc repository

- [01_Moi-truong-thuc-nghiem](01_Moi-truong-thuc-nghiem/README.md) – Mô hình mạng và môi trường chạy.
- [02_Cau-hinh-Suricata](02_Cau-hinh-Suricata/README.md) – Cấu hình và luật dùng chung.
- [03_Cac-kich-ban-thuc-nghiem](03_Cac-kich-ban-thuc-nghiem/README.md) – 13 kịch bản theo báo cáo Word.
- [04_Phan-tich-log-Suricata](04_Phan-tich-log-Suricata/README.md) – Mã nguồn và log phân tích.
- [05_Mo-hinh-Decision-Tree](05_Mo-hinh-Decision-Tree/README.md) – Mã nguồn, dữ liệu và kết quả Decision Tree.
- [06_Tong-hop-ket-qua-thuc-nghiem](06_Tong-hop-ket-qua-thuc-nghiem/README.md) – Bảng tổng hợp, biểu đồ.
- [07_Tai-lieu-bao-cao](07_Tai-lieu-bao-cao/README.md) – Báo cáo và hướng dẫn.

## Danh sách kịch bản

- [KB01_Nmap_SYN_Scan – Nmap SYN Scan](03_Cac-kich-ban-thuc-nghiem/KB01_Nmap_SYN_Scan/README.md)
- [KB02_Nmap_UDP_Scan – Nmap UDP Scan](03_Cac-kich-ban-thuc-nghiem/KB02_Nmap_UDP_Scan/README.md)
- [KB03_Nmap_NSE_OS_Detection – Nmap NSE OS Detection](03_Cac-kich-ban-thuc-nghiem/KB03_Nmap_NSE_OS_Detection/README.md)
- [KB04_SSH_Brute_Force – SSH Brute Force](03_Cac-kich-ban-thuc-nghiem/KB04_SSH_Brute_Force/README.md)
- [KB05_FTP_Brute_Force – FTP Brute Force](03_Cac-kich-ban-thuc-nghiem/KB05_FTP_Brute_Force/README.md)
- [KB06_HTTP_Basic_Auth – HTTP Basic Auth](03_Cac-kich-ban-thuc-nghiem/KB06_HTTP_Basic_Auth/README.md)
- [KB07_Telnet_Brute_Force – Telnet Brute Force](03_Cac-kich-ban-thuc-nghiem/KB07_Telnet_Brute_Force/README.md)
- [KB08_ICMP_Flood – ICMP Flood](03_Cac-kich-ban-thuc-nghiem/KB08_ICMP_Flood/README.md)
- [KB09_TCP_SYN_Flood – TCP SYN Flood](03_Cac-kich-ban-thuc-nghiem/KB09_TCP_SYN_Flood/README.md)
- [KB10_UDP_Flood – UDP Flood](03_Cac-kich-ban-thuc-nghiem/KB10_UDP_Flood/README.md)
- [KB11_SQL_Injection – SQL Injection](03_Cac-kich-ban-thuc-nghiem/KB11_SQL_Injection/README.md)
- [KB12_Reflected_XSS – Reflected XSS](03_Cac-kich-ban-thuc-nghiem/KB12_Reflected_XSS/README.md)
- [KB13_Directory_Enumeration – Directory Enumeration](03_Cac-kich-ban-thuc-nghiem/KB13_Directory_Enumeration/README.md)

## Quy tắc khi tái lập

- Thực hiện trong mạng lab/VM được phép, không chạy script vào hệ thống bên ngoài.
- Trước khi chạy, kiểm tra IP, interface và dịch vụ; thay giá trị mẫu theo đúng môi trường của người chạy.
- Đọc script trước khi chạy: một số script dùng `sudo`, gửi lưu lượng lớn hoặc ghi PCAP.
- Không ghi đè thư mục log/PCAP cũ; mỗi lần chạy nên dùng thư mục kết quả riêng.
- Kết quả trong README là kết quả của môi trường được mô tả, không đảm bảo lặp lại giống hệt trên môi trường khác.

## Nguồn dữ liệu gốc và phần chưa chuyển

Repository nguồn: [phanyen206/Suricata](https://github.com/phanyen206/Suricata).

Các tệp văn bản có thể đọc được qua GitHub đã được chuyển vào các KB mới, gồm README hướng dẫn, script shell, luật, một số tệp lệnh và EVE JSON. Các tệp nhị phân PCAP, ảnh PNG, gói TAR.GZ và tài liệu DOCX vẫn được giữ ở repository nguồn; README từng KB có liên kết về thư mục gốc để xem/tải. Chúng chưa được sao chép nhị phân sang repository này trong lượt chuyển hiện tại.

Không tạo giả luật, PCAP, log, ảnh hoặc số liệu. Những gì chưa có minh chứng phải được ghi rõ là chưa xác minh.
