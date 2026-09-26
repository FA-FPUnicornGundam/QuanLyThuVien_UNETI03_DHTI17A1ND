# QuanLyThuVien_UNETI03_DHTI17A1ND

Bài tập lớn môn **Thực hành lập trình .NET** — Đề tài 02: Xây dựng hệ thống quản lý thư viện và mượn trả sách.

## 1. Giới thiệu

Ứng dụng web quản lý thư viện, hỗ trợ 2 nhóm người dùng:

- **Admin**: quản lý thể loại, sách, độc giả, phiếu mượn, xác nhận mượn/trả, xem thống kê và Dashboard.
- **Độc giả**: đăng nhập, tra cứu sách, đăng ký mượn sách, xem sách đang mượn và lịch sử mượn trả.

## 2. Công nghệ sử dụng

| Thành phần | Công nghệ |
|---|---|
| Nền tảng | .NET 10 SDK |
| Framework Web | ASP.NET Core 10 MVC |
| Ngôn ngữ | C# |
| ORM | Entity Framework Core 10 (Code First) |
| Cơ sở dữ liệu | SQL Server |
| Truy vấn dữ liệu | LINQ |
| Giao diện | Razor View, Tag Helper/HTML Helper, HTML/CSS, JavaScript |
| Quản lý mã nguồn | Git/GitHub |

## 3. Thành viên nhóm & phân công Module

| STT | Họ và tên | Mã sinh viên | Module phụ trách |
|---|---|---|---|
| 1 | | | Module 1 — Tài khoản, Đăng nhập, Phân quyền, Quản lý thể loại |
| 2 | | | Module 2 — Quản lý và tra cứu sách |
| 3 | | | Module 3 — Quản lý độc giả và đăng ký mượn sách |
| 4 | | | Module 4 — Quản lý mượn trả, Dashboard, Thống kê |

## 4. Cấu trúc thư mục

```
QuanLyThuVien_UNETI03_DHTI17A1ND/
├── Controllers/        # Xử lý request, điều phối nghiệp vụ
├── Models/             # Entity, ViewModel
├── Views/               # Giao diện Razor
├── wwwroot/             # CSS, JS, thư viện tĩnh
├── Program.cs           # Cấu hình ứng dụng
├── appsettings.json     # Cấu hình chung (connection string...)
└── .gitignore
```

## 5. Hướng dẫn cài đặt và chạy chương trình

### Yêu cầu môi trường

- [.NET 10 SDK](https://dotnet.microsoft.com/)
- SQL Server (LocalDB hoặc SQL Server Express)
- Visual Studio 2026 hoặc Visual Studio Code

### Các bước thực hiện

1. **Clone repository**
   ```bash
   git clone https://github.com/FA-FPUnicornGundam/QuanLyThuVien_UNETI03_DHTI17A1ND.git
   cd QuanLyThuVien_UNETI03_DHTI17A1ND
   ```

2. **Cấu hình chuỗi kết nối SQL Server**

   Mở `appsettings.json`, chỉnh sửa `ConnectionStrings`:
   ```json
   "ConnectionStrings": {
     "DefaultConnection": "Server=(localdb)\\MSSQLLocalDB;Database=QuanLyThuVienDB;Trusted_Connection=True;MultipleActiveResultSets=true;TrustServerCertificate=True"
   }
   ```

3. **Khôi phục package**
   ```bash
   dotnet restore
   ```

4. **Tạo database từ Migration**
   ```bash
   dotnet ef database update
   ```

5. **Chạy ứng dụng**
   ```bash
   dotnet run
   ```
   Hoặc mở solution bằng Visual Studio và nhấn `F5`.

### Tài khoản mẫu để kiểm tra

| Vai trò | Tên đăng nhập | Mật khẩu |
|---|---|---|
| Admin | admin | (cập nhật sau khi tạo dữ liệu mẫu) |
| Độc giả | docgia01 | (cập nhật sau khi tạo dữ liệu mẫu) |

## 6. Quy tắc làm việc nhóm

- Mỗi thành viên dùng tài khoản GitHub cá nhân để commit/push.
- Commit message theo mẫu: `[Mã SV] [Module] Nội dung công việc`
  Ví dụ: `[22103100001] [Sach] Them chuc nang phan trang`
- Mỗi file mã nguồn ghi rõ Họ tên, Mã sinh viên và nội dung thực hiện ở đầu file.
- Không dồn toàn bộ công việc vào một commit cuối cùng.

## 7. Tài liệu liên quan

- Báo cáo bài tập lớn: *(cập nhật đường dẫn khi hoàn thành)*
- Thiết kế cơ sở dữ liệu: *(cập nhật đường dẫn khi hoàn thành)*
- Bảng phân công công việc chi tiết: *(cập nhật đường dẫn khi hoàn thành)*
