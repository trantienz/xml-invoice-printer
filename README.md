# In hoá đơn hàng loạt

Trang web chạy offline để in cùng lúc nhiều hoá đơn điện tử Việt Nam từ file `.xml`, ví dụ file xuất từ KiotViet. Hoá đơn được trình bày theo trang tra cứu trên [hoadondientu.gdt.gov.vn](https://hoadondientu.gdt.gov.vn).

Toàn bộ công cụ nằm trong một file duy nhất, `in-hoa-don.html`. Không cần cài đặt, không dùng thư viện ngoài và không gửi dữ liệu đi đâu.

## Tính năng

- Đọc mọi file `.xml` nằm ngay trong một thư mục, không đọc thư mục con.
- Hỗ trợ hoá đơn GTGT (mẫu số 1) và hoá đơn bán hàng (mẫu số 2), kể cả hoá đơn khởi tạo từ máy tính tiền.
- Xem trước dạng lưới, phóng to từng hoá đơn.
- Tìm theo người mua, mã số thuế, số hoá đơn (không cần gõ dấu), lọc theo ngày và sắp xếp.
- Tạo mã QR theo định dạng của trang tra cứu GDT.
- Tuỳ chọn co mỗi hoá đơn vừa 1 trang A4.
- Ghi hoá đơn đã in vào `da-in.txt` trong thư mục hoá đơn để tránh in trùng, có nút hoàn tác.

## Cách dùng

1. Tải file `in-hoa-don.html` về máy.
2. Mở file bằng Chrome hoặc Edge trên máy tính.
3. Bấm **Bắt đầu in hoá đơn**, rồi **Chọn thư mục…** và chọn thư mục chứa file `.xml`.
4. Cho phép trang truy cập thư mục khi trình duyệt hỏi.
5. Chọn hoá đơn cần in, rồi bấm **In đã chọn** hoặc **In tất cả**.

Hướng dẫn chi tiết nằm ngay trong trang, ở nút **Hướng dẫn**.

Trên trình duyệt không hỗ trợ ghi file, trang vẫn xem và in được nhưng không lưu `da-in.txt`.

## Giới hạn

- Trang chỉ hiển thị thông tin chữ ký có trong file, không kiểm tra chữ ký số. Dòng "Signature Valid" không có nghĩa là chữ ký đã được xác thực. Hãy tra cứu trên trang GDT khi cần kiểm tra hoá đơn.
- Chế độ co 1 trang sẽ làm chữ nhỏ đi với hoá đơn nhiều dòng.

## Quyền riêng tư

Mọi xử lý diễn ra trong trình duyệt trên máy của bạn. Không đưa file hoá đơn thật hoặc `da-in.txt` lên kho mã, vì chúng chứa thông tin của khách hàng và doanh nghiệp. `.gitignore` đã loại các file này.
