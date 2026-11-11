# 04. Phân tích log Suricata

Mục này dành cho người đọc muốn xem hoặc chạy lại bước phân tích log sau khi hoàn thành các kịch bản.

## Thành phần
- `Ma-nguon/`: script phân tích log.
- `Du-lieu-log/`: dữ liệu EVE JSON hoặc dữ liệu đã trích xuất.
- `Ket-qua-phan-tich/`: bảng thống kê, biểu đồ và kết quả.

## Cách sử dụng
1. Đọc README trong `Ma-nguon/` để biết script nào chạy trước và thư viện cần cài.
2. Đặt log đầu vào theo đúng đường dẫn mà script yêu cầu; nếu đổi đường dẫn, cập nhật cấu hình đầu vào trong script.
3. Chạy từng script theo thứ tự được ghi trong hướng dẫn.
4. So sánh đầu ra với các tệp trong `Ket-qua-phan-tich/`.

EVE JSON của Suricata thường có nhiều loại sự kiện; khi thống kê cảnh báo, cần lọc đúng `event_type == alert` và kiểm tra SID, địa chỉ nguồn/đích. Không coi mỗi dòng log là một cuộc tấn công độc lập.
