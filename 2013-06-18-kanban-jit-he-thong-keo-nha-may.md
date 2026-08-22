---
title: "Kanban & Just-in-Time: Nghệ thuật hệ thống kéo (Pull System) trong cung ứng vật tư nhà máy"
date: 2013-06-18 14:00:00 +0700
categories: [logistics, san-xuat]
tags: [Kanban, JIT, Lean, hệ thống kéo, Toyota, WIP]
author: factory_supply_team
---

Trong khi MRP (đã giới thiệu ở [bài trước](/posts/mrp-hoach-dinh-nhu-cau-vat-tu/)) là hệ thống **đẩy (push)** — tính toán trước rồi đẩy vật tư vào sản xuất — thì **Kanban** lại là đại diện tiêu biểu của hệ thống **kéo (pull)**: chỉ sản xuất và cung ứng khi có nhu cầu thực tế. Hai triết lý tưởng tượng như đối lập nhau, nhưng các nhà máy giỏi nhất thế giới lại biết **kết hợp cả hai**.

## Nguồn gốc: Từ siêu thị đến dây chuyền Toyota

Vào cuối thập niên 1940, Taiichi Ohno — kỹ sư công nghiệp của Toyota — nghiên cứu cách vận hành của các **siêu thị Mỹ** và nhận ra một nguyên lý đắt giá:

> Khách hàng chỉ lấy những gì họ cần, vào thời điểm họ cần — không hơn, không less. Và siêu thị chỉ nhập thêm hàng khi kệ sắp trống, vì nguồn cung tương lai được đảm bảo.
{: .prompt-info }

Ohno áp dụng nguyên lý này vào nhà máy: **xem mỗi công đoạn là "khách hàng" của công đoạn trước nó**, và công đoạn trước là "cửa hàng" cung cấp. Khi công đoạn sau tiêu thụ vật tư, một tín hiệu (thẻ Kanban) sẽ kích hoạt công đoạn trước sản xuất bổ sung đúng bằng lượng đã dùng.

Chính từ đây, thuật ngữ *Just-in-Time* (đúng lúc) ra đời — vật tư đến **đúng lúc cần**, không sớm gây tồn kho, không muộn gây dừng chuyền.

## Push vs Pull: Hiểu đúng bản chất

| Tiêu chí | Hệ thống đẩy (Push - MRP) | Hệ thống kéo (Pull - Kanban) |
|----------|--------------------------|------------------------------|
| Tín hiệu | Kế hoạch/dự báo | Tiêu thụ thực tế |
| Sản xuất theo | Lịch trình đã tính sẵn | Đơn hàng/nhu cầu thực |
| Tồn kho WIP | Có thể tích tụ lớn | Bị giới hạn chặt chẽ |
| Phù hợp khi | Nhu cầu ổn định, dự báo tốt | Nhu cầu biến động, lead time dài |
| Rủi ro chính | Dư thừa do dự báo sai | Thiếu hụt nếu tín hiệu chậm |

Điểm mấu chốt theo Ohno: **Kanban dùng tốc độ tiêu thụ thực tế để điều khiển tốc độ sản xuất**, truyền nhu cầu từ khách hàng cuối cùng ngược lên toàn bộ chuỗi cung ứng.

## Sáu quy tắc vàng của Toyota với Kanban

Toyota formulated 6 quy tắc nghiêm ngặt — vi phạm bất kỳ quy tắc nào cũng phá vỡ toàn hệ thống:

1. **Mỗi công đoạn chỉ gửi yêu cầu (kanban) cho nhà cung cấp khi tiêu thụ vật tư của mình**
2. **Mỗi công đoạn sản xuất đúng số lượng và đúng thứ tự** của các yêu cầu nhận được
3. **Không sản xuất hay vận chuyển gì nếu không có yêu cầu**
4. **Thẻ kanban luôn gắn liền với vật tư** mà nó đại diện
5. **Không chuyển giao sản phẩm lỗi** sang công đoạn sau
6. **Giới hạn số yêu cầu đang chờ** — giúp quá trình nhạy cảm hơn và bộc lộ điểm kém hiệu quả

Quy tắc số 6 đặc biệt quan trọng: giới hạn này chính là cơ chế **tự phơi bày vấn đề**. Khi tồn tại vượt giới hạn → có điểm nghẽn → phải xử lý gốc rễ thay vì tăng tồn kho che đậy.

## Thẻ Kanban & Hệ thống hai thùng (Two-Bin System)

### Thẻ Kanban hoạt động thế nào?

Thẻ kanban về bản chất là **một thông điệp báo hiệu sự cạn kiệt** của sản phẩm/phụ tùng/tồn kho. Khi nhận thẻ, hệ thống kích hoạt bổ sung đúng lượng đó:

```text
[Công đoạn lắp ráp] ──lấy hộp vật tư──▶ [Kho/buffer]
        │                                    │
        └──gắn thẻ kanban vào hộp rỗng──────┘
                                             │
[Hộp rỗng + thẻ] ──về công đoạn trước──▶ [Sản xuất bổ sung]
                                             │
[Sản xuất xong + thẻ] ──trả về buffer────────┘
```

Có hai loại thẻ chính:
- **Thẻ thu hồi (Withdrawal/Conveyance kanban)**: cho phép lấy vật tư từ công đoạn trước
- **Thẻ sản xuất (Production kanban)**: cho phép công đoạn trước sản xuất bổ sung

### Two-Bin System — Phiên bản đơn giản nhất

Nguồn gốc xa xưa của kanban là **hệ thống hai thùng** từ các nhà máy Spitfire Anh Quốc thời Thế chiến II:

- **Thùng 1**: đang sử dụng ở dây chuyền
- **Thùng 2**: dự phòng bên cạnh
- Khi Thùng 1 cạn → đưa thùng 1 đi làm đầy → dùng Thùng 2 trong lúc chờ
- Chu kỳ lặp lại vô hạn — đơn giản, trực quan, gần như không thể sai

Hệ thống này vẫn cực kỳ hiệu quả cho **vật tư C giá trị thấp** (ốc vít, vòng đệm...) đến ngày nay.

## Công thức tính số thẻ Kanban

Số lượng thẻ quyết định mức tồn kho trong hệ thống. Công thức kinh điển:

```text
N = D × L × (1 + α) / C

Trong đó:
N = số thẻ kanban
D = nhu cầu trung bình (đơn vị/thời gian)
L = lead time bổ sung (thời gian)
α = hệ số an toàn (%)
C = sức chứa của một container/hộp (đơn vị)
```

### Ví dụ thực tế

Dây chuyền tiêu thụ **200 ốc vít/giờ**, lead time làm đầy hộp là **2 giờ**, hệ số an toàn 10%, mỗi hộp chứa **500 con**:

```text
N = 200 × 2 × (1 + 0.10) / 500 = 0.88 → làm tròn lên 1 thẻ... 
```

Thực tế nên làm tròn lên **2 thẻ** để tạo buffer an toàn. Mỗi thẻ thêm = thêm 500 con tồn kho. Đây là cách kanban **biến tồn kho thành con số hữu hình, kiểm soát được**.

## Giới hạn WIP: Vũ khí chống "bệnh tồn kho"

Một trong những lợi ích lớn nhất của kanban là thiết lập **giới hạn trên cho Work-in-Process inventory**:

- Không bao giờ cho phép tồn đọng vượt mức định sẵn tại bất kỳ điểm cung ứng nào
- Khi giới hạn bị vượt qua → đó là tín hiệu của **sự kém hiệu quả cần xử lý**
- Giảm dần giới hạn theo thời gian → buộc hệ thống liên tục cải tiến

Đây là triết lý khác biệt căn bản so với tư duy truyền thống: **tồn kho không phải đệm an toàn, mà là nơi che giấu vấn đề** (máy hỏng, chất lượng kém, giao hàng chậm). Loại bỏ tồn kho = buộc mọi vấn đề phải lộ diện và được giải quyết.

## Điều kiện để Kanban thành công

Kanban không phải "viên đạn bạc" — nó chỉ hoạt động khi đáp ứng các điều kiện:

1. ✅ **Nhu cầu tương đối ổn định hoặc lặp lại** — kanban khó hoạt động với sản phẩm đơn chiếc
2. ✅ **Lead time nhà cung cấp ngắn và tin cậy** — nếu giao hàng 3 tháng/lần, kanban sẽ gây thiếu hụt
3. ✅ **Chất lượng ổn định** — quy tắc số 5 đòi hỏi không chuyển lỗi; chất lượng kém sẽ dừng toàn chuỗi
4. ✅ **Layout nhà máy hợp lý** — khoảng cách ngắn giữa các công đoạn để luân chuyển thẻ nhanh
5. ✅ **Văn hóa cải tiến liên tục (Kaizen)** — đội ngũ sẵn sàng giải quyết vấn đề khi chúng lộ diện

## Kết hợp MRP + Kanban: Mô hình lai tối ưu

Các nhà máy hiện đại thường dùng mô hình lai:

```text
                    ┌─────────────────────────┐
   MRP (Push)       │  Hoạch định tổng thể     │
   MPS/BOM          │  - Kế hoạch tháng/quý    │
                    │  - Mua nguyên liệu chính │
                    └───────────┬─────────────┘
                                │
                    ┌───────────▼─────────────┐
   Kanban (Pull)    │  Vận hành hàng ngày      │
   Thẻ/Hai-bin      │  - Cung cấp nội bộ       │
                    │  - Vật tư tiêu hao       │
                    │  - Nhà cung cấp gần      │
                    └─────────────────────────┘
```

- **MRP lo tầm nhìn xa**: kế hoạch tổng thể, mua nguyên liệu chính có lead time dài
- **Kanban lo vận hành**: điều phối dòng vật tư hàng ngày trong nhà máy và với nhà cung cấp địa phương

Nhiều doanh nghiệp còn mở rộng pull system ra ngoài qua **Vendor Managed Inventory (VMI)** — mô hình Walmart và P&G tiên phong: nhà cung cấp tự quản lý mức tồn kho tại kho khách hàng dựa trên dữ liệu tiêu thụ chia sẻ qua EDI, giúp giảm đáng kể hiệu ứng bullwhip và chi phí tồn kho chung cho cả hai bên.

## Kết luận

Kanban dạy chúng ta một bài học sâu sắc: **hệ thống cung ứng tốt nhất không phải hệ thống thông minh nhất, mà là hệ thống phản ánh trung thực nhất nhu cầu thực tế**. Bắt đầu nhỏ — chọn một vài vật tư nhóm C áp dụng two-bin, đo lường, cải tiến — rồi mở rộng dần. Đừng quên rằng kanban sinh ra không phải để quản lý tồn kho, mà để **tiêu diệt lãng phí**.

> **Mẹo triển khai**: Chọn 5-10 mã vật tư tiêu hao có nhu cầu ổn định để pilot kanban trong 1 tháng. Đo thời gian chờ, số lần thiếu hàng, mức tồn kho trước/sau. Con số cải thiện thực tế sẽ thuyết phục ban lãnh đạo hơn bất kỳ slide thuyết trình nào.
{: .prompt-tip }