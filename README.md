# Portfolio CV cá nhân - Đinh Đức Anh

## Giới thiệu

Website portfolio/CV cá nhân giới thiệu Đinh Đức Anh với vai trò Frontend Developer. Trang gồm phần giới thiệu, nội dung tổng quan, các mục nổi bật, thông tin liên hệ và điều hướng giữa các phần. Đây là website tĩnh, phù hợp để học tập, làm bài tập và làm nền tảng xây dựng portfolio cá nhân.

## Chức năng

- Hiển thị thông tin giới thiệu và vai trò cá nhân.
- Điều hướng đến các phần Giới thiệu, Tổng quan, Nổi bật và Liên hệ.
- Trình bày các mục nổi bật dưới dạng lưới thẻ.
- Cung cấp liên kết email và các kênh mạng xã hội.
- Bố cục responsive cho màn hình điện thoại, máy tính bảng và máy tính.
- Cuộn mượt đến các phần và có liên kết quay lại đầu trang.

## Công nghệ

- HTML5: cấu trúc nội dung và ngữ nghĩa trang.
- CSS3: giao diện, Flexbox, CSS Grid, biến CSS và media query.
- Nginx (tùy chọn): phục vụ website tĩnh khi chạy bằng Docker.

Không cần cài Node.js, npm hay biên dịch mã nguồn.

## Cấu trúc dự án

```text
CV-1.0/
├── index.html
├── README.md
└── assets/
	├── css/
	│   └── styles.css
	└── img/
		├── images.jfif
		└── okii.jfif
```

## Yêu cầu môi trường

- Trình duyệt hiện đại như Chrome, Firefox, Edge hoặc Safari.
- Để mở trực tiếp: không cần cài thêm môi trường chạy.
- Để chạy máy chủ cục bộ: Python 3 (hoặc một máy chủ HTTP tương đương).
- Để chạy bằng Docker: Docker Engine trên Linux, Docker Desktop trên Windows/macOS.
- Kết nối Internet không bắt buộc để xem trang; các tệp HTML, CSS và hình ảnh được lưu trong dự án.

## Cài đặt

Tải hoặc sao chép mã nguồn về máy, sau đó mở thư mục dự án trong VS Code hoặc trình soạn thảo bất kỳ. Nếu dự án được lấy bằng Git, thay `<URL-repository>` bằng địa chỉ repository thực tế:

```bash
git clone <URL-repository>
cd CV-1.0
```

Nếu đã có thư mục dự án trên máy, chỉ cần mở thư mục đó; không cần cài package.

## Cấu hình và tùy chỉnh

- Nội dung, tiêu đề trang, email và liên kết mạng xã hội: chỉnh trong `index.html`.
- Giao diện, màu sắc, bố cục và điểm responsive: chỉnh trong `assets/css/styles.css`.
- Hình ảnh: đặt ảnh trong `assets/img/` và cập nhật thuộc tính `src` tương ứng trong `index.html`.
- Thông tin liên hệ hiện được khai báo trong HTML. Hãy thay email, hồ sơ GitHub/LinkedIn và các liên kết `#` bằng địa chỉ thực tế trước khi công khai.

**Lưu ý về ảnh:** một số thẻ ảnh trong `index.html` đang tham chiếu đến các tệp `.jpg` không xuất hiện trong cấu trúc dự án hiện tại. Hãy bổ sung đúng các tệp đó hoặc đổi `src` sang ảnh sẵn có để tránh ảnh bị lỗi.

## Chạy thử

### Windows

Mở PowerShell tại thư mục dự án và chạy máy chủ bằng Python Launcher:

```powershell
py -m http.server 8000
```

Mở <http://localhost:8000> trong trình duyệt. Nếu lệnh `py` không có, cài Python 3 hoặc mở trực tiếp `index.html`.

### macOS

Mở Terminal, chuyển đến thư mục dự án rồi chạy:

```bash
cd /duong-dan/toi/CV-1.0
python3 -m http.server 8000
```

Mở <http://localhost:8000>. Dừng máy chủ bằng `Control+C`.

### Linux

Mở Terminal, chuyển đến thư mục dự án rồi chạy:

```bash
cd /duong-dan/toi/CV-1.0
python3 -m http.server 8000
```

Mở <http://localhost:8000>. Dừng máy chủ bằng `Control+C`.

### Mở trực tiếp trên mọi hệ điều hành

Mở tệp `index.html` bằng trình duyệt. Cách này phù hợp để xem nhanh trang; dùng máy chủ HTTP cục bộ nếu trình duyệt hoặc công cụ phát triển yêu cầu truy cập qua HTTP.

## Chạy bằng Docker

Cần khởi động Docker trước. Các lệnh dưới đây dùng Nginx để phục vụ thư mục dự án trên cổng `8080`; không cần tạo image riêng.

**Windows PowerShell** (chạy tại thư mục dự án):

```powershell
docker run --rm -d --name cv-portfolio -p 8080:80 --mount "type=bind,source=$((Get-Location).Path),target=/usr/share/nginx/html,readonly" nginx:alpine
```

**macOS/Linux** (chạy tại thư mục dự án):

```bash
docker run --rm -d --name cv-portfolio -p 8080:80 --mount type=bind,source="$(pwd)",target=/usr/share/nginx/html,readonly nginx:alpine
```

Truy cập <http://localhost:8080>. Dừng container bằng:

```bash
docker stop cv-portfolio
```

Nếu cổng `8080` đang được sử dụng, đổi phần `8080:80` thành một cổng trống khác, ví dụ `8081:80`, rồi truy cập cổng mới.

## Thông tin liên hệ

- **Tên:** Đinh Đức Anh
- **Email:** [dinhducanh34@gmail.com](mailto:dinhducanh34@gmail.com)
- **GitHub:** [github.com/ducanh25](https://github.com/ducanh25)
- **LinkedIn:** [linkedin.com/in/ducanh2501](https://linkedin.com/in/ducanh2501)

> Các liên kết hồ sơ và thông tin liên hệ nên được xác nhận, cập nhật trước khi phát hành website.
