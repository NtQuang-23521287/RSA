Các chức năng: Mã hóa, Giải mã, Ký văn bản, Xác thực văn bản đã ký 
Luồng hoạt động:
  - Khi mở app, phải generate public key và private key, sau đó lưu 2 key lại
  - Luồng Mã hóa:
    + A chọn 1 file từ máy hoặc nhập text bằng tay, chọn public key của B, mã hóa và lưu lại file cipherText.
  - Luồng Giải mã:
    + B chọn 1 file cipherText từ máy hoặc nhập bằng tay, chọn private key của B, giải mã và lưu lại file plaintext
  - Luồng ký văn bản:
    + A chọn 1 file txt từ máy hoặc nhập text bằng tay, chọn private key của A, ký văn bản và lưu lại file signature. Gửi cho B cả file txt và file .sig
  - Luồng xác thực:
    + B chọn file txt và file signature nhận được từ A, chọn public key của A, verify văn bản, nếu valid => văn bản là của A và không bị sửa đổi. Nếu invalid, văn bản đã bị sửa đổi và không còn giá trị.
