# Wallist_Auto
==========================================================================
                HƯỚNG DẪN CÀI ĐẶT VÀ SỬ DỤNG TOOL SLUSH CARD
==========================================================================

1. CÀI ĐẶT THƯ VIỆN (Mở CMD tại thư mục tool và chạy các lệnh sau):
--------------------------------------------------------------------------
npm install 

2. CHUẨN BỊ FILE DỮ LIỆU ĐẦU VÀO:
--------------------------------------------------------------------------
- mail.txt: Định dạng (Email|Mật khẩu Mail|Token API Mail.tm)
  Ví dụ: abc@airsworld.net|pass123|eyJhbGciOiJIUzI1Ni...

- proxy.txt: Định dạng mỗi dòng 1 proxy (HTTP/HTTPS)
  Ví dụ: http://user:pass@123.456.78.9:8080

- user_agents.txt: Mỗi dòng 1 User-Agent trình duyệt
  Ví dụ: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36...

- Config.json: Cấu hình luồng và thời gian nghỉ
  {
    "threads": 5,
    "delay_step_min": 3,
    "delay_step_max": 10,
    "delay_account_min": 30,
    "delay_account_max": 60,
    "start_stagger_min": 3,
    "start_stagger_max": 10
  }

- index.txt: Ghi số 0 (Tool sẽ tự cập nhật vị trí đang chạy tại đây)


3. CÁC FILE ĐẦU RA (TOOL TỰ TẠO):
--------------------------------------------------------------------------
- Sui.txt: Lưu kết quả thành công (PrivateKey|Địa chỉ ví Sui)
- profiles.json: Lưu trạng thái các tài khoản đã hoàn thành để skip lần sau.
- license.txt: Lưu Key bản quyền sau khi nhập lần đầu.


4. CÁCH CHẠY TOOL:
--------------------------------------------------------------------------
Lệnh: node p1.js

Lưu ý: 
- Nếu gặp lỗi Status 429, hãy giảm số luồng (threads) trong Config.json.
- Token Mail.tm phải còn hạn để tool có thể đọc được mã OTP.
==========================================================================
