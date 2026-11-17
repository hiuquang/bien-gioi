# Trò Chơi Biên Giới — trang web riêng

Trang tĩnh, không cần build. Mở `index.html` là chạy.

- `index.html` / `tro-choi-bien-gioi.html` — menu + Đuổi Sói
- `thang-may.html` — Thang Máy 20 Tầng
- `giat-diem.html` — Giật Điểm (chơi một mình hoặc chơi chung)
- `anh/` — hình của Giật Điểm
- `cau-hinh.js` — địa chỉ + khoá CÔNG KHAI của Supabase (để trống thì chỉ chơi một mình)

## Chơi chung chạy thế nào
Supabase lo sảnh (ai ở phòng nào), tài khoản (đăng ký / đăng nhập / quên mật khẩu) và chuyển lời mời nối.
Dữ liệu trận đi thẳng giữa máy chủ phòng và máy khách bằng WebRTC, nên không tốn hạn mức tin nhắn của Supabase.

## Cài Supabase (một lần)
1. Tạo dự án mới ở supabase.com.
2. Settings → API: chép **Project URL** và khoá **anon / publishable** vào `cau-hinh.js`.
3. Authentication → Sign In / Providers → Email: tắt **Confirm email** nếu muốn đăng ký xong chơi được ngay.
4. Authentication → URL Configuration: đặt **Site URL** là địa chỉ trang web, thêm `…/giat-diem.html` vào Redirect URLs
   (đường dẫn "quên mật khẩu" trong email sẽ đưa người ta về đó).
