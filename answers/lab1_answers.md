# Lab 01 Answers
## CIA & Risk: Hệ thống lưu điểm

**Họ và tên:** Nguyễn Minh Đức.......................................

**MSSV:** 1871020149.............................................

**Lớp/Nhóm:** CNTT18-01.........................................

---

## 1. Assets
Liệt kê ít nhất 2 assets cần bảo vệ.

- Asset 1:Cơ sở dữ liệu thông tin khách hàng (tên, địa chỉ, số điện thoại, email).
- Asset 2:Hệ thống xác thực và quản lý truy cập (danh sách tài khoản, mật khẩu, session token).
- Asset 3 (nếu có):Mã nguồn ứng dụng lõi và tài liệu thiết kế hệ thống.



---

## 2. Mapping CIA
Ghép từng sự cố với CIA.

- Sự cố A -> Availability (vi phạm tính sẵn sàng)
- Sự cố B -> Integrity (vi phạm tính toàn vẹn)
- Sự cố C -> Confidentiality (vi phạm tính bảo mật)


---

## 3. Phân tích sự cố B
- Threat: Tin tặc có kỹ năng trung bình khai thác lỗ hổng SQL Injection để thay đổi dữ liệu số dư tài khoản.
- Vulnerability: Ứng dụng web không kiểm tra (sanitize) đầu vào người dùng trước khi truy vấn cơ sở dữ liệu; thiếu phân quyền ở mức hàng (row-level security).
- Mitigation: Sử dụng truy vấn tham số hóa (parameterized queries) hoặc ORM an toàn.

Áp dụng nguyên tắc least privilege cho tài khoản kết nối DB.

Triển khai Web Application Firewall (WAF) và kiểm tra code (SAST/DAST) định kỳ.

---

## 4. Reflection
Viết 5-7 dòng.
Phân tích sự cố Integrity (sự cố B) cho thấy dù bảo mật tập trung nhiều vào việc ngăn chặn rò rỉ dữ liệu (Confidentiality), nhưng việc đảm bảo dữ liệu không bị sửa đổi trái phép cũng quan trọng không kém. Một lỗ hổng nhỏ ở tầng ứng dụng có thể dẫn đến thiệt hại tài chính nghiêm trọng và mất niềm tin khách hàng. Điều này nhấn mạnh sự cần thiết của kiểm thử xâm nhập thường xuyên và giám sát nhật ký hệ thống để phát hiện hành vi bất thường. Về lâu dài, tổ chức nên xây dựng văn hóa bảo mật trong suốt vòng đời phát triển phần mềm (DevSecOps). Chỉ có kết hợp cả kỹ thuật, quy trình và con người mới giảm thiểu rủi ro một cách toàn diện.


---

## 5. Bonus Flag
`FIT4012{A-?-B-?-C-?}`

Flag của em:

