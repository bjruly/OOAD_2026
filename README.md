# OOAD_2026
Object-Oriented Analysis and Design (OOAD) project for Cinema Booking Management System (SGU). Built with Java, Java Swing, MySQL, JDBC, Maven, and MVC Architecture.


# 🎬 Cinema Booking Management System - OOAD Project

Dự án **Phân tích, thiết kế và xây dựng Hệ thống Quản lý Rạp phim (Cinema Booking)** là đồ án môn học **Phân tích Thiết kế Hướng đối tượng (OOAD)**[span_5](start_span)[span_5](end_span) tại **Trường Đại học Sài Gòn (SGU)**[span_6](start_span)[span_6](end_span).

---

## 👥 Thông tin nhóm thực hiện (Nhóm 09)[span_7](start_span)[span_7](end_span)
* **Giảng viên hướng dẫn:** Hoàng Mạnh Hà[span_8](start_span)[span_8](end_span)
* **Thành viên nhóm:**[span_9](start_span)[span_9](end_span)
  * 3124411337 - Nguyễn Thanh Tuấn[span_10](start_span)[span_10](end_span)
  * 3124411261 - Đào Hữu Tài[span_11](start_span)[span_11](end_span)
  * 3124411038 - Trần Lê Gia Bảo[span_12](start_span)[span_12](end_span)
  * 3124411245 - Huỳnh Nhật Quang[span_13](start_span)[span_13](end_span)
  * 312441198 - Tô Thành Nhân[span_14](start_span)[span_14](end_span)

---

## 🛠️ Công nghệ sử dụng (Tech Stack)[span_15](start_span)[span_15](end_span)
* **Ngôn ngữ lập trình:** Java[span_16](start_span)[span_16](end_span)
* **Giao diện người dùng:** Java Swing[span_17](start_span)[span_17](end_span)
* **Cơ sở dữ liệu:** MySQL[span_18](start_span)[span_18](end_span)
* **Kết nối CSDL:** JDBC[span_19](start_span)[span_19](end_span)
* **Quản lý dự án & thư viện:** Maven[span_20](start_span)[span_20](end_span)
* **Xử lý mã QR:** ZXing Library[span_21](start_span)[span_21](end_span)
* **Kiến trúc ứng dụng:** MVC Architecture (Model - View - Controller - DAO)[span_22](start_span)[span_22](end_span)

---

## 🏗️ Kiến trúc hệ thống (System Architecture)[span_23](start_span)[span_23](end_span)
Hệ thống được tổ chức phân tầng rõ ràng theo mô hình MVC kết hợp DAO[span_24](start_span)[span_24](end_span):
* **Model:** Đại diện cho dữ liệu và đối tượng nghiệp vụ (`Account`, `Movie`, `Cinema`, `Room`, `Seat`, `Showtime`, `Booking`, `Combo`, `Promotion`, `Review`...)[span_25](start_span)[span_25](end_span).
* **View:** Giao diện người dùng xây dựng bằng Java Swing (`Login`, `MovieDetail`, `SeatSelection`, `Payment`, `Admin`, `Staff`...)[span_26](start_span)[span_26](end_span).
* **Controller:** Điều phối xử lý luồng giữa View và DAO (`MovieController`, `BookingController`, `AuthController`, `AdminController`, `StaffController`...)[span_27](start_span)[span_27](end_span).
* **DAO (Data Access Object):** Thực hiện tương tác dữ liệu CRUD trực tiếp với MySQL thông qua JDBC[span_28](start_span)[span_28](end_span).
* **Database:** Cơ sở dữ liệu quan hệ lưu trữ dữ liệu tập trung[span_29](start_span)[span_29](end_span).

---

## ⚡ Các chức năng chính (Features)[span_30](start_span)[span_30](end_span)

### 1. Khách hàng (Customer)[span_31](start_span)[span_31](end_span)
* Đăng ký, đăng nhập và quản lý tài khoản cá nhân[span_32](start_span)[span_32](end_span).
* Xem danh sách phim, tìm kiếm phim và xem chi tiết phim[span_33](start_span)[span_33](end_span).
* Xem lịch chiếu/suất chiếu theo rạp và phòng chiếu[span_34](start_span)[span_34](end_span).
* Chọn ghế trực quan với cơ chế giữ ghế tạm thời (`AVAILABLE` -> `HELD` -> `BOOKED`)[span_35](start_span)[span_35](end_span).
* Chọn combo dịch vụ đi kèm (Bắp/Nước)[span_36](start_span)[span_36](end_span).
* Áp dụng mã khuyến mãi/giảm giá[span_37](start_span)[span_37](end_span).
* Thực hiện thanh toán, nhận thông tin vé kèm mã QR code[span_38](start_span)[span_38](end_span).
* Tra cứu lịch sử đặt vé[span_39](start_span)[span_39](end_span).
* Đánh giá và viết nhận xét về phim[span_40](start_span)[span_40](end_span).

### 2. Nhân viên (Staff)[span_41](start_span)[span_41](end_span)
* Đăng nhập hệ thống[span_42](start_span)[span_42](end_span).
* Tra cứu thông tin vé và kiểm tra trạng thái vé[span_43](start_span)[span_43](end_span).
* Quét/Kiểm tra mã QR vé của khách hàng[span_44](start_span)[span_44](end_span).
* Thực hiện Check-in vé cho khách vào phòng chiếu[span_45](start_span)[span_45](end_span).

### 3. Quản trị viên (Admin)[span_46](start_span)[span_46](end_span)
* **Quản lý dữ liệu hệ thống:** Quản lý tài khoản người dùng, phân quyền[span_47](start_span)[span_47](end_span).
* **Quản lý rạp & phòng:** Thêm/sửa/xóa thông tin rạp chiếu, phòng chiếu và danh sách ghế[span_48](start_span)[span_48](end_span).
* **Quản lý phim & suất chiếu:** Cập nhật thông tin phim, lên lịch suất chiếu[span_49](start_span)[span_49](end_span).
* **Quản lý dịch vụ & ưu đãi:** Quản lý danh mục Combo và các chương trình khuyến mãi[span_50](start_span)[span_50](end_span).
* **Thống kê & Báo cáo:** Xem báo cáo doanh thu và hoạt động vận hành rạp[span_51](start_span)[span_51](end_span).

---

## 🔄 Quy trình đặt vé cơ bản[span_52](start_span)[span_52](end_span)
```text
Đăng nhập ➔ Chọn Phim ➔ Chọn Suất Chiếu ➔ Chọn Ghế ➔ Giữ Ghế ➔ Chọn Combo ➔ Áp dụng Khuyến Mãi ➔ Thanh Toán ➔ Tạo Vé & QR Code ➔ Check-in tại Rạp[span_53](start_span)[span_53](end_span)
