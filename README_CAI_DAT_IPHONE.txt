SHADOWING 中文 5.6 – GÓI CÀI TRÊN IPHONE / PWA

VÌ SAO FILE HTML MỞ THÀNH BẢN XEM TRƯỚC?
Trên iPhone, khi chạm file .html trong ứng dụng Tệp hoặc trình tải xuống, iOS có thể mở Quick Look/bản xem trước thay vì chạy file như một website. Đây không phải lỗi riêng của nội dung Shadowing. Cách ổn định là đưa bộ này lên một địa chỉ HTTPS.

CÁCH TRIỂN KHAI DỄ NHẤT: CLOUDFLARE PAGES (CẦN MỘT LẦN TRÊN MÁY TÍNH)
1. Giải nén ZIP này. Bên trong phải thấy index.html ở thư mục gốc, cùng manifest.webmanifest, sw.js và thư mục icons.
2. Trên máy tính, đăng nhập Cloudflare Dashboard.
3. Mở Workers & Pages → Create application → Pages → Direct Upload / Drag and drop.
4. Đặt tên dự án, ví dụ shadowing-cn-study.
5. Kéo thả thư mục đã giải nén (hoặc ZIP này, theo giao diện Direct Upload) và chọn Deploy site.
6. Cloudflare cấp địa chỉ dạng https://TEN-DU-AN.pages.dev. Mở địa chỉ đó để kiểm tra.

CÀI TRÊN IPHONE
1. Gửi địa chỉ HTTPS vừa tạo sang iPhone.
2. Mở địa chỉ bằng Safari (khuyến nghị khi cài PWA).
3. Nhấn Share → Add to Home Screen.
4. Bật “Open as Web App” nếu iOS hiển thị tùy chọn, rồi nhấn Add.
5. Từ nay mở biểu tượng Shadowing 中文 ngoài màn hình chính. Anh vẫn có thể mở cùng địa chỉ HTTPS bằng Cốc Cốc.

LƯU Ý QUAN TRỌNG
- Không thể biến file HTML cục bộ thành ứng dụng chạy ổn định bên trong iOS Quick Look chỉ bằng cách sửa file. Phải dùng địa chỉ HTTPS để tránh chế độ xem trước.
- Gói này thêm manifest, biểu tượng iPhone và service worker để cache vỏ ứng dụng. Lần đầu phải online; các yêu cầu dịch, Pinyin từ CDN và Cloud vẫn cần Internet.
- Dữ liệu lưu cục bộ trong trình duyệt không tự chuyển sang trình duyệt khác. Hãy dùng chức năng sao lưu/khôi phục hiện có hoặc cấu hình Cloud riêng nếu muốn đồng bộ thiết bị.
- Gói này không tự tạo tài khoản Cloudflare và không tự xuất bản website; chủ tài khoản phải tự đăng nhập và triển khai.

CẤU TRÚC
index.html                 Ứng dụng Shadowing 5.6
manifest.webmanifest       Cấu hình cài như ứng dụng
sw.js                      Cache giao diện và hỗ trợ mở offline sau lần truy cập đầu
icons/                     Biểu tượng ứng dụng
