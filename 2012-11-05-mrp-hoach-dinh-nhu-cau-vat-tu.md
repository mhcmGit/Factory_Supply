---
title: "MRP - Hoạch định nhu cầu vật tư: Trái tim của hệ thống cung ứng nhà máy sản xuất"
date: 2012-11-05 09:00:00 +0700
categories: [logistics, hoach-dinh]
tags: [MRP, BOM, hoạch định vật tư, ERP, sản xuất]
author: factory_supply_team
---

**Material Requirements Planning (MRP)** — Hoạch định nhu cầu vật tư — là hệ thống lập kế hoạch, xếp lịch và kiểm soát tồn kho được dùng để quản lý quy trình sản xuất. Ra đời từ những năm 1960 qua công trình của Joseph Orlicky (phản ứng trước chương trình sản xuất Toyota), MRP đến nay vẫn là **nền tảng cốt lõi** của mọi hệ thống ERP sản xuất hiện đại như SAP, Oracle hay Odoo.

## Ba mục tiêu của MRP

Một hệ thống MRP được thiết kế để đồng thời đạt được ba mục tiêu:

1. **Đảm bảo nguyên liệu sẵn sàng** cho sản xuất và thành phẩm sẵn sàng giao cho khách hàng
2. **Duy trì mức tồn kho thấp nhất có thể** đối với nguyên liệu và thành phẩm
3. **Lập kế hoạch hoạt động sản xuất**, lịch giao hàng và hoạt động mua hàng

Điểm mấu chốt: MRP trả lời câu hỏi *"Cần mua gì, mua bao nhiêu, đặt hàng khi nào?"* một cách tự động dựa trên nhu cầu sản xuất thực tế.

## Ba đầu vào của MRP

Hệ thống MRP hoạt động dựa trên ba nguồn dữ liệu đầu vào:

### 1. Master Production Schedule (MPS) — Kế hoạch sản xuất tổng thể

MPS trả lời câu hỏi: *"Chúng ta sẽ sản xuất gì, bao nhiêu, vào lúc nào?"*

| Tuần | Sản phẩm A | Sản phẩm B |
|------|-----------|-----------|
| Tuần 5 | 500 chiếc | 300 chiếc |
| Tuần 6 | 700 chiếc | 300 chiếc |
| Tuần 7 | 600 chiếc | 400 chiếc |

### 2. Bill of Materials (BOM) — Cây cấu trúc sản phẩm

BOM là "công thức" phân rã sản phẩm thành các cấp nguyên liệu. Ví dụ với sản phẩm A:

```text
Sản phẩm A (cấp 0)
├── 2x Thân vỏ nhựa (cấp 1)
│   ├── 50g Nhựa ABS (cấp 2)
│   └── 1x Nắp đậy (cấp 2)
├── 1x Bo mạch điện tử (cấp 1)
│   ├── 8x Tụ điện (cấp 2)
│   └── 1x Vi điều khiển (cấp 2)
└── 4x Ốc vít M3 (cấp 1)
```

Nếu tuần 5 cần 500 sản phẩm A → MRP tự động tính ra cần **1.000 thân vỏ**, **500 bo mạch**, **4.000 ốc vít**, **25kg nhựa ABS**...

### 3. Inventory Records — Hồ sơ tồn kho

Dữ liệu thời gian thực về:
- Tồn kho hiện tại của từng vật tư
- Đơn hàng đã đặt chưa nhận (open orders / scheduled receipts)
- Thời gian dẫn (lead time) của từng vật tư

## Logic tính toán MRP: Từ nhu cầu gộp đến đơn hàng

Quy trình tính toán MRP cho từng vật tư diễn ra theo 4 bước:

```text
Nhu cầu gộp (Gross Requirements)
    ↓ trừ đi tồn kho khả dụng + hàng đang về
Nhu cầu ròng (Net Requirements)
    ↓ nhân với lot size (quy cách đóng gói/mua tối thiểu)
Nhu cầu đặt hàng theo lô (Planned Order Receipts)
    ↓ lùi lại theo lead time
Ngày phát hành đơn hàng (Planned Order Release)
```

### Ví dụ minh họa cụ thể

Vật tư: **Ốc vít M3** — lead time 2 tuần, tồn kho 10.000 cái, đang có 5.000 cái về tuần 3, lot size 5.000.

| Tuần | 1 | 2 | 3 | 4 | 5 |
|------|---|---|---|---|---|
| Nhu cầu gộp | 0 | 12.000 | 8.000 | 15.000 | 10.000 |
| Hàng đang về | 0 | 0 | 5.000 | 0 | 0 |
| Tồn đầu kỳ | 10.000 | 10.000 | -2.000 | -5.000 | -20.000 |
| Tồn cuối kỳ | 10.000 | -2.000 | -5.000 | -20.000 | -30.000 |
| **Nhận hàng kế hoạch** | 0 | 5.000 | 5.000 | 15.000 | 10.000 |
| **Phát hành PO** | **5.000** | **5.000** | **15.000** | **10.000** | — |

👉 Kết luận: Bộ phận mua hàng phải **phát hành PO 5.000 ốc vít ngay tuần này** để kịp nhu cầu tuần 3. Đây chính là giá trị của MRP — biến dữ liệu phức tạp thành hành động cụ thể, đúng thời điểm.

## Các phương pháp xác định kích thước lô (Lot Sizing)

| Phương pháp | Nguyên tắc | Khi nào dùng |
|-------------|-----------|--------------|
| **Lot-for-Lot (L4L)** | Đặt đúng bằng nhu cầu ròng | Vật tư đắt tiền, dễ hỏng |
| **Fixed Order Quantity (FOQ)** | Đặt theo bội số cố định | Quy cách đóng thùng/pallet |
| **EOQ** | Tối ưu chi phí đặt hàng + lưu kho | Nhu cầu ổn định |
| **Period Order Quantity (POQ)** | Gom nhu cầu nhiều tuần thành 1 đơn | Giảm số lần đặt hàng |

## Từ MRP đến MRP II và ERP

Sự tiến hóa của hệ thống hoạch định:

- **1964**: Orlicky phát triển MRP tại J.I. Case, Black & Decker là công ty đầu tiên triển khai
- **1975**: Cuốn sách *Material Requirements Planning* của Orlicky — đến 1975 đã có 700 công ty áp dụng, 1981 tăng lên ~8.000
- **1983**: Oliver Wight mở rộng thành **MRP II** (Manufacturing Resource Planning) — bổ sung lập lịch tổng thể, hoạch định năng lực sơ bộ (RCCP), hoạch định năng lực chi tiết (CRP) và S&OP
- **1990s**: MRP II tiến hóa thành **ERP** — tích hợp tài chính, nhân sự, bán hàng, chuỗi cung ứng

> Theo Computerworld (1986): các công ty hưởng trọn lợi ích từ MRP II có **ROI trung bình 200%** — con số ấn tượng hiếm phần mềm kinh doanh nào đạt được.
{: .prompt-info }

## Những lỗi thường gặp khi triển khai MRP

### 1. Dữ liệu BOM không chính xác

Đây là **lỗi số 1** khiến MRP thất bại. Nếu BOM ghi 4 ốc vít nhưng thực tế dùng 5, toàn bộ kế hoạch sai lệch. Hãy kiểm kê BOM định kỳ và cập nhật ngay khi thay đổi thiết kế (ECN).

### 2. Lead time khai báo "lý tưởng"

Nhiều nhà máy khai lead time theo hợp đồng (7 ngày) nhưng thực tế nhà cung cấp giao chậm (9-10 ngày). Hãy dùng **lead time thực tế trung bình động** thay vì con số trên giấy.

### 3. Tồn kho không khớp thực tế

MRP chỉ tốt bằng dữ liệu tồn kho đưa vào. Nếu hệ thống ghi 10.000 mà kho chỉ còn 8.000, kế hoạch sẽ thiếu hụt. Giải pháp: **đếm vòng quay (cycle counting)** thường xuyên thay vì chỉ kiểm kê năm.

### 4. Quá tin vào con số hệ thống

MRP là công cụ hỗ trợ quyết định, không thay thế con người. Người làm kế hoạch (planner) vẫn phải review exception messages — các cảnh báo như "reschedule in", "reschedule out", "cancel" — trước khi phát hành đơn hàng.

## Kết luận

MRP không phải là phần mềm mua về là chạy, mà là một **quy trình quản lý kỷ luật**: dữ liệu chuẩn (BOM, tồn kho, lead time) + quy trình duyệt đơn rõ ràng + con người hiểu hệ thống. Khi ba yếu tố này hội tụ, MRP trở thành "trái tim" giúp nhà máy luôn đủ nguyên liệu với mức tồn kho tối thiểu — đúng ba mục tiêu mà Orlicky đề ra từ hơn nửa thế kỷ trước.

> **Bài học thực tiễn**: Trước khi đầu tư ERP đắt tiền, hãy đảm bảo BOM của bạn chính xác trên 98% và tồn kho khớp thực tế trên 95%. Không hệ thống nào cứu được dữ liệu bẩn.
{: .prompt-tip }