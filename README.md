# OOAD_2026
Object-Oriented Analysis and Design (OOAD) project for Cinema Booking Management System (SGU). Built with Java, Java Swing, MySQL, JDBC, Maven, and MVC Architecture.


# 🎬 Cinema Booking Management System - OOAD Project

Dự án **Phân tích, thiết kế và xây dựng Hệ thống Quản lý Rạp phim (Cinema Booking)** là đồ án môn học **Phân tích Thiết kế Hướng đối tượng (OOAD)** tại **Trường Đại học Sài Gòn (SGU)**.

---

## 👥 Thông tin nhóm thực hiện (Nhóm 09)
* **Giảng viên hướng dẫn:** Hoàng Mạnh Hà
* **Thành viên nhóm:**
  * 3124411337 - Nguyễn Thanh Tuấn
  * 3124411261 - Đào Hữu Tài
  * 3124411038 - Trần Lê Gia Bảo
  * 3124411245 - Huỳnh Nhật Quang
  * 3124411198 - Tô Thành Nhân

---

## 🛠️ Công nghệ sử dụng (Tech Stack)
* **Ngôn ngữ lập trình:** Java
* **Giao diện người dùng:** Java Swing
* **Cơ sở dữ liệu:** MySQL
* **Kết nối CSDL:** JDBC
* **Quản lý dự án & thư viện:** Maven
* **Xử lý mã QR:** ZXing Library
* **Kiến trúc ứng dụng:** MVC Architecture (Model - View - Controller - DAO)

---

## 🏗️ Kiến trúc hệ thống (System Architecture)
Hệ thống được tổ chức phân tầng rõ ràng theo mô hình MVC kết hợp DAO:
* **Model:** Đại diện cho dữ liệu và đối tượng nghiệp vụ (`Account`, `Movie`, `Cinema`, `Room`, `Seat`, `Showtime`, `Booking`, `Combo`, `Promotion`, `Review`...).
* **View:** Giao diện người dùng xây dựng bằng Java Swing (`Login`, `MovieDetail`, `SeatSelection`, `Payment`, `Admin`, `Staff`...).
* **Controller:** Điều phối xử lý luồng giữa View và DAO (`MovieController`, `BookingController`, `AuthController`, `AdminController`, `StaffController`...).
* **DAO (Data Access Object):** Thực hiện tương tác dữ liệu CRUD trực tiếp với MySQL thông qua JDBC.
* **Database:** Cơ sở dữ liệu quan hệ lưu trữ dữ liệu tập trung.

---

## ⚡ Các chức năng chính (Features)

### 1. Khách hàng (Customer)
* Đăng ký, đăng nhập và quản lý tài khoản cá nhân.
* Xem danh sách phim, tìm kiếm phim và xem chi tiết phim.
* Xem lịch chiếu/suất chiếu theo rạp và phòng chiếu.
* Chọn ghế trực quan với cơ chế giữ ghế tạm thời (`AVAILABLE` -> `HELD` -> `BOOKED`).
* Chọn combo dịch vụ đi kèm (Bắp/Nước).
* Áp dụng mã khuyến mãi/giảm giá.
* Thực hiện thanh toán, nhận thông tin vé kèm mã QR code.
* Tra cứu lịch sử đặt vé.
* Đánh giá và viết nhận xét về phim.

### 2. Nhân viên (Staff)
* Đăng nhập hệ thống.
* Tra cứu thông tin vé và kiểm tra trạng thái vé.
* Quét/Kiểm tra mã QR vé của khách hàng.
* Thực hiện Check-in vé cho khách vào phòng chiếu.

### 3. Quản trị viên (Admin)
* **Quản lý dữ liệu hệ thống:** Quản lý tài khoản người dùng, phân quyền.
* **Quản lý rạp & phòng:** Thêm/sửa/xóa thông tin rạp chiếu, phòng chiếu và danh sách ghế.
* **Quản lý phim & suất chiếu:** Cập nhật thông tin phim, lên lịch suất chiếu.
* **Quản lý dịch vụ & ưu đãi:** Quản lý danh mục Combo và các chương trình khuyến mãi.
* **Thống kê & Báo cáo:** Xem báo cáo doanh thu và hoạt động vận hành rạp.

---

## 🔄 Quy trình đặt vé cơ bản
```text
Đăng nhập ➔ Chọn Phim ➔ Chọn Suất Chiếu ➔ Chọn Ghế ➔ Giữ Ghế ➔ Chọn Combo ➔ Áp dụng Khuyến Mãi ➔ Thanh Toán ➔ Tạo Vé & QR Code ➔ Check-in tại Rạp

