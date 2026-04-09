# Lab 01 Answers
## CIA & Risk: Hệ thống lưu điểm

**Họ và tên:** Nguyễn Minh Đức.......................................

**MSSV:** 1871020149.............................................

**Lớp/Nhóm:** CNTT18-01.........................................

---

## 1. Assets
Liệt kê ít nhất 2 assets cần bảo vệ.

- Asset 1: Dữ liệu người dùng (thông tin cá nhân, tài khoản, mật khẩu)
- Asset 2: Hệ thống server / cơ sở dữ liệu
- Asset 3 (nếu có): Ứng dụng web (source code, API)

---

## 2. Mapping CIA
Ghép từng sự cố với CIA.

- Sự cố A -> Confidentiality (Lộ dữ liệu người dùng)
- Sự cố B -> Integrity (Dữ liệu bị sửa đổi trái phép)
- Sự cố C -> Availability (Hệ thống bị sập / không truy cập được)


---

## 3. Phân tích sự cố B
- Threat: Hacker tấn công và thay đổi dữ liệu (SQL Injection, tấn công nội bộ, v.v.)
- Vulnerability: Không kiểm tra input, thiếu validation, phân quyền kém
- Mitigation: Sử dụng prepared statements (chống SQL Injection)
Kiểm tra và validate dữ liệu đầu vào
Phân quyền người dùng rõ ràng
Log và giám sát hệ thống


---

## 4. Reflection
Viết 5-7 dòng.
Qua bài này, em hiểu rõ hơn về tầm quan trọng của bảo mật trong hệ thống thông tin. Ba yếu tố CIA (Confidentiality, Integrity, Availability) giúp đánh giá và phân loại các rủi ro một cách rõ ràng. Việc xác định assets giúp biết được cái gì cần bảo vệ trước tiên. Ngoài ra, phân tích threat và vulnerability giúp tìm ra nguyên nhân gốc rễ của sự cố. Từ đó, có thể đề xuất các biện pháp mitigation phù hợp để giảm thiểu rủi ro. Đây là kiến thức quan trọng khi thiết kế và vận hành hệ thống phần mềm.

---

## 5. Bonus Flag
`FIT4012{A-?-B-?-C-?}`

Flag của em:

