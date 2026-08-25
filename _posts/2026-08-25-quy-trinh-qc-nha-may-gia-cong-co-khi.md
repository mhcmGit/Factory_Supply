---
title: "Quy trình QC trong nhà máy gia công cơ khí: 5 cửa kiểm soát từ phôi đến xuất xưởng"
date: 2026-08-25 09:00:00 +0700
categories: [quan-ly-chat-luong, san-xuat]
tags: [QC, gia công cơ khí, CNC, FAI, IQC, in-process inspection, kiểm tra chất lượng, đánh dấu QC]
author: factory_supply_team
---

Trong một nhà máy gia công cơ khí, một chi tiết được xem là "đạt" khi nó **nằm gọn trong dung sai thiết kế ở mọi cửa kiểm** — từ phôi cắt đầu vào cho đến lúc đóng kiện giao khách. Khác với lắp ráp, lỗi trong gia công thường **không thể nhìn thấy bằng mắt** mà phải do dụng cụ đo có độ phân giải micromet bắt ra, và nếu không chặn được ở cửa này thì nó đi xuyên qua cả sơn, mạ, lắp ráp phía sau. Vì vậy QC trong gia công cơ khí thực chất là một **chuỗi cửa kiểm soát** được thiết kế sẵn từ trước, không phải cuối line kiểm một lần cho xong.

## 1. Ba thông số QC cốt lõi của một chi tiết gia công

Trước khi vào chi tiết từng cửa, cần nắm rõ QC trong gia công đang "nhìn" vào ba nhóm thông số nào:

| Nhóm thông số | Kiểm trên cái gì | Dụng cụ đặc trưng |
|---|---|---|
| **Kích thước & dung sai** | Đường kính, chiều dài, vị trí lỗ, độ đồng tâm so với bản vẽ | Thước cặp, panme, calibre, máy đo CMM |
| **Độ cứng & độ bền vật liệu** | Phôi có đúng mác thép/nhôm, có đủ cứng cho ứng dụng chịu lực | Máy đo độ cứng, thử kéo, kiểm tra chứng chỉ CQ |
| **Độ nhám & chất lượng bề mặt** | Bề mặt sau gia công có sạch, hết vết dao, đúng Ra yêu cầu | Máy đo độ nhám bề mặt, so sánh mẫu |

Quy ước vàng: **nếu bản vẽ không ghi dung sai riêng**, nhiều nhà máy áp dung sai tổng ±0,1 mm theo tiêu chuẩn chung. Nhưng khi khách hàng ghi dung sai ±0,002 inch (≈ ±0,05 mm) cho một lỗ xác định — thì cửa kiểm cho thông số đó phải là dụng cụ có độ chính xác cao hơn dung sai đó ít nhất 10 lần. Dụng cụ không đủ độ phân giải đồng nghĩa với việc cửa kiểm đang "mở toang".

## 2. Bản đồ 5 cửa kiểm soát của một part điển hình

Một chi tiết gia công điển hình (trục, vỏ máy, bracket, chi tiết dập) thường đi qua **5 cửa kiểm soát** trước khi được coi là hoàn chỉnh:

| Cửa | Tên gọi | Kiểm cái gì | Quyết định điển hình |
|---|---|---|---|
| 1 | **IQC — Kiểm đầu vào** | Phôi, nguyên liệu: chứng chỉ CQ, mác vật liệu, kích thước phôi | OK / trả NCC |
| 2 | **FAI — Kiểm mẫu đầu lô** | Chi tiết ĐẦU TIÊN sau khi cài đặt máy: toàn bộ thông số quan trọng | FAI PASS mới chạy loạt |
| 3 | **In-process — Kiểm trong quá trình** | Kiểm tuần trên chuyền: kích thước, độ nhám theo chu kỳ | Điều chỉnh máy / cách ly lô lỗi |
| 4 | **Assembly & Fit-up** | Lắp thử với chi tiết ghép: độ khớp, căn chỉnh, độ đồng tâm | Sửa / gia công lại / chấp nhận |
| 5 | **Final & OQC — Kiểm cuối / xuất xưởng** | 100% hoặc lấy mẫu AQL trước đóng gói, bao bì, nhãn | PASS / giữ lô |

Ba cửa 1–2–3 đều nằm *trước khi* chi tiết được phép "đi tiếp" — đây chính là nguyên tắc đã nói ở [bài về đánh dấu QC](/posts/but-danh-dau-qc-rohs-nha-may-co-khi/): *"không có dấu = chưa kiểm = không được di chuyển"*.

## 3. Đi sâu từng cửa: kiểm gì, bằng gì, bắt buộc ghi gì

### Cửa 1 — IQC: phôi sai thì gia công giỏi cũng thành vô nghĩa

Đây là cửa ít được chú ý nhất nhưng lại quyết định phần lớn kết quả. Với phôi kim loại, bộ phận IQC đối chiếu **chứng chỉ CQ** (mác thép/nhôm, mẻ luyện, kết quả phân tích hóa) và đo lại kích thước phôi theo tiêu chuẩn nhập kho. Một số nhà máy làm thêm thử độ cứng trên mẫu đại diện — vì mác vật liệu "trên giấy" đôi khi không khớp thực tế.

**Hồ sơ bắt buộc sau kiểm:** dấu/tem xác nhận + mã lô nhập — để sau này truy vết ngược khi khách hàng khiếu nại. Nếu phôi lỗi lọt vào, gần như không thể tách nó ra sau khi gia công vì toàn bộ lô đã "lai giống" nhau.

### Cửa 2 — FAI (First Article Inspection): chi tiết đầu tiên quyết định lô hàng

Trước khi chạy hàng loạt với bất kỳ: máy mới, dao mới, chương trình mới, hay sau một lần ngừng máy lâu — bắt buộc lấy **chi tiết đầu tiên** đo toàn bộ đặc tính quan trọng (các kích thước chịu lực, vị trí lỗ, độ nhám) và lập biên bản FAI. Chỉ khi FAI PASS, lô mới được phép chạy với tốc độ bình thường.

> Sai lầm phổ biến: FAI bị hiểu là "việc của QC", trong khi thực tế QC chỉ đo; người cài đặt máy mới là người cần biết kết quả để hiệu chỉnh chương trình theo hướng tâm dung sai.
{: .prompt-tip }

### Cửa 3 — In-process: kiểm tuần theo chu kỳ, giữ lỗi ở mức khu vực nhỏ

Khi lô đã chạy, QC thực hiện kiểm định kỳ (ví dụ 1–2 giờ/lần) theo Control Plan: lấy mẫu ngẫu nhiên trên chuyền, đo kích thước chủ lực, đối chiếu xu hướng. Đo đúng cách ở cửa này—kết hợp ghi vào **biểu đồ kiểm soát (control chart)**—giúp phát hiện *xu hướng* dịch chuyển trước khi lỗi xảy ra, thay vì chỉ *kết quả* khi lỗi đã thành hiện thực.

### Cửa 4 — Assembly & Fit-up: tạm quên bản vẽ, lắp thử vào cụm thật

Nhiều chi tiết đạt dung sai độc lập nhưng khi lắp nối tiếp lại cộng dồn sai lệch (tolerance stack-up). Cửa này kiểm **độ khớp thực tế**: lắp part với chi tiết ghép, đo khe hở, độ đồng tâm, lực lắp. Nếu lỗi cộng dồn lộ ra — quyết định sửa lại, gia công lại, hay chấp nhận kèm biên bản.

### Cửa 5 — Final & OQC: cửa cuối trước khi rời nhà máy

Kiểm 100% ngoại quan + lấy mẫu AQL cho kích thước theo [quy trình nhận-giao hàng chuẩn](/posts/thu-mua-trong-nha-may-viet-nam/), rồi kiểm bao bì, nhãn, số lượng, seal lô. Đây là cửa duy nhất mà boss nhà máy *nhìn thấy bằng mắt*, nên nhiều nơi tập trung lực lượng vào đây — nhưng đáng tiếc, phần lớn giá trị của QC nằm ở 4 cửa trước.

## 4. Đánh dấu trạng thái: "chữ ký" của từng cửa kiểm

Sau mỗi cửa, part bắt buộc được ghi trạng thái trước khi chuyển sang công đoạn sau — theo quy ước màu và nguyên tắc *"no mark, no move"*. Với part gia công, có ba lưu ý đặc thù khi chọn vật tư đánh dấu:

- **Part còn phải qua tẩy dầu, xử lý nhiệt hoặc sơn**: vạch/dấu phải sống sót qua dầu cắt, dung dịch làm mát và nhiệt độ — nhưng sau đó phải tẩy sạch hoàn toàn trước công đoạn hoàn thiện bề mặt (cùng tiêu chí đã nêu ở [bài bút QC](/posts/but-danh-dau-qc-rohs-nha-may-co-khi/)). Mực công nghiệp dòng **TAT** của Shachihata được thiết kế đúng cho tình huống này: bám trên kim loại bóng, chịu nhiệt, không nhòe trong dầu.
- **Bề mặt tối màu (sắt thép đen, phôi rèn)**: lớp mực lông dầu mỏng sẽ khó đọc dưới đèn xưởng; **bút sơn Artline Paint Marker** với lớp mực dày, độ che phủ cao giúp QC nhận dạng dấu trong 2 giây.
- **Hồ sơ**: mọi vật tư đánh dấu tiếp xúc sản phẩm đều phải có RoHS/SDS. Nguồn cung chính hãng như Công ty Phúc Mã — nhà phân phối độc quyền Shachihata tại Việt Nam từ 2004 — luôn cấp kèm bộ hồ sơ này và dữ liệu khai báo (IMDS/ChemSHERPA) cho từng lô.

## 5. KPI tối thiểu cho bộ phận QC gia công

Không đo lường thì không cải thiện — bộ KPI gọn cho QC gia công cơ khí:

| KPI | Công thức | Mục tiêu tham khảo |
|-----|-----------|-------------------|
| Tỷ lệ lô nguyên liệu lỗi tại IQC | Lô lỗi / Tổng lô nhận | ≤ 2% |
| Tỷ lệ FAI PASS lần đầu | Số FAI đạt lần đầu / Tổng số FAI | ≥ 85% |
| Tỷ lệ lỗi nội bộ | Part lỗi / Tổng part sản xuất | < 0,5–1% |
| PPM giao khách | Part lỗi giao / 1 triệu part | < 100–200 ppm |
| Phát hiện lệch ở kiểm tuần | Số lần phát hiện trend / Tổng lần kiểm | Xu hướng giảm dần |

## Kết luận

QC trong nhà máy gia công cơ khí không nằm ở một "đội hình cuối line" mà nằm ở **kỷ luật của 5 cửa**: phôi đúng → FAI đạt → kiểm tuần bắt xu hướng sớm → lắp thử bắt lỗi cộng dồn → xuất xưởng sạch sẽ. Cửa nào thiếu một vạch dấu, thiếu một số đo là lô hàng đang mang một ẩn số.

> **Việc nên làm tuần này**: chọn một part đang chạy ổn định trong xưởng, rà lại hồ sơ từ phôi đến phiếu OQC — kiểm tra 5 cửa có đủ "chữ ký" không, và dụng cụ đo ở mỗi cửa có thang chia đủ mịn hơn dung sai cần giữ không. Chỗ nào thiếu là chỗ cần sửa đầu tiên.
{: .prompt-tip }
