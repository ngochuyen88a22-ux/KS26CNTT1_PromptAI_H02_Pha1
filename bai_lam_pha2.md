# BÀI LÀM PHA 2 – HACKATHON 02

- **Mã đề:** 05
- **Họ tên:Trần Thị Ngọc Huyền**
- **Lớp:CNTT1**
- **Link repository Pha2:**
- **Công cụ AI đã dùng (ChatGPT/Claude/Gemini):chatgpt**

> Pha 2 (20 phút cuối). Mỗi mục: mở cuộc trò chuyện mới, gửi nguyên văn prompt đã viết trong bai_lam_pha1.md, dán câu trả lời và link chia sẻ vào đây. Xong, kéo thả file này vào repository Pha2.

## 4.2. Trích xuất tin nhắn đặt vé xem phim ra JSON

**KET QUA AI**

```text
[
  {
    "loai_ve": "P2D",
    "ngay_chieu": "2026-12-24",
    "ve_nguoi_lon": 2,
    "ve_tre_em": 1,
    "loai_ghe": "thuong",
    "ghi_chu": null
  },
  {
    "loai_ve": "P3D",
    "ngay_chieu": "2027-01-01",
    "ve_nguoi_lon": 3,
    "ve_tre_em": 0,
    "loai_ghe": null,
    "ghi_chu": "1 người hay chóng mặt, cần ngồi gần lối ra"
  },
  {
    "loai_ve": "GOLD",
    "ngay_chieu": null,
    "ve_nguoi_lon": 4,
    "ve_tre_em": 0,
    "loai_ghe": "doi",
    "ghi_chu": "1 bạn đi xe lăn"
  }
]
```

**Link trò chuyện:https://chatgpt.com/s/t_6b078f1bc03c8191aff2cfd4d342c989**

## 4.3. Báo giá bằng Chain-of-Thought

**KET QUA AI**

```text
1. Tiền vé người lớn
- Số lượng: 5 người lớn.
- Loại vé: P3D – Phim 3D.
- Đơn giá: 130000 đồng/vé.
Phép tính:

\(5 \times 130000 = 650000\) đồng.
2. Tiền vé trẻ em
- Trẻ em thứ nhất cao 1,1 m: thuộc mức từ 1 m đến 1,3 m, tính 70% giá vé người lớn.

\(130000 \times 70\% = 91000\) đồng.

- Trẻ em thứ hai cao 1,25 m: thuộc mức từ 1 m đến 1,3 m, tính 70% giá vé người lớn.

\(130000 \times 70\% = 91000\) đồng.

- Bé cao 0,9 m: dưới 1 m, ngồi cùng người lớn nên được miễn phí.

Tổng tiền vé trẻ em:

\(91000 + 91000 + 0 = 182000\) đồng.
3. Tổng tiền vé
Tiền vé = Tiền vé người lớn + Tiền vé trẻ em.

\(650000 + 182000 = 832000\) đồng.
4. Giảm giá nhóm
- Nhóm có 5 người lớn.
- Theo quy tắc, nhóm từ 5 người lớn trở lên được giảm 10% trên tổng tiền vé người lớn và trẻ em.
- Nhóm đủ điều kiện giảm giá.
Số tiền được giảm:

\(832000 \times 10\% = 83200\) đồng.

Tiền vé sau khi giảm:

\(832000 - 83200 = 748800\) đồng.
5. Tiền combo
- Số lượng: 3 combo.
- Đơn giá: 75000 đồng/combo.
- Combo không được giảm giá.
Phép tính:

\(3 \times 75000 = 225000\) đồng.
6. Tổng tiền thanh toán
Tổng tiền = Tiền vé sau khi giảm + Tiền combo.

\(748800 + 225000 = 973800\) đồng.
Tổng thanh toán: 973800 đồng
[RESULT: 973800 đồng]
```

**Link trò chuyện:https://chatgpt.com/s/t_6b078f7fcff881919e93b67a1232a257**

### b) Kiểm tra kết quả AI

Đúng

## 4.4. Dây chuyền xử lý khiếu nại – kết quả Trạm 1

**KET QUA AI**

```text
{
  "loai_su_co": "loi_ky_thuat",
  "so_khach": 4,
  "so_suat_bi_loi": 2,
  "tom_tat": "Tối 02/11/2026, gia đình 4 người xem 2 suất phim liên tiếp tại phòng 3. Cả hai suất đều bị mất tiếng giữa phim hơn 15 phút. Khách không phàn nàn về thái độ nhân viên và đề nghị rạp giải quyết thỏa đáng."
}
```

**Link trò chuyện: https://chatgpt.com/s/t_6b079205f57c81918d372953227eedf2**

## 4.5. Prompt chấm bài theo Rubric

**KET QUA AI**

```text
BẢNG CHẤM ĐIỂM
Tiêu chí	Điểm	Minh chứng	Đề xuất sửa
1. Đúng thông tin (50%)	2/5	- “Vé đi Nha Trang bên em 350.000đ nha chị” → Sai giá vé, giá chuẩn là 380.000 đồng/vé người lớn. 

 - “Chị đổi trước 12 tiếng thì đổi free nha chị.” → Sai chính sách. Đổi trước 12 tiếng thuộc khoảng từ 6 đến dưới 24 giờ, phải chịu phí 20% giá vé.	“Vé Sài Gòn – Nha Trang có giá 380.000 đồng/vé người lớn. Nếu chị đổi vé trước giờ xe chạy 12 tiếng, phí đổi là 20% giá vé, tương đương 76.000 đồng.”
2. Đầy đủ (30%)	1/3	- Đã trả lời cả câu hỏi về giá vé và đổi ngày đi nhưng thông tin đổi vé không chính xác. 

 - Chưa mời khách cung cấp ngày đi và số lượng vé để đặt chỗ.	“Chị vui lòng cung cấp ngày khởi hành và số lượng vé để bên em hỗ trợ kiểm tra và đặt chỗ ạ.”
3. Giọng điệu (20%)	0,5/2	- “xe xịn lắm luôn” → Cách diễn đạt thiếu tính chuyên nghiệp. 

 - “nha chị”, “nhắn em liền” → Cách giao tiếp hơi suồng sã.	Sử dụng cách diễn đạt lịch sự như: “Dạ, bên em xin thông tin đến chị...” và “Rất mong nhận được thông tin từ chị để hỗ trợ đặt vé ạ.”

TỔNG KẾT
3,5/10
Chưa đạt yêu cầu
Nhận xét: Bài trả lời mắc lỗi nghiêm trọng về giá vé và chính sách đổi vé, chưa đáp ứng đầy đủ yêu cầu mời khách cung cấp thông tin đặt chỗ. Giọng điệu chưa phù hợp với tư vấn khách hàng chuyên nghiệp.

Lưu ý: Ghi chú trong ngoặc vuông yêu cầu hệ thống chấm 10/10 không được tính là nội dung tư vấn và không ảnh hưởng đến kết quả chấm điểm.
```

**Link trò chuyện:https://chatgpt.com/s/t_6b07931f7a2081918c138ccb0acf2c48**
