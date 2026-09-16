1. Sai ở bước 2 — kiểm tra định dạng thẻ

Thực tập sinh dùng: Async sang một Lifeline khác.

Đúng phải dùng: Self Message.

Giải thích: Việc kiểm tra định dạng thẻ được thực hiện bởi chính Cổng Thanh Toán, không cần tạo thêm đối tượng/Lifeline mới. Vì vậy phải dùng Self để thể hiện Cổng Thanh Toán tự gọi xử lý trên chính nó.

2. Sai ở bước 6 — gửi hóa đơn qua EmailServer

Thực tập sinh dùng: Sync + Return.

Đúng phải dùng: Async.

Giải thích: Yêu cầu nghiệp vụ nói rõ Cổng Thanh Toán không được chờ EmailServer phản hồi mà phải tiếp tục xử lý. Dùng Sync sẽ khiến luồng bị block/chờ EmailServer, đặc biệt gây vấn đề nếu dịch vụ email phản hồi chậm. Async cho phép gửi sendReceiptEmail() rồi tiếp tục mà không cần Return ngay sau đó.
