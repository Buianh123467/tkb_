bai tap 4: (sql server)
yêu cầu bài toán:
 - Tạo csdl cho hệ thống TKB (đã nghe giảng, đã xem cách làm)
 - Nguồn dữ liệu: TMS.tnut.edu.vn
 - Tạo các bảng tuỳ ý (3nf)
 - Tạo được query truy vấn ra thông tin gồm 4 cột: họ tên gv, môn dạy, giờ vào lớp, giờ ra.
   trả lời câu hỏi: trong khoảng thời gian từ datetime1 tới datetime2 thì có những gv nào đang bận giảng dạy.

các bước thực hiện:
1. Tạo github repo mới: đặt tên tuỳ ý (có liên quan đến bài tập này)
2. tạo file readme.md, edit online nó:
   paste những ảnh chụp màn hình
   gõ text mô tả cho ảnh đó

Gợi ý:
  sử dung tms => dữ liệu thô => tiền xử lý => dữ liệu như ý (3nf)
  tạo các bảng với struct phù hợp
  insert nhiều rows từ excel vào cửa sổ edit dữ liệu 1 table (quan sát thì sẽ làm đc)
  

deadline: 15/4/2025
Truy cập vào TMS.tnut.edu.vn để lấy dữ liệu, ở đây ta sẽ lấy ví dụ là thời khóa biểu Tuần: 33 (14/04/2025 → 20/04/2025) của lớp K58KTP.K01
Tạo database có tên là TKB, sau đó tiến hành tạo các bảng có tên là GiangVien, Lop, MonHoc, PhongHoc, TietHoc, LichDay
Tạo bảng Giang vien
![Image](https://github.com/user-attachments/assets/65825d9c-43ba-418d-8c26-7075577b1e0d)
Tạo bảng Lop
![Image](https://github.com/user-attachments/assets/a8e4ec78-770c-4a15-86e3-848d2fa6518d)
Tạo bảng PhongHoc
![Image](https://github.com/user-attachments/assets/c9afa03f-32b5-4ebc-8a17-0a0bcdd27731)
Tạo bảng TietHoc
![Image](https://github.com/user-attachments/assets/4bcdd770-3667-469d-8a59-3ac0573167fa)
Tạo bảng Monhoc
![Image](https://github.com/user-attachments/assets/95d619b1-399d-4cc7-b4b1-36d97250cd3e)
Tạo bảng lichDay
![Image](https://github.com/user-attachments/assets/f2cba35b-0950-4e22-81ea-b89264497d3a)
Sau đó tạo mối liên kết giữa các bảng (FK) và tiến hành nhập dữ liệu từ thời khóa biểu Tuần: 33 (14/04/2025 → 20/04/2025) của lớp K58KTP.K01 và bảng thời gian biểu giảng dạy ở trên cho từng bảng.
Khi hoàn thành các bước trên ta có được sơ đồ sau
![Image](https://github.com/user-attachments/assets/fffbc6f0-d8fd-41e7-a3d1-bbd27aff7689)
 Sử dụng DECLARE @datetime1 DATETIME = '2025-04-08 06:30:00';

DECLARE @datetime2 DATETIME = '2025-04-08 09:10:00';

Lấy tất cả các buổi học có thời gian giáo viên đang dậy học.
![Image](https://github.com/user-attachments/assets/66395b46-f0c3-401a-b49c-38097463783b)


