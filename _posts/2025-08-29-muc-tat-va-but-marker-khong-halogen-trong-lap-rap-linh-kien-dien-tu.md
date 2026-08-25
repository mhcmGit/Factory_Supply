---
title: "Tại sao ngành điện tử gắt gao với Halogen? Bài toán mực TAT và bút marker Artline trong lắp ráp board mạch"
description: "Tìm hiểu lý do các nhà máy gia công, lắp ráp linh kiện điện tử yêu cầu khắt khe về mực dấu và bút marker không chứa halogen. Phân tích RoHS, hạn chế halogen, giấy tờ chemSHERPA, JAPIA, REACH SVHC và vai trò của mực TAT, bút Artline trong quy trình kiểm tra sản phẩm."
date: 2025-08-29 09:00:00 +0700
categories: [quan-ly-chat-luong, san-xuat]
tags: [RoHS, halogen, mực TAT, bút marker, electronics, board mạch, chemSHERPA, REACH, SVHC, JAPIA]
author: factory_supply_team
---

Trong các nhà máy gia công, lắp ráp linh kiện điện tử, người ta dùng **mực đóng dấu** (ink stamp) để xác nhận trạng thái và bút marker để đánh dấu trong khâu kiểm tra chất lượng sản phẩm. Loại mực được dùng phổ biến đến mức nhà máy đặt tên riêng theo thương hiệu — điển hình là **"mực TAT"**, gắn liền với loại mực đóng dấu công nghiệp được ưa dùng trên dây chuyền.

Nhưng những năm gần đây, các nhà máy rất **gắt gao** về việc mực dấu và bút marker phải **không chứa halogen**. Vì sao? Câu trả lời nằm ở tính nhạy cảm của bo mạch điện tử với hóa chất và khả năng gây hỏng hóc nghiêm trọng trong quá trình hàn nhiệt.

## 1. Halogen là gì và nằm đâu trong sản phẩm điện tử?

Halogen là nhóm nguyên tố gồm **Flo (F), Clo (Cl), Brom (Br), I-ốt (I)**. Trong ngành điện tử, các hợp chất chứa Clo và Brom thường được dùng làm chất chậm cháy (flame retardant) hoặc phụ gia. Khi thiết bị hoạt động ở nhiệt độ cao, các hợp chất này **nhả acid (HBr, HCl)** — mà acid là kẻ thù của mạch điện tử.

Với **mực dấu, bút marker**, halogen có thể ngấm vào dung môi, phụ gia tạo màu, nhựa nền. Nếu không kiểm soát, chúng sẽ "theo dấu mực" bám lên bo mạch (PCB) và tạo nguy cơ khi qua nhiệt.

## 2. Vì sao điện tử nhạy cảm với halogen đến vậy?

Khác với cơ khí, linh kiện điện tử trải qua **nhiệt độ cao nhiều lần**: hàn nhúng (wave), hàn chảy (reflow) thường trên 250°C. Ở nhiệt độ này:

- Hợp chất halogen có trong mực, nhớt, keo trên PCB **phân hủy và giải phóng axit**.
- Axit ăn mòn đường mạ đồng, đầu nối, giảm cách điện.
- Lâu ngày gây **gỉ, nứt, đứt nối hàn**, tăng tỷ lệ lỗi và hàng trả về.

Đó là lý do các tiêu chuẩn ngành điện tử như **IEC 61249-2-21** hay yêu cầu nội bộ của các hãng lớn (Apple, Samsung, khách OEM) đặt mức chặt **halogen (< 900 ppm mỗi loại, tổng < 1500 ppm)** trong vật liệu. Một nhà máy lắp ráp linh kiện cũng phải quét toàn bộ danh mục vật liệu, trong đó có cả **mực dấu và bút marker** cấp từ bên ngoài.

## 3. Yêu cầu chứng từ môi trường đối với mực dấu và bút marker

Vì mực dấu và bút marker tiếp xúc trực tiếp với board mạch, nhà máy thường yêu cầu nhà cung cấp đáp ứng bộ hồ sơ môi trường đầy đủ, trong đó các loại giấy tờ thường gặp:

| Chứng từ | Vai trò |
|---|---|
| **RoHS** | Khai báo giới hạn chất nguy hiểm (chì, thủy ngân, cadmium, halogen...), cho thấy sản phẩm đáp ứng |
| **chemSHERPA** | Tiêu chuẩn truyền thông tin hóa chất phổ biến của Nhật, dùng trong chuỗi cung ứng điện tử |
| **JAPIA** | Hệ thống khai báo hóa chất của các nhà sản xuất thiết bị Nhật, yêu cầu dữ liệu thành phần |
| **REACH (SVHC)** | Quy định EU; SVHC là danh mục chất đặc biệt quan ngại cần phải kê khai |
| **MSDS / SDS** | Bảng dữ liệu an toàn, khai báo thành phần và nguy cơ khi sử dụng |

Nhà máy có thể yêu cầu mức độ tùy theo đối tác (khách Nhật hay đòi chemSHERPA/JAPIA, khách EU đòi REACH SVHC, hoặc cả ba). Vì vậy nhà cung cấp mực dấu và bút marker cần **cam kết hạn chế halogen tối đa** và sẵn sàng xuất trình bộ hồ sơ này.

## 4. Vai trò của mực dấu và bút marker trong quy trình QC lắp ráp điện tử

Trong quy trình kiểm tra lắp ráp linh kiện điện tử, **mực đóng dấu** được dùng để xác nhận trạng thái (kiểm tra thị giác IQC, kiểm tra chức năng FCT, dấu PASS/NG), còn **bút marker** để đánh dấu vị trí lỗi, mã lot, ghi chú cho operator/QC.

Vì những dấu này nằm lại trên sản phẩm (có thể đi theo đến tận thiết bị hoàn chỉnh), chúng phải:

- **Không chứa halogen** để không sinh acid khi hàn nhiệt.
- Đạt **RoHS** và không nằm trong **danh mục SVHC (REACH)**.
- Có hồ sơ **chemSHERPA / JAPIA** khi khách hàng yêu cầu.
- Bám tốt trên bề mặt PCB/nhãn nhưng không ăn mòn, không gây rò điện ở vùng mạ.

Hiện nay các nhà máy rất gắt gao với phần này — nhiều nhà cung cấp phải dùng **mực TAT** (loại mực đóng dấu được ưa chuộng) và bút marker như **Artline**, thường do nhà phân phối như Phúc Mã cung cấp kèm hồ sơ RoHS/chemSHERPA/JAPIA/REACH. Đây là góc chia sẻ hiểu biết, không phải quảng bá thương hiệu.

## 5. Kiểm soát hóa chất, phụ gia trong quy trình nhà máy điện tử

Ngoài mực dấu và bút marker, các nhà máy lắp ráp linh kiện còn phải kiểm soát cả hóa chất, phụ gia khác trên dây chuyền: chất tẩy rosin, keo dán, kem hàn (solder paste), dung môi làm sạch. Tất cả đều nằm trong phạm vi kiểm soát về **halogen, RoHS, REACH/SVHC** để đảm bảo khi ghép nhiều vật liệu không tạo ra "tổng halogen" vượt mức.

Điểm khác biệt của mực dấu/bút marker: chúng là vật liệu **nằm lại ở lớp ngoài**, dễ được kiểm tra bằng thiết bị phân tích (XRF, đốt ion). Vì thế chúng là một trong những vật phẩm đầu tiên được nhà máy yêu cầu chứng nhận khi audit. Nhà cung cấp nên chủ động có sẵn bộ hồ sơ, chuẩn bị mẫu để đối ứng cho khách hàng.

## Kết luận

Gắt gao về halogen với mực dấu, bút marker không phải là "khó khăn công ty" mà là **bắt buộc về mặt kỹ thuật và tuân thủ** trong ngành điện tử: mực chứa halogen khi gặp nhiệt hàn sẽ sinh acid phá hỏng board mạch, và vi phạm RoHS/REACH ảnh hưởng đến khả năng xuất khẩu cũng như đối tác khách hàng lớn.

Do đó, khi một nhà máy điện tử yêu cầu mực dấu và bút marker không halogen, đó là dấu hiệu của quy trình kiểm soát hóa chất nghiêm ngặt mà người cung cấp cần đồng hành đáp ứng — đi kèm bộ giấy tờ RoHS, chemSHERPA, JAPIA, REACH SVHC, MSDS đầy đủ.

> **Việc nên làm tuần này:** nếu bạn cung cấp mực dấu hoặc bút marker cho nhà máy điện tử, hãy rà lại bộ chứng từ môi trường (RoHS, MSDS, chemSHERPA/JAPIA nếu khách Nhật, REACH SVHC) và kết quả xét nghiệm halogen gần nhất — để sẵn sàng trình ra khi khách audit.
{: .prompt-tip }

*Bài viết mang tính chia sẻ về kiến thức tuân thủ hóa chất trong sản xuất điện tử. Số liệu chứng từ và đặc tính từng sản phẩm mực/ bút cần đối chiếu tài liệu kỹ thuật chính thức của nhà cung cấp.*