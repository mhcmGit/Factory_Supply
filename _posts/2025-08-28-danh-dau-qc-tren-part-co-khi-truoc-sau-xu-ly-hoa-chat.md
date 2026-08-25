---
title: "Đánh dấu QC trên part cơ khí: Ghi chú đo đạc trước khi xử lý hóa chất, xi mạ và sơn phủ"
description: "Chia sẻ chuyên sâu về vai trò của bút marker đánh dấu QC trên bề mặt chi tiết cơ khí: ghi đường kính trục, lỗ, độ nhám, dung sai sau đo đạc, trước khi ngâm axit tẩy, xi mạ và sơn phủ. Cách chọn bút metal marker cho khu vực gia công."
date: 2025-08-28 09:00:00 +0700
categories: [quan-ly-chat-luong, san-xuat]
tags: [QC, marking, đánh dấu, bút marker, xi mạ, sơn phủ, xử lý hóa chất, gia công cơ khí, metal marker]
author: factory_supply_team
---

Trên một phân xưởng gia công cơ khí, sau khi chi tiết rời máy CNC hoặc bàn đo, hầu như lúc nào cũng có một việc nhỏ nhưng quyết định ngầm: **ghi chú lên chính bề mặt của part**. Con số `D12±0.02`, dòng chữ `M6 h16`, ký hiệu `Ra1.6` hay vệt khoanh vùng lỗi — tất cả là ghi chú của QC sau quá trình đo đạc, để part chờ qua công đoạn gia công tiếp theo (gia công lại, làm nguội, hay xử lý bề mặt).

Bài này bóc tách khâu tưởng như phụ trợ ấy thành một phần của quy trình QC: **vì sao phải đánh dấu, dùng loại bút nào, ghi những gì, và xử lý ra sao khi chi tiết gặp axit tẩy, bể xi mạ và dây chuyền sơn phủ.**

## 1. Vì sao phải đánh dấu lên bề mặt part?

Trong nhà máy cơ khí, "đo đạt → ghi chép → chi tiết rời máy" là thao tác liên tục. Nếu chỉ ghi vào sổ hoặc hệ thống MES mà trên part không có dấu, ca sau hoặc công nhân kế tiếp sẽ không biết part đó đang ở trạng thái nào:

- Đã qua kiểm tra hay vẫn còn chờ.
- Đường kính thực đo là **trên / dưới / đúng dung sai**.
- Part cần gia công lại, cần làm nguội, hay chuyển thẳng sang công đoạn hoàn tất.

Dấu đánh trên bề mặt chính là **cầu nối thị giác** giữa con số trong máy tính và chi tiết thực tế nằm trên giá chờ. Khi part nằm chờ trên kệ, vệt ghi là "đèn báo" duy nhất mà công nhân đọc ngay mà chẳng cần mở máy.

## 2. Yêu cầu đặc thù: bám tốt nhưng dễ loại bỏ trước khi xử lý hóa chất

Khác với việc đánh dấu vĩnh viễn trên sản phẩm hoàn chỉnh (như dấu torque seal giữ lâu dài), ở công đoạn này mực đánh dấu phải thỏa mãn hai yêu cầu trái ngược:

| Yêu cầu | Ý nghĩa |
|---|---|
| **Bám tốt** | Đủ vững để không lem, mờ khi part qua nhiều bàn, nhiều ca, tiếp xúc dầu, nước làm mát |
| **Dễ loại sạch** | Trước khi xi mạ / sơn phủ, vết đánh dấu cần được tẩy sạch khỏi bề mặt, tránh ảnh hưởng lớp phủ hay tạo khuyết tật |

Chọn mực sai (quá bám hoặc quá trơn) là rủi ro hai chiều: hoặc dấu bay sạch quá sớm khiến thông tin thất lạc, hoặc mực "nằm lại" trong quá trình xi mạ tạo vệt/chấm trên bề mặt hoàn thành.

## 3. Bút đánh dấu công nghiệp phù hợp cho khu vực đo đạc

Thực tế phổ biến ở nhà máy cơ khí, các dòng **bút lông dầu công nghiệp** (industrial oil marker) và **paint marker** đầu ngòi mịn (fine / extra-fine) được ưu tiên vì:

- **Bám đủ tốt** trên thép cacbon, thép không gỉ, nhôm dù bề mặt còn lớp dầu chống gỉ mỏng.
- **Khô nhanh**, không nhỏ, ít lem trong khu vực đo.
- Đầu mịn cho phép viết **chữ số, ký hiệu nhỏ** dễ đọc — rất cần cho ghi chú dung sai.

Một số dòng thường thấy trên thị trường do nhà phân phối như Phúc Mã cung cấp cho phân khúc này gồm bút lông bi công nghiệp **Artline EK-041T**, dòng **Artline X605**, và các mực viết kim loại (paint marker **EK-400XF**, **EKPR-LNM** dùng cho vị trí sâu / lỗ hẹp). Việc chọn thương hiệu và model phụ thuộc loại vật liệu, điều kiện môi trường và yêu cầu lưu dấu từng xưởng — cần đối chiếu tài liệu kỹ thuật chính thức từ nhà cung cấp.

> Nội dung trên chỉ mang tính chia sẻ, không phải quảng bá cho bất kỳ thương hiệu nào. Người đọc nên đối chiếu datasheet và quy trình của từng nhà máy.

## 4. Nguyên tắc ghi chú trên bề mặt cho khâu đo đạc

Để dâu dễ đọc và khó nhầm, các ca làm nên theo vài quy tắc chung:

1. **Ngắn gọn, đúng ký hiệu GD&T:**
   - Đường kính trục: `Ø12.02` hoặc `D12±0.02`
   - Lỗ: `M6×1.0 – 7H`
   - Độ nhám: `Ra1.6`
   - Sai số kiểu trục-lỗ: `Ø10 h6 / Ø10 H7`
2. **Vị trí cố định, dễ thấy** nhưng **tránh bề mặt lắp ráp quan trọng** và mặt có dung sai chặt.
3. **Một màu một ý nghĩa** theo quy ước nhà máy:
   - Xanh: đã đo đạt OK
   - Đỏ: NG / chờ xử lý lại
   - Vàng / cam: chờ lệnh / chờ quyết định
4. **Đánh dấu ngay khi còn trên bàn đo hoặc đồ gá**, đảm bảo số liệu không bị lệch lạc.

## 5. Dấu đánh khi chi tiết đi qua xử lý hóa chất, xi mạ, sơn phủ

Khi part được chuyển sang bước xử lý bề mặt (ngâm axit tẩy, xi mạ, sơn phủ), QC cần kiểm soát dấu đánh theo đúng công đoạn:

- **Trước khi ngâm axit / tẩy sạch**: phần lớn nhà máy sẽ **loại bỏ dấu bằng dung môi tẩy rửa** hoặc để nó tan trong chính bể xử lý. Dấu lúc này chỉ phục vụ khâu đo-đạt trước đó, không nên để nguyên vào bể mạ vì dễ tạo vẩn, vết trên lớp phủ.
- **Sau khi mạ / sơn**: nếu cần đánh lại dấu trạng thái (mã OK, dấu PASS, mã lot), dấu lúc này thường dùng **mực paint marker** bám tốt trên lớp phủ và phải tương thích với lớp mạ/sơn (không ăn mòn, không phản ứng, không làm bong lớp phủ).
- Nếu xưởng **đánh dấu rồi mới phủ lớp sơn trong**, cần chắc mực chịu được cách phủ mà không bị chảy, loang hay mất màu.

Nói gọn: **đánh dấu đúng công đoạn quan trọng hơn chọn mực**. Đánh đúng lúc, đúng vị trí, màu đúng quy định, và luôn có kế hoạch loại bỏ dấu ở bước xử lý khi cần.

## 6. Checklist QC trước khi đưa part vào dây chuyền xử lý

Trước khi chi tiết vào dây chuyền axit / xi mạ / sơn, QC nên đối soát lại:

- [ ] Vị trí đánh dấu đúng bản vẽ, không che mặt lắp ráp quan trọng
- [ ] Nội dung ghi đủ (đường kính, lỗ, độ nhám, dung sai)
- [ ] Màu dấu đúng quy ước (OK / NG / HOLD)
- [ ] Dấu rõ ràng, không lem, không làm mất con số đo
- [ ] Bút dùng đúng loại đã chọn tại trạm, đầu ngòi còn tốt
- [ ] Đã thống nhất kế hoạch loại bỏ dấu trước khi ngâm / xi / sơn

## Kết luận

Dấu đánh trên bề mặt part — dù chỉ là vài con số ghi bằng bút công nghiệp — là **thẻ hành trình vật lý** của chi tiết đi qua chuỗi công đoạn: đo đạt, chờ xử lý, gia công lại, và hoàn tất bề mặt. Chọn đúng loại bút, tuân theo quy ước ghi dấu, ghi đúng lúc và kịp thời loại bỏ trước khi ngâm/mạ/sơn giúp nhà máy kiểm soát thông tin đo lường mà không làm hại lớp phủ cuối cùng.

> **Việc nên làm tuần này:** rà lại bảng quy ước ghi dấu từng ca (màu sắc, vị trí chuẩn) cho khớp với các loại xử lý bề mặt đang vận hành; in và dán tại trạm đo để cả team dùng chung một mẫu.
{: .prompt-tip }

*Bài chia sẻ mang giá trị tham khảo về nghiệp vụ QC. Thông số từng dòng bút đánh dấu cần đối chiếu tài liệu kỹ thuật chính thức của nhà cung cấp để chọn sản phim phù hợp với điều kiện thực tế từng nhà máy.*