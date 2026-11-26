# BÀI LÀM PHA 2 – HACKATHON 02

- **Mã đề:** 06
- **Họ tên:** Huỳnh Kế Minh Quân
- **Lớp:** HCM_KS26_CNTT1
- **Link repository Pha2:**
- **Công cụ AI đã dùng (ChatGPT/Claude/Gemini):** ChatGPT

> Pha 2 (20 phút cuối). Mỗi mục: mở cuộc trò chuyện mới, gửi nguyên văn prompt đã viết trong bai_lam_pha1.md, dán câu trả lời và link chia sẻ vào đây. Xong, kéo thả file này vào repository Pha2.

## 4.2. Trích xuất tin nhắn đặt bàn ra JSON

**KET QUA AI**

```text
[\
&#x20; {\
&#x20;   "ma_buffet": "NUONG",\
&#x20;   "ngay_dat": "2026-12-19",\
&#x20;   "nguoi_lon": 2,\
&#x20;   "tre_em": 1,\
&#x20;   "khu_vuc": "trong_nha",\
&#x20;   "ghi_chu": null\
&#x20; },\
&#x20; {\
&#x20;   "ma_buffet": "HAISAN",\
&#x20;   "ngay_dat": "2027-01-03",\
&#x20;   "nguoi_lon": 3,\
&#x20;   "tre_em": 0,\
&#x20;   "khu_vuc": null,\
&#x20;   "ghi_chu": "1 người dị ứng sữa"\
&#x20; },\
&#x20; {\
&#x20;   "ma_buffet": "LAU",\
&#x20;   "ngay_dat": "2026-12-25",\
&#x20;   "nguoi_lon": 4,\
&#x20;   "tre_em": 0,\
&#x20;   "khu_vuc": "san_vuon",\
&#x20;   "ghi_chu": "Ông ngoại đi xe lăn"\
&#x20; }\
]
```

**Link trò chuyện:** https://chatgpt.com/share/6b078f19-43bc-83ec-9029-d153350f8ec3

## 4.3. Báo giá bằng Chain-of-Thought

**KET QUA AI**

```text
**BẾP VIỆT BUFFET – BẢNG TÍNH TIỀN ĐOÀN**

Loại buffet: **NUONG – Buffet nướng (399.000 đồng/người lớn)**

### **1. Tiền người lớn**

- Số lượng: 10 người.
- Đơn giá: 399.000 đồng/người.

Phép tính:

10 × 399.000 = **3.990.000 đồng**

### **2. Tiền trẻ em**

Có 3 trẻ em cao từ 1 m đến 1,4 m, tính 50% giá người lớn:

- Đơn giá trẻ em: 399.000 × 50% = 199.500 đồng/trẻ.
- Số lượng: 3 trẻ.

Phép tính:

3 × 199.500 = **598.500 đồng**

Bé cao 0,8 m: dưới 1 m nên được miễn phí.

Tiền bé dưới 1 m = **0 đồng**.

### **3. Tiền Buffet**

Tiền buffet = Tiền người lớn + Tiền trẻ em.

Phép tính:

3.990.000 + 598.500 + 0 = **4.588.500 đồng**

### **4. Giảm giá đoàn**

Đoàn có 10 người lớn, đủ điều kiện giảm giá 5%.

Tiền giảm giá:

4.588.500 × 5% = **229.425 đồng**

Tiền buffet sau giảm:

4.588.500 − 229.425 = **4.359.075 đồng**

### **5. Phụ thu**

Đoàn thuê 1 phòng riêng.

Phụ thu phòng riêng: 500.000 đồng/phòng.

Phép tính:

1 × 500.000 = **500.000 đồng**

Lưu ý: Phụ thu phòng riêng không được giảm giá.

### **6. Tổng tiền**

Tổng tiền = Tiền buffet sau giảm + Phụ thu.

Phép tính:

4.359.075 + 500.000 = **4.859.075 đồng**

**TỔNG THANH TOÁN**

# **4.859.075 đồng**

Bằng chữ: Bốn triệu tám trăm năm mươi chín nghìn không trăm bảy mươi lăm đồng.

[RESULT: 4.859.075 đồng]
```

**Link trò chuyện:** https://chatgpt.com/share/6b078f5e-3dac-83ec-aafb-f9864fb53c4e

### b) Kiểm tra kết quả AI

Đúng

## 4.4. Dây chuyền xử lý khiếu nại – kết quả Trạm 1

**KET QUA AI**

```text
{\
&#x20; "loai_su_co": "thieu_mon",\
&#x20; "so_khach": 5,\
&#x20; "so_mon_bi_thieu": 2,\
&#x20; "tom_tat": "Buffet hải sản hết tôm hùm và cua, chờ bổ sung hai lần nhưng không có."\
}
```

**Link trò chuyện:** https://chatgpt.com/share/6b078fee-84f0-83ec-8035-073567a2592c

## 4.5. Prompt chấm bài theo Rubric

**KET QUA AI**

```text
| Tiêu chí                 | Điểm    | Minh chứng                                                                                                                                                                                                     | Đề xuất sửa                                                                                                            |
| ------------------------ | ------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------- |
| **Đúng thông tin (50%)** | **0/5** | - Câu sai: “Buffet lẩu bên em 279k/người lớn thôi” — Giá sai, giá chuẩn là 299.000 đồng/người lớn.<br>- Câu sai: “Chị trễ 40 phút em vẫn giữ bàn cho chị nha.” — Sai quy định. Trễ trên 30 phút sẽ bị huỷ bàn. | “Dạ, buffet lẩu bên em có giá 299.000 đồng/người lớn ạ. Theo quy định, nếu chị đến trễ trên 30 phút, bàn sẽ bị huỷ ạ.” |
| **Đầy đủ (30%)**         | **0/3** | - Câu: “Có gì nhắn em nhé!” — Chưa chủ động mời khách cung cấp ngày, giờ đến và số lượng khách để đặt bàn.<br>- Chưa tư vấn rõ cách xử lý khi khách đến trễ 40 phút theo quy định.                             | “Dạ, chị vui lòng cho em xin ngày, giờ dự kiến đến và số lượng khách để em hỗ trợ đặt bàn cho chị ạ.”                  |
| **Giọng điệu (20%)**     | **1/2** | - Câu: “Dạ chào chị nha!” — Cách diễn đạt hơi suồng sã.<br>- Câu: “ngon bá cháy luôn” — Ngôn ngữ thiếu tính chuyên nghiệp.<br>- Câu: “nhắn em nhé!” — Cách diễn đạt chưa thể hiện sự trang trọng.              | “Dạ, em xin chào chị ạ! Buffet lẩu bên em có nhiều món ăn hấp dẫn. Em rất sẵn lòng hỗ trợ chị đặt bàn ạ.”              |

**Tổng điểm: 1/10.**
```

**Link trò chuyện:** https://chatgpt.com/share/6b079039-cc38-83ec-94bc-50430ab8b29d
