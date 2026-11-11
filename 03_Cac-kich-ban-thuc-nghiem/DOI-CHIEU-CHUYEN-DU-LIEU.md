# Đối chiếu và chuyển dữ liệu từ repository Suricata cũ

Nguồn: [phanyen206/Suricata – scenarios](https://github.com/phanyen206/Suricata/tree/main/scenarios).

Mã KB ở repository mới được chuẩn hóa theo báo cáo Word 13 kịch bản. Tên thư mục cũ được ghi lại để truy xuất nguồn, không dùng làm mã KB chính thức.

## Bảng ánh xạ và tình trạng chuyển

| KB mới | Thư mục nguồn cũ | Đã chuyển vào repository mới | Còn ở repository nguồn |
|---|---|---|---|
| KB01 Nmap SYN Scan | [01-nmap-syn-scan](https://github.com/phanyen206/Suricata/tree/main/scenarios/01-nmap-syn-scan) | README hướng dẫn, attack.sh, custom-rule.rules, 2 EVE attack, 2 EVE benign, lệnh Attacker/Victim, lệnh benign, summary Run 1/2 | 5 PCAP, 24 PNG và README ảnh |
| KB02 Nmap UDP Scan | [02-nmap-udp-scan](https://github.com/phanyen206/Suricata/tree/main/scenarios/02-nmap-udp-scan) | README, attack.sh, custom-rule.rules, 2 EVE attack, 2 EVE benign, lệnh Attacker/Victim, summary Run 1 | 5 PCAP, 22 PNG, summary Run 2 |
| KB03 Nmap NSE OS Detection | [05-nmap-nse-os-detect](https://github.com/phanyen206/Suricata/tree/main/scenarios/05-nmap-nse-os-detect) | README, attack.sh, custom-rule.rules, 2 EVE attack, 2 EVE benign, lệnh Attacker/Victim, summary Run 1/2 | 5 PCAP, 17 PNG |
| KB04 SSH Brute Force | [06-ssh-bruteforce](https://github.com/phanyen206/Suricata/tree/main/scenarios/06-ssh-bruteforce) | README, attack.sh | Tài liệu KB06.docx gốc |
| KB05 FTP Brute Force | [07-ftp-bruteforce](https://github.com/phanyen206/Suricata/tree/main/scenarios/07-ftp-bruteforce) | README, attack.sh | Tài liệu KB07.docx gốc |
| KB06 HTTP Basic Auth | [08-http-basic-auth-bruteforce](https://github.com/phanyen206/Suricata/tree/main/scenarios/08-http-basic-auth-bruteforce) | README, attack.sh | Tài liệu KB08.docx gốc |
| KB07 Telnet Brute Force | [09-telnet-bruteforce](https://github.com/phanyen206/Suricata/tree/main/scenarios/09-telnet-bruteforce) | README, attack.sh | Tài liệu KB09.docx gốc |
| KB08 ICMP Flood | [10-icmp-flood](https://github.com/phanyen206/Suricata/tree/main/scenarios/10-icmp-flood) | README, attack.sh, capture.sh, normal.sh, run-tests.sh, custom-rule.rules, custom-rule-original.rules | 11 PNG (có một tên file .1png), KB10-evidence.tar.gz |
| KB09 TCP SYN Flood | [11-syn-flood](https://github.com/phanyen206/Suricata/tree/main/scenarios/11-syn-flood) | README, attack.sh, capture.sh, http-server.sh, normal.sh, run-tests.sh, custom-rule.rules, EVE Run 2 | PNG, KB11-evidence.tar.gz; một số EVE file nguồn rỗng |
| KB10 UDP Flood | [12-udp-flood](https://github.com/phanyen206/Suricata/tree/main/scenarios/12-udp-flood) | README, attack.sh, capture.sh, normal.sh, run-tests.sh, custom-rule.rules | PNG, KB12-evidence.tar.gz |
| KB11 SQL Injection | [13-sql-injection](https://github.com/phanyen206/Suricata/tree/main/scenarios/13-sql-injection) | README, attack.sh, tệp luật trích từ khối luật trong README nguồn | Nguồn không có PCAP/log rời trong thư mục này |
| KB12 Reflected XSS | [14-reflected-xss](https://github.com/phanyen206/Suricata/tree/main/scenarios/14-reflected-xss) | README hướng dẫn tái lập, attack.sh, các khối luật được ghi trong README | 7 PNG minh chứng |
| KB13 Directory Enumeration | [15-dir-bruteforce](https://github.com/phanyen206/Suricata/tree/main/scenarios/15-dir-bruteforce) | README, attack.sh, tệp luật trích từ README nguồn | Nguồn không có PCAP/log rời trong thư mục này |

## Vì sao một số tệp chưa được sao chép?

Trong lượt chuyển này, thao tác đọc/ghi qua GitHub chỉ xử lý được nội dung văn bản UTF-8. Các tệp nhị phân như `.pcap`, `.png`, `.docx`, `.tar.gz` không thể được tải ra dưới dạng nội dung văn bản để tạo bản sao nhị phân chính xác. Vì vậy, chúng được giữ nguyên ở repository nguồn và README của từng KB có liên kết đến thư mục gốc.

**Không xóa repository cũ.** Chỉ chuyển/xóa các tệp nguồn sau khi đã tải được bản nhị phân, kiểm tra kích thước/hash và xác nhận bản sao mở được.

## Lưu ý quan trọng khi sử dụng

1. KB04–KB07: tài liệu cấu hình Victim và luật được lưu trong DOCX nguồn; README mới chưa tự tách các nội dung này thành file riêng. Mở DOCX tại link nguồn trước khi tái lập.
2. KB11–KB13: một số luật được trích từ phần code block trong README nguồn. Cần đối chiếu với ảnh/log lần chạy trước khi coi là bản luật cuối cùng đã dùng.
3. Các script `attack.sh` giữ nguyên nội dung từ nguồn; kiểm tra IP, interface, đường dẫn và quyền thực thi trước khi chạy.
4. Tệp EVE JSON benign của KB01–KB03 được chuyển nguyên nội dung từ nguồn; dung lượng lớn không có nghĩa là toàn bộ log gốc, cần xem tên tệp và README để hiểu phạm vi excerpt.
5. Không có PCAP hoặc ảnh nào được tạo mới để lấp chỗ trống.
