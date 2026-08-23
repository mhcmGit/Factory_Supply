---
title: "Bút đánh dấu QC trong nhà máy cơ khí: Từ quy trình kiểm tra part đến vì sao bắt buộc dùng bút đạt RoHS (Artline, Uni)"
date: 2025-01-30 16:00:00 +0700
categories: [quan-ly-chat-luong, chuoi-cung-ung]
tags: [QC, đánh dấu part, bút marker, RoHS, Artline, Uni, kiểm tra chất lượng, nhà máy cơ khí, an toàn lao động]
author: factory_supply_team
---

Trong một nhà máy gia công cơ khí sản xuất hàng chục nghìn part mỗi ngày, có một công cụ nhỏ mà nếu thiếu, toàn bộ hệ thống chất lượng sụp đổ ngay: **bút đánh dấu**. Part nào đã qua kiểm tra kích thước? Part nào bị lỗi cần cách ly? Lô nào đã qua tẩy dầu trước khi sơn? Tất cả câu trả lời nằm trên những vệt mực nhỏ trên bề mặt metal.

Nhưng ít người biết rằng: **loại bút marker công nhân cầm mỗi ngày 8 tiếng cũng là một "vật tư nguy hiểm tiềm ẩn"** nếu không đạt RoHS — mực chứa chì, cadmium hay dung môi xylene có thể ảnh hưởng sức khỏe người lao động và khiến lô hàng bị khách hàng EU/Nhật từ chối nhận.

Bài viết này đi sâu vào hai mặt của vấn đề: **(1) hệ thống đánh dấu trong quy trình kiểm định cơ khí** và **(2) tiêu chuẩn chọn bút marker đạt RoHS** từ góc nhìn chuyên gia QC.

## 1. Vai trò của đánh dấu trong chuỗi kiểm định sản xuất cơ khí

### Quy trình kiểm định chuẩn của một part cơ khí

Một part điển hình (bracket, vỏ máy, trục, chi tiết dập) đi qua các trạm kiểm soát sau:

| Trạm | Tên gọi | Nội dung kiểm | Đánh dấu sau kiểm |
|------|---------|---------------|-------------------|
| 1 | **IQC** (Incoming Quality Control) | Kiểm nguyên liệu/nhập kho: chứng chỉ CQ, thử hóa học, đo kích thước phôi | Dấu tem xanh / ghi mã lô |
| 2 | **IPQC - First Article** (FAI) | Kiểm mẫu đầu lô trước khi chạy hàng loạt | Dấu "FAI PASS" + chữ ký QC |
| 3 | **IPQC - Patrol** (kiểm tuần) | Kiểm định kỳ 1-2 giờ/lần trên chuyền | Đánh dấu thời điểm kiểm trên khay/fixture |
| 4 | **FQC** (Final Quality Control) | Kiểm 100% hoặc AQL sampling trước đóng gói | Tem PASS / dấu OK trên part |
| 5 | **OQC** (Outgoing Quality Control) | Kiểm trước giao hàng: số lượng, bao bì, nhãn | Seal lô + phiếu kiểm |

Tại mỗi trạm, **đánh dấu chính là "chữ ký" xác nhận part đã qua cửa chất lượng**. Không có đánh dấu → không thể chứng minh part đã được kiểm → theo nguyên tắc ISO 9001 về traceability, cả lô phải bị nghi ngờ.

### Ba loại thông tin bắt buộc phải "ghi lên" part

1. **Trạng thái chất lượng**: OK / NG / Pending (chờ quyết định MRB)
2. **Nguồn gốc**: mã lô, ngày sản xuất, máy/tuyến, ca làm việc — phục vụ truy vết ngược khi có khiếu nại
3. **Công đoạn tiếp theo**: đã tẩy dầu chưa? đã qua xử lý nhiệt chưa? được phép sơn chưa?

## 2. Hệ thống màu sắc và ký hiệu: Ngôn ngữ chung của xưởng

Các nhà máy world-class chuẩn hóa đánh dấu bằng **quy ước màu thống nhất**, giúp bất kỳ ai nhìn vào cũng hiểu trạng thái part trong 2 giây:

| Màu | Ý nghĩa | Ví dụ sử dụng |
|-----|---------|---------------|
| 🟢 Xanh lá | Đã kiểm, đạt (PASS) | Chấm/dấu xanh trên part qua FQC |
| 🔴 Đỏ | Lỗi, cách ly (NG/Hold) | Xanh đỏ vòng quanh part lỗi, chuyển red bin |
| 🟡 Vàng | Chờ xử lý / concession (dùng có điều kiện) | Chờ MRB (Material Review Board) quyết định |
| ⚪ Trắng/Ghi | Đã tẩy sạch, sẵn sàng sơn | Xác nhận qua pre-treatment |
| 🔵 Xanh dương | Thông tin kỹ thuật bổ trợ | Ghi số bản vẽ rev., vị trí lắp |

**Red Bin System**: mọi part đánh dấu đỏ phải vào thùng cách ly khóa — không ai được lấy ra sử dụng nếu không có giấy NCR (Non-Conformance Report) và quyết định disposition (scrap / rework / re-inspect / use-as-is).

> 💡 **Nguyên tắc vàng của đánh dấu QC**: *"Không có dấu = chưa kiểm = không được di chuyển"* (No mark, no move). Quy tắc này đơn giản nhưng ngăn được 90% sự cố part chưa kiểm lọt sang công đoạn sau.
{: .prompt-tip }

## 3. Vì sao đánh dấu phải là "tạm thời"? Bài học từ dây chuyền sơn

Đây là điểm nhiều nhà máy Việt Nam trả giá đắt mới hiểu: **part cơ khí hầu hết sẽ qua công đoạn làm sạch (degreasing/phosphating) rồi sơn tĩnh điện hoặc sơn lỏng**. Nếu mực đánh dấu:

- **Không tẩy được bằng degreaser thông thường** → vệt mực lộ ra dưới lớp sơn → lỗi thẩm mỹ, bong sơn tại chỗ mực → claim từ khách hàng
- **Chứa silicone hoặc wax** → gây **lỗ kim (fish eyes/craters)** trên bề mặt sơn — lỗi khó sửa nhất trong sơn công nghiệp
- **Ăn mòn bề mặt thép** (mực axit, chloride cao) → gỉ mốc tại chỗ đánh dấu sau vài tuần

Do đó, tiêu chuẩn chọn bút đánh dấu cho part trước sơn gồm 4 điều kiện:

```text
1. Mực oil-based/không silicone — không gây fish eye khi sơn
2. Tẩy sạch hoàn toàn bằng degreaser/alkaline cleaner chuẩn dây chuyền
3. Không ăn mòn, không để lại "bóng ma" (ghosting) trên bề mặt kim loại
4. Chịu được môi trường xưởng: dầu cắt, độ ẩm, nhiệt độ xử lý nhiệt (nếu đánh dấu trước nhiệt luyện)
```

Bút marker công nghiệp chuyên dụng như **Artline EK series (Shachihata)** hay **Uni PX series (Mitsubishi Pencil)** được thiết kế đúng cho mục đích này: mực bám chắc khi viết, chịu dầu mỡ, nhưng vẫn removable trong quá trình pre-treatment.

## 4. RoHS và sức khỏe công nhân: Vì sao "con bút rẻ" lại đắt?

### RoHS là gì?

**RoHS (Restriction of Hazardous Substances)** — Directive 2011/65/EU của EU (và các phiên bản mở rộng) hạn chế 10 chất độc hại trong sản phẩm điện tử và vật liệu liên quan:

| Chất | Giới hạn | Nguy hại sức khỏe |
|------|----------|-------------------|
| Chì (Pb) | ≤ 0.1% (1000 ppm) | Tổn thương thần kinh, thận; đặc biệt hại phụ nữ mang thai |
| Cadmium (Cd) | ≤ 0.01% (100 ppm) | Gây ung thư, tổn thương thận, loãng xương |
| Mercury (Hg) | ≤ 0.1% | Tổn thương hệ thần kinh trung ương |
| Chromium VI (Cr6+) | ≤ 0.1% | Gây ung thư, dị ứng da nghiêm trọng |
| PBB, PBDE | ≤ 0.1% | Chất chống cháy bromine — rối loạn nội tiết |
| Phthalates (DEHP, BBP, DBP, DIBP) | ≤ 0.1% | Rối loạn nội tiết, hại sinh sản |

### Hai lý do bắt buộc dùng bút đạt RoHS trong nhà máy

#### Lý do 1: Sức khỏe người lao động — rủi ro nghề nghiệp âm thầm

Công nhân QC cầm bút đánh dấu **hàng trăm lần mỗi ca**, tiếp xúc trực tiếp qua da với mực và hít hơi dung môi trong môi trường xưởng kín. Bút trôi nổi giá rẻ không kiểm soát thường chứa:

- **Dung môi aromatic (xylene, toluene)**: gây đau đầu, chóng mặt, tổn thương gan/thần kinh khi phơi nhiễm lâu dài
- **Kim loại nặng trong pigment** (một số mực đỏ/chấm chứa cadmium, chì): hấp thu qua da trầy xước
- **Formaldehyde và chất bảo quản**: gây dị ứng da nghề nghiệp

Theo nguyên tắc an toàn vệ sinh lao động, đây là **phơi nhiễm hóa chất thường xuyên, tích lũy** — loại rủi ro nguy hiểm nhất vì không thấy ngay hậu quả. Nhà máy có trách nhiệm pháp lý theo Bộ luật Lao động và Nghị định an toàn hóa chất phải kiểm soát nguồn phơi nhiễm này.

#### Lý do 2: Yêu cầu khách hàng và tính hợp lệ của lô hàng

Với nhà máy cung cấp part cho ngành điện tử, ô tô, thiết bị y tế — khách hàng (đặc biệt Nhật Bản, EU) yêu cầu **toàn bộ vật tư tiếp xúc sản phẩm phải có hồ sơ RoHS/REACH**, kể cả bút đánh dấu dùng trong quá trình (mực có thể lan truyền qua tiếp xúc bề mặt). Khi audit khách hàng hỏi: *"Cho tôi xem SDS và báo cáo RoHS của bút anh đang dùng?"* — không trả lời được nghĩa là **major non-conformance**.

### Cách xác minh bút thật sự đạt RoHS — tránh hàng fake

Thị trường Việt Nam đầy bút giả thương hiệu với chất lượng mực không kiểm soát. Checklist xác minh:

1. ✅ **Yêu cầu SDS (Safety Data Sheet)** từ nhà phân phối chính hãng — tài liệu bắt buộc, cập nhật theo GHS
2. ✅ **Báo cáo kiểm nghiệm RoHS từ phòng lab bên thứ ba** (SGS, Intertek, TÜV) trên mã bút cụ thể — không chấp nhận "tờ cam kết tự khai" không có số test report
3. ✅ **COA/CQ (Certificate of Analysis/Quality)** kèm từng lô hàng nhập
4. ✅ **Mua qua nhà phân phối độc quyền chính hãng** — ví dụ tại Việt Nam, Shachihata (Artline) có hệ thống phân phối độc quyền với đầy đủ chứng từ; mua qua kênh trôi nổi thì không thể đối chứng nguồn gốc
5. ✅ **Kiểm tra bao bì**: mã vạch, số lot, địa chỉ nhà sản xuất, logo in sắc nét — hàng giả thường sai sót ở packaging

> 💡 **Quy tắc mua sắm QC tools**: Bút marker là vật tư "giá trị thấp — rủi ro cao". Đừng đấu thầu chỉ theo giá. Hãy thêm vào tiêu chí đánh giá NCC: *SDS + RoHS test report + kênh phân phối chính hãng*. Chênh 2.000 đồng/chiếc không đáng đổi lấy rủi ro sức khỏe 200 công nhân và lô hàng bị reject.
{: .prompt-tip }

## 5. Triển khai SOP đánh dấu QC chuẩn — checklist thực hành

Để hệ thống đánh dấu vận hành hiệu quả, nhà máy cần một SOP (Standard Operating Procedure) tối thiểu gồm:

### A. Quy ước đánh dấu (Marking Convention)

- [ ] Bảng quy ước màu in tại mỗi trạm kiểm (như bảng ở mục 2)
- [ ] Quy định rõ: viết ở đâu trên part (vị trí không ảnh hưởng gia công/sơn), viết gì (mã lô, ngày, chữ ký tắt)
- [ ] Part nhỏ không đủ chỗ viết → dùng tag/túi zip kèm phiếu

### B. Quản lý vật tư đánh dấu

- [ ] Danh mục bút/dấu được duyệt (Approved List) — chỉ dùng bút trong danh sách, có SDS + RoHS report
- [ ] Bút lưu kho có kiểm soát hạn dùng (mực khô giảm độ bám)
- [ ] Cấp phát theo ca, thu hồi kiểm đếm — tránh bút lạ trôi vào xưởng

### C. Đào tạo & audit

- [ ] Đào tạo onboarding cho mọi công nhân QC về quy ước màu và kỹ thuật viết (không viết đè lên mặt gia công tinh)
- [ ] Audit nội bộ hàng tháng: lấy mẫu 20 part tại mỗi trạm, đối chiếu dấu với hồ sơ kiểm tra
- [ ] KPI: tỷ lệ part thiếu dấu (< 0.5%), tỷ lệ lỗi sơn do mực (target: 0)

### D. Xử lý sự cố điển hình

| Sự cố | Nguyên nhân thường gặp | Hành động |
|-------|----------------------|-----------|
| Sơn bị fish eye | Mực chứa silicone/wax | Dừng dùng bút đó, kiểm tra lại Approved List, tẩy lại lô part |
| Mực không tẩy sạch | Sai loại bút (permanent không phù hợp) | Rà soát degreaser concentration, đổi bút removable |
| Part gỉ tại chỗ đánh dấu | Mực chứa chloride/axit | Đổi bút, thêm bước rinse |
| Part không dấu lọt sang công đoạn sau | Thiếu kỷ luật "no mark no move" | Audit + đào tạo lại, treo visual management |

## 6. Kết luận: Con bút nhỏ, bài toán lớn

Đánh dấu QC tưởng là chuyện nhỏ trong nhà máy cơ khí, nhưng nó chạm vào ba trụ cột cùng lúc:

1. **Chất lượng**: traceability và "no mark, no move" là xương sống của hệ thống ISO 9001/IATF 16949
2. **Sản xuất**: mực đúng loại quyết định thành công của công đoạn sơn phía sau — một con bút sai có thể phá hỏng cả lô part đã hoàn thiện
3. **Con người & tuân thủ**: bút đạt RoHS với SDS đầy đủ bảo vệ sức khỏe công nhân và giữ vững tư cách nhà cung cấp trước audit khách hàng quốc tế

Chi phí để làm đúng điều này rất nhỏ — vài triệu đồng chênh lệch giữa bút chính hãng đạt chuẩn và bút trôi nổi cho cả năm. Nhưng cái giá của việc làm sai: lô hàng bị reject, mất điểm audit, và sức khỏe của những người lao động mỗi ngày cầm bút trên tay.

> **Việc nên làm tuần này**: Kiểm tra ngay cây bút đang dùng tại trạm QC của bạn — hỏi nhà cung cấp 3 câu: *"Có SDS không? Có báo cáo RoHS test từ lab thứ ba không? Anh là kênh phân phối chính hãng hay không?"* Nếu thiếu bất kỳ câu trả lời nào, đã đến lúc thay đổi.
{: .prompt-tip }