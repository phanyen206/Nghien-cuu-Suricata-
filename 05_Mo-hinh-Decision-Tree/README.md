# 05. Mô hình Decision Tree

Mục này chứa mã nguồn và kết quả mô hình Decision Tree dùng cho bài toán phân loại lưu lượng mạng.

## Thành phần
- `Ma-nguon/`: các script tiền xử lý, tạo đặc trưng, huấn luyện và đánh giá.
- `Du-lieu/`: dữ liệu đầu vào hoặc hướng dẫn lấy dữ liệu.
- `Ket-qua/`: báo cáo phân loại, confusion matrix, biểu đồ và mô hình đã lưu (nếu có).

## Quy trình sử dụng
1. Đọc hướng dẫn trong `Ma-nguon/` và xác định đúng phiên bản Python/thư viện.
2. Chuẩn bị dữ liệu đúng định dạng và đường dẫn.
3. Chạy tiền xử lý/tạo đặc trưng trước khi huấn luyện.
4. Chạy script huấn luyện và đánh giá theo đúng thứ tự.
5. Đối chiếu precision, recall, F1-score và confusion matrix trong `Ket-qua/`.

Dữ liệu CIC-IDS2017 và log EVE JSON từ lab Suricata là hai nguồn khác nhau; không gộp chúng nếu chưa có quy trình chuyển đổi, nhãn và mục tiêu thí nghiệm được mô tả rõ.
