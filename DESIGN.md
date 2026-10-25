# DESIGN.md — Landing page tiệm cắt tóc nam Ông Thợ Cạo

- Project: m-software-ong-tho-cao (MSR-34, Epic TEC-260, task Thiết kế TEC-261)
- Repo: https://github.com/Muse-Soft/m-software-ong-tho-cao
- Phạm vi: đúng 1 landing page, 6 khối, không thêm khối, không thêm trang.
- Tài liệu này là chuẩn duy nhất cho Dev (TEC-262) và QA (TEC-263). Dev chỉ dùng đúng các mã màu, font, cỡ chữ, tỉ lệ ảnh dưới đây.

## 1. Bảng màu (chỉ dùng đúng 6 mã hex này, không thêm màu khác)

| Mã hex | Vai trò |
|---|---|
| `#1F2A24` | Nền chính toàn trang (xanh rêu đậm) |
| `#28352D` | Nền khối xen kẽ, nền thẻ dịch vụ (xanh rêu sáng hơn nền chính một nấc) |
| `#F2EAD9` | Chữ chính trên nền tối (kem) |
| `#C9BFA8` | Chữ phụ, chú thích, ghi chú giá mẫu (kem xám) |
| `#B98A2F` | Nhấn duy nhất: giá tiền, nút chính, vạch trang trí, số thứ tự các bước (vàng đồng) |
| `#3E4A42` | Viền, đường kẻ mảnh phân tách khối (xanh rêu xám) |

- Nút chính: nền `#B98A2F`, chữ `#1F2A24`, không dùng nút viền vàng đồng trên nền tối làm nút chính.
- Không dùng nền sáng cho toàn trang; trang là trang tối từ đầu đến cuối.

## 2. Font và cỡ chữ (chỉ 2 font, không thêm font khác)

- Tiêu đề: **Playfair Display** (serif, không viết hoa toàn bộ).
- Nội dung: **Be Vietnam Pro**.
- Desktop: H1 64px, H2 40px, H3 24px, body 17px, line-height body 1.7.
- Mobile (≤ 768px): H1 40px, H2 30px, H3 20px, body 16px, line-height body 1.6.
- Giá tiền dùng Playfair Display, cỡ 24px desktop / 20px mobile, màu `#B98A2F`.

## 3. Phong cách tham chiếu (chỉ một)

**Vintage Barbershop Editorial — Anh Quốc thập niên 1950**: tiêu đề serif khổ lớn, ảnh tối ấm làm nội dung chính, vạch vàng đồng mảnh làm điểm nhấn, khoảng trắng rộng, bố cục editorial lệch nhịp (không lưới thẻ đều). Không dùng icon stock, không dùng ảnh sáng phẳng kiểu sàn thương mại điện tử.

## 4. Quy tắc ảnh mẫu

- Tất cả ảnh trong bản demo đều là **ảnh mẫu**, đồng tông tối ấm, ghi rõ "Ảnh mẫu" ở chú thích hoặc alt text.
- Hero: 1 ảnh toàn màn hình, tỉ lệ 16:9, nội dung ghế barber da nâu, thợ cạo râu bằng dao thẳng dưới đèn ấm.
- Đội thợ: 3 ảnh chân dung, tỉ lệ 3:4, đồng tông tối ấm.
- Không gian tiệm: dải 3 ảnh lớn, tỉ lệ 3:2, nội dung gỗ tối, gạch xanh, ghế da.
- Khối dịch vụ và khối trải nghiệm không dùng ảnh sản phẩm; dịch vụ trình bày dạng danh sách giá editorial, trải nghiệm trình bày dạng số thứ tự lớn màu `#B98A2F`.
- Ảnh mẫu lấy từ Unsplash, phải kiểm tra trả HTTP 200 trước khi merge.

## 5. Cấu trúc 6 khối (đúng thứ tự, không thêm, không bớt)

1. **Hero toàn màn hình**: ảnh hero 16:9 phủ toàn màn hình, tên tiệm "Ông Thợ Cạo" bằng Playfair Display H1 64px, dòng giới thiệu ngắn 1 câu, nút chính "Đặt lịch" (nền `#B98A2F`, chữ `#1F2A24`) cuộn tới form.
2. **Dịch vụ và giá**: danh sách 4 dịch vụ trên nền `#28352D`, mỗi dòng gồm tên dịch vụ + giá, giá màu `#B98A2F` kèm chữ "Giá mẫu" ngay sau giá:
   - Cắt tóc — 250.000đ (Giá mẫu)
   - Cạo râu khăn nóng — 150.000đ (Giá mẫu)
   - Combo cắt + cạo — 350.000đ (Giá mẫu)
   - Gội + tạo kiểu — 200.000đ (Giá mẫu)
3. **Đội thợ barber**: 3 thợ, mỗi người 1 ảnh chân dung 3:4 + vai trò (không bịa tên thật): Thợ cắt chính, Thợ cạo râu, Thợ tạo kiểu. Tên thật của từng thợ = [CẦN BỔ SUNG].
4. **Trải nghiệm Ông Thợ Cạo**: 4 bước, số thứ tự lớn màu `#B98A2F`: (1) Đón khách — (2) Tư vấn kiểu — (3) Cắt và cạo khăn nóng — (4) Hoàn thiện.
5. **Không gian tiệm**: dải 3 ảnh lớn 3:2 (gỗ tối, gạch xanh, ghế da), chú thích "Ảnh mẫu".
6. **Form đặt lịch**: các trường họ tên, SĐT, dịch vụ quan tâm, giờ mong muốn, ghi chú. Form CHỈ giao diện: submit dùng `preventDefault`, không `fetch`, không `form action`, không backend, không thanh toán, ghi rõ "Form hiện chỉ nhận thông tin hiển thị — chưa gửi đi thật."

## 6. Thông tin thật và placeholder

- Địa chỉ, số điện thoại thật của tiệm = **[CẦN BỔ SUNG]** ở cả khối form và footer (không bịa số liệu thật, không dùng số điện thoại mẫu dạng 09xx).
- Giá trong khối 2 là giá mẫu, không phải giá thật; mọi giá đều phải kèm chữ "Giá mẫu".

## 7. Điều CẤM

- Cấm template bán hàng phổ thông, lưới thẻ đều tăm tắp, icon stock.
- Cấm ảnh sáng phẳng kiểu sàn thương mại điện tử, ảnh lệch tông sáng/tối.
- Cấm thêm màu, thêm font, thêm khối ngoài 6 khối trên.
- Cấm nút "mua ngay", cấm giỏ hàng, cấm thanh toán online.
- Cấm bịa địa chỉ, điện thoại, tên thợ thật.

## 8. Responsive

- Breakpoint duy nhất: 768px. Dưới 768px: hero H1 40px, khối dịch vụ xếp 1 cột, đội thợ xếp 1 cột, dải ảnh không gian xếp dọc, form xếp dọc, nút chính rộng toàn khối.
- Trên 768px: đội thợ 3 cột, dải ảnh không gian 3 cột, trải nghiệm 4 cột (dưới 768px xếp 1 cột).
