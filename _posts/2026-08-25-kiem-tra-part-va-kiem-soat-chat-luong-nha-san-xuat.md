---
title: "Kiểm tra part trong xưởng cơ khí: ba lớp kiểm soát và vòng lặp đo – hiệu chỉnh"
date: 2026-08-25 14:00:00 +0700
categories: [quan-ly-chat-luong, san-xuat]
tags: [kiểm tra part, in-process inspection, probing, SPC, go/no-go, lắp ráp, torque marking, đánh dấu QC]
author: factory_supply_team
---

Một chiếc part gia công được bàn giao cho bộ phận QC với đầy đủ kích thước "trong dung sai" — nhưng câu hỏi đầu tiên của một QC kỳ cựu không phải là *"đo lại bao nhiêu lần"*, mà là: **ai đã kiểm, kiểm bằng gì, và kiểm lúc nào?** Vì một part không thể tự tốt; nó tốt nhờ có người (hoặc máy) kiểm nó ở đúng thời điểm, đúng cách. Bài viết này đi vào ba lớp kiểm soát phổ biến trong xưởng cơ khí và vòng lặp *đo – hiệu chỉnh* giúp giữ dung sai mà không phải chạy lại cả lô.

## 1. Ba lớp kiểm soát của một xưởng cơ khí chuẩn

Mọi part gia công — dù đơn giản hay phức tạp — đều đi qua một trong ba lớp kiểm sau, theo thứ tự tăng dần về độ độc lập:

| Lớp | Ai kiểm | Kiểm bằng gì | Thời điểm |
|---|---|---|---|
| **1. Operator check** | Thợ đứng máy | Panme, thước cặp, calibre Go/No-Go | Ngay trên máy hoặc vừa tháo part xuống |
| **2. In-process probing** | Chính máy (tự đo) | Đầu dò probe chạy theo chương trình G-code | Trong chu kỳ gia công |
| **3. Bộ phận QC độc lập** | Nhân viên QC chuyên trách | CMM, máy đo độ nhám, hồ sơ đo | Sau khi part rời tay thợ, theo kế hoạch lấy mẫu |

Vì sao cần tới ba lớp? Vì **một người kiểm công việc do chính mình làm sẽ luôn thấy nó đúng** — một cái lỗ khoan lệch sang phía sai, người khoan lệch thường không bao giờ nhận ra. Lớp QC độc lập tồn tại chính là để phá vỡ "mù" này. Còn lớp probing tự động tồn tại để bắt lỗi ở thời điểm còn nằm trong chu trình máy — là lúc rẻ nhất để sửa.

## 2. Vòng lặp "đo – hiệu chỉnh" giữ dung sai ngay trong quá trình

Một trong những kỹ thuật mạnh nhất của gia công có kiểm soát là **in-process inspection theo vòng lặp kín** (closed-loop), áp dụng khi chạy dung sai hẹp hoặc khi mới phát triển chương trình part:

```text
1. Chỉnh tool offset để chừa một chút phần thừa (excess stock) khi cắt
2. Cho dao gia công phôi
3. Đo kết quả dao vừa cắt (bằng probe hoặc thước)
4. Hiệu chỉnh tool offset dựa trên kết quả đo
5. Chạy lại dao đó
6. Đo xác nhận đã đúng dung sai
```

Vòng lặp này cho phép xưởng vừa chạy vừa "siết" dần về tâm dung sai, thay vì cắt thẳng tới kích thước cuối rồi mới đo — nếu lệch thì phải vứt cả chi tiết. Khi part chạy ổn định rồi, vòng lặp có thể chuyển sang chế độ kiểm định kỳ thay vì từng part.

## 3. Từng lớp trong thực tế nhà xưởng

### Lớp 1 — Thợ đứng máy: bắt lỗi trong 30 giây đầu

Trang bị chuẩn của lớp này là **panme** và **calibre Go/No-Go**. Với lỗ khoan chẳng hạn, đầu "Go" phải lọt vừa khít còn đầu "No-Go" phải không lọt — kiểm tra nhanh, khó lỗi, không cần đọc số. Thợ có kinh nghiệm sẽ đo ngay bộ kích thước chủ lực khi part vừa tháo khỏi máy, vì lúc đó còn kịp sửa dao cho part tiếp theo.

> Quy ước phổ biến trong xưởng: part vừa kiểm xong phải được **đánh dấu trạng thái** ngay (kẻ vạch/dấu tem theo quy ước màu). Nguyên tắc *"no mark, no move"* đã nói kỹ ở [bài đánh dấu QC](/posts/but-danh-dau-qc-rohs-nha-may-co-khi/) chính là nền để lớp 1 hoạt động ăn khớp với lớp 3.
{: .prompt-tip }

### Lớp 2 — In-process probing: "QC không mệt" chạy ngay trong chương trình

Đầu dò probe được gắn trên máy và gọi bằng lệnh G-code trong chính chương trình gia công. Khi chạy, máy tự đo vị trí lỗ, tự xác định kích thước đã cắt và **tự hiệu chỉnh offset** theo vòng lặp đo–hiệu chỉnh ở mục 2. Lợi ích lớn nhất không phải là tiết kiệm công đo — mà là phát hiện sai lệch *trong cùng chu kỳ cắt*, khi chi phí sửa còn tính bằng phút, chưa tính bằng lô.

> Lưu ý cài đặt: đầu dò cũng là một dụng cụ đo, nên phải nằm trong lịch **hiệu chuẩn định kỳ** giống panme và CMM. Probe chưa hiệu chuẩn giống cái thước bị cong — đo rất đều nhưng đều sai.
{: .prompt-info }

### Lớp 3 — Bộ phận QC độc lập: quyết định bằng số, không bằng cảm tính

Sau khi part rời tay thợ, nhân viên QC đo lại theo kế hoạch lấy mẫu. Ở đây **SPC (Statistical Process Control)** quyết định nên kiểm bao nhiêu part và ai chỉ định cần đo gì: nếu quá trình đang ổn định thì giảm cỡ mẫu, nếu có xu hướng lệch thì tăng tần suất. Kết quả đo được ghi vào hồ sơ part (inspection report) — đây là bằng chứng cho khách hàng audit sau này.

## 4. Phần đặc thù: lắp ráp — kiểm tra *sau khi siết* mới là thứ giữ an toàn

Trong dây chuyền lắp ráp cơ khí (đặc biệt ô tô, xe máy), lỗi nguy hiểm nhất thường không nằm ở kích thước part mà nằm ở **độ chặt của kết nối**. Và một công cụ QC kinh điển ở đây là **torque marking**: sau khi bu lông/đai ốc được siết đủ lực bằng máy, người ta kẻ một vạch mực nối liền giữa đầu bu lông và bề mặt chi tiết. Nếu về sau bu lông bị lỏng do rung động, vạch mực sẽ lệch — QC nhìn là bắt lỗi ngay, không cần đem dây chuyền ra đo.

Để vạch torque marking tồn tại đúng mục đích, mực đánh dấu trong môi trường này phải:

- **Bám tốt trên bề mặt có dầu máy / mỡ bôi trơn**, không tự trôi;
- **Chịu nhiệt và rung động** của động cơ, không phai theo thời gian;
- **Không ăn mòn kim loại** (low corrosion, không chứa halogen) — nếu không vạch mực chính là nơi bắt đầu rỉ sét.

Ở góc độ vật tư, đây là lý do các xưởng lắp ráp thường chuẩn hoá dùng **bút marker công nghiệp và mực đóng dấu chuyên dụng** thay vì bút văn phòng thường: mực công nghiệp gốc dầu (như dòng **TAT** của hãng Shachihata) được thiết kế bám dính trên kim loại bóng và chịu nhiệt cao; còn bút **Artline Paint Marker** có độ che phủ tốt để vạch nổi bật trên nền sắt thép tối màu. Tại Việt Nam, loại vật tư này được phân phối chính hãng qua **Công ty Phúc Mã** — đơn vị đại diện độc quyền Shachihata từ 2004 — nơi có thể yêu cầu đủ bộ hồ sơ môi trường (RoHS, SDS, dữ liệu khai báo IMDS cho ngành ô tô) mà một cửa hàng văn phòng phẩm thông thường không thể cung cấp.

## 5. Kiểm *khi nào*: lịch kiểm tối thiểu cho một part chạy loạt

Ai kiểm và kiểm bằng gì rất quan trọng, nhưng lịch kiểm cũng không kém. Mức tối thiểu mà hầu hết xưởng cơ khí và nhà máy lắp ráp áp dụng:

| Thời điểm | Việc cần làm |
|---|---|
| **Trước khi chạy loạt** | FAI — đo chi tiết đầu tiên, lập biên bản |
| **Part đầu mỗi ca / sau khi thay dao** | First-piece check: đo các kích thước chủ lực |
| **Định kỳ trong ca** | Kiểm tuần theo chu kỳ ghi trong Control Plan |
| **Cuối ca** | Rà part cuối, đối chiếu biểu đồ kiểm soát |
| **Trước khi giao** | Kiểm cuối (100% ngoại quan hoặc AQL), bao bì, seal lô |

Lịch này nên được viết thành bảng treo ngay tại máy để ai cũng đọc được — thay vì nằm im trong tập quy trình trên kệ.

## 6. Checklist tối thiểu để không bỏ sót khâu kiểm

- [ ] Mỗi part khi rời máy đều có trạng thái đánh dấu rõ ràng (*no mark, no move*)
- [ ] Panme/calibre Go-No-Go còn hạn hiệu chuẩn, đủ độ phân giải so với dung sai
- [ ] Đầu dò probe trong chương trình gia công nằm trong lịch hiệu chuẩn định kỳ
- [ ] Lịch kiểm tuần + biểu đồ kiểm soát được cập nhật thực sự, không phải để trang trí
- [ ] Torque marking có quy ước rõ: màu nào cho công đoạn nào, ai vạch, ai kiểm
- [ ] Bút/mực đánh dấu nằm trong Approved List, có RoHS/SDS kèm lô hàng
- [ ] Phiếu kiểm (inspection report) lưu theo mã lô, đủ cho khách hàng audit truy vết

## Kết luận

Một xưởng cơ khí giữ được dung sai không phải nhờ dụng cụ đo đắt tiền, mà nhờ **ba lớp kiểm hoạt động ăn khớp**: thợ bắt lỗi ngay tại máy, máy tự hiệu chỉnh trong chu kỳ cắt, và bộ phận QC độc lập ghi hồ sơ bằng số liệu. Kiểm tra là khoản đầu tư rẻ nhất khi được làm đúng thời điểm — và đắt nhất khi bị bỏ qua đến lúc giao hàng.

> **Việc nên làm tuần này**: chọn một trạm đang chạy dung sai hẹp và tự hỏi ba câu — *ai kiểm khi part còn trên máy? ai kiểm sau khi part rời máy? kết quả kiểm có thành hồ sơ để audit không?* Câu nào chưa trả lời được là câu cần ưu tiên xử lý.
{: .prompt-tip }