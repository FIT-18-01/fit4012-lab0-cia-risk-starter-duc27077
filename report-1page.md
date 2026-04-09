# FIT4012 - Report 1 Page
## Lab 01 - CIA & Risk: Hệ thống lưu điểm

### 1. Mục tiêu bài lab
- Nhận diện tài sản cần bảo vệ trong một hệ thống thông tin đơn giản.
- Phân biệt Confidentiality, Integrity, Availability.
- Xác định threat, vulnerability, mitigation.
- Thực hành workflow GitHub cơ bản để nhận và nộp bài.

### 2. Cách làm
- Đọc bối cảnh và xác định các thành phần quan trọng của hệ thống.
- Phân tích từng sự cố theo bộ ba CIA.
- Chọn sự cố B để phân tích sâu hơn theo threat - vulnerability - mitigation.
- Hoàn thiện bài làm trong repo và commit/push lên GitHub.

### 3. Kết quả chính
**Assets:**
- Cơ sở dữ liệu thông tin khách hàng (tên, địa chỉ, số điện thoại, email)
- Hệ thống xác thực và quản lý truy cập (tài khoản, mật khẩu, session token)

**CIA mapping:**
- Sự cố A -> Availability
- Sự cố B -> Integrity
- Sự cố C -> Confidentiality

**Phân tích sự cố B:**
- Threat: Tin tặc khai thác lỗ hổng SQL Injection để thay đổi số dư tài khoản trái phép.
- Vulnerability: Ứng dụng web không kiểm tra đầu vào người dùng; thiếu phân quyền ở mức hàng trong cơ sở dữ liệu.
- Mitigation: Sử dụng truy vấn tham số hóa, áp dụng nguyên tắc least privilege, triển khai WAF và kiểm tra bảo mật mã nguồn định kỳ.

### 4. Kết luận ngắn
Qua bài lab này, em học được cách phân biệt rõ ba thành phần cốt lõi của bảo mật (CIA) và thấy rằng một sự cố có thể ảnh hưởng đến nhiều hơn một yếu tố. Phần khó nhất đối với em là xác định chính xác lỗ hổng (vulnerability) chứ không phải chỉ nêu ra mối đe dọa (threat) chung chung. Khi phân tích một sự cố an toàn thông tin, điều quan trọng là phải nhìn vào nguyên nhân gốc rễ về mặt kỹ thuật và quy trình, không chỉ dừng ở biểu hiện bên ngoài. Em cũng rút ra rằng giảm nhẹ rủi ro (mitigation) cần có giải pháp cụ thể, có thể đo lường được, không nên chỉ đưa ra lời khuyên chung như "tăng cường bảo mật".
