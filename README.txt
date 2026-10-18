LẠI KHÔNG BIẾT ĂN GÌ À? — ỨNG DỤNG HTML

Mở index.html bằng trình duyệt để sử dụng.
Triển khai Netlify: kéo thả tệp ZIP này vào Netlify Drop.
Triển khai GitHub Pages: tải index.html vào thư mục gốc repository, sau đó bật Pages.

CHỨC NĂNG
- Ăn uống: lập kế hoạch, địa điểm, lịch sử, check bill gọi đồ.
- Hóa đơn ăn uống: giảm giá theo món, nhiều dòng thuế/phí dịch vụ (% sau giảm hoặc số tiền cố định), chia bill theo số người.
- Mua sắm: so sánh hàng lẻ, combo nhiều thành phần; giảm giá/thuế tùy chọn trên mỗi mặt hàng; đánh giá giá thực trả; chuyển vào hóa đơn nhanh.
- Sửa tại chỗ từng địa điểm, món ăn, thuế/phí, hàng hóa/ combo và dòng bill.
- Có bộ lọc/tìm kiếm và tạm lưu so sánh.

QUY TẮC TÍNH
- Giá sau giảm cho mỗi đơn vị = giá gốc trừ giảm giá (% giá gốc hoặc số tiền).
- Thuế trên mỗi đơn vị = % của giá sau giảm hoặc số tiền thuế cố định.
- Tổng tiền mua = số lượng × (giá sau giảm + thuế).
- Thuế/phí ăn uống tính độc lập theo % trên tiền món sau giảm hoặc trên cơ sở tính thuế nhập riêng cho từng dịch vụ, hoặc theo tiền cố định cho cả bill.
- Combo gồm nhiều loại hàng khác nhau chỉ so giá trực tiếp khi danh sách mặt hàng và định lượng mỗi combo tương đồng hoàn toàn.
- Nhóm sản phẩm tương đương cùng loại đơn vị được so bằng giá quy đổi trên kg, lít, m, m² hoặc cái.

LƯU TRỮ
Dữ liệu lưu bằng localStorage ở từng trình duyệt / tên miền. Khi thay đổi tên miền hay xóa dữ liệu trình duyệt, dữ liệu sẽ không tự chuyển.
Không có kết nối cơ sở dữ liệu hoặc dữ liệu giá thời gian thực.

NHẬP / XUẤT DỮ LIỆU (PHIÊN BẢN NÀY)
Vào tab "💾 DỮ LIỆU" trên thanh điều hướng chính.
- Nhấn "Xuất toàn bộ dữ liệu (.json)" để sao lưu cả 7 nhóm:
  địa điểm, lịch sử, check bill gọi đồ, thuế/phí ăn uống,
  danh sách check giá/combo, so sánh giá tạm lưu, check bill mua sắm.
- "Xuất CSV nhóm đã chọn" chỉ phục vụ xem hoặc tính toán trong Excel/Sheets.
  CSV không phải tệp để khôi phục, vì không chứa toàn bộ cấu trúc dữ liệu.
- Muốn nhập: chọn file JSON đã được xuất từ ứng dụng, xem số lượng
  từng nhóm rồi chọn GỘP hoặc THAY THẾ TOÀN BỘ và nhấn xác nhận.
- GỘP: giữ các mục hiện có và thêm mục từ sao lưu nếu khác mã ID.
- THAY THẾ: xóa dữ liệu hiện tại trong 7 nhóm và nạp nội dung của tệp.
  NÊN XUẤT BACKUP TRƯỚC KHI THAY THẾ.
- Dữ liệu nhập có bước xác minh định dạng và nội dung; file sai bị từ chối.
- Không tự đồng bộ giữa các máy. Chuyển file JSON sang máy khác và nhập.
- Giữ file JSON an toàn, vì tệp có thể chứa ghi chú và thông tin liên hệ.
