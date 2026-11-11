# KB02_Nmap_UDP_Scan – Nmap UDP Scan

## Mục tiêu
Mô tả hành vi cần kiểm tra và mục tiêu của kịch bản.

## Môi trường
- Attacker:
- Victim:
- Dịch vụ/cổng liên quan:
- Phiên bản Suricata:
- Interface giám sát:

## Chuẩn bị Victim
Ghi các lệnh cấu hình dịch vụ và kiểm tra trạng thái đã thực sự sử dụng vào `lenh-may-nan-nhan.md`.

## Thực hiện Attacker
Ghi lệnh đã thực sự chạy vào `lenh-tan-cong.sh`.

## Luật Suricata
Đưa đúng luật đã dùng vào `luat-suricata.rules`; ghi SID, rev và giải thích điều kiện phát hiện. Không suy đoán luật.

## Kết quả và minh chứng
Bổ sung PCAP, EVE JSON, ảnh chụp và kết quả thực tế nếu có. Phân biệt lưu lượng tấn công và bình thường.

## Đối chiếu repository cũ
Thư mục nguồn cũ: `02-nmap-udp-scan`. Đây chỉ là đường dẫn truy xuất nguồn; mã KB chính thức là `KB02` theo báo cáo Word.

## Checklist bàn giao
- [ ] README đã đối chiếu báo cáo
- [ ] Lệnh Attacker
- [ ] Lệnh Victim
- [ ] Luật thực tế đã chạy
- [ ] Minh chứng (nếu có)
- [ ] Đã kiểm tra IP, interface, SID và phiên bản
