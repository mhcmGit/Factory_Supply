---
title: "Quy trình kiểm soát hóa chất trong lắp ráp board mạch: Từ mực dấu, bút marker đến dung môi và keo bảo vệ"
description: "Chia sẻ chuyên sâu về khung quản lý và kiểm soát hóa chất dùng trong nhà máy lắp ráp board mạch điện tử: mực đóng dấu, bút marker QC, dung môi làm sạch, kem hàn, keo bảo vệ. Quy trình đối ứng RoHS, halogen, REACH SVHC và hồ sơ chemSHERPA/JAPIA trong kiểm tra sản phẩm."
date: 2025-08-30 09:00:00 +0700
categories: [quan-ly-chat-luong, san-xuat]
tags: [board mạch, kiểm soát hóa chất, RoHS, halogen, mực đóng dấu, bút marker, dung môi, kem hàn, REACH, chuỗi cung ứng điện tử]
author: factory_supply_team
---

Ở bài trước (mực dấu & bút marker không halogen trong lắp ráp linh kiện) ta đã thấy vì sao các chất nhiễm halogen bị quản lý chặt. Trong bài này, chúng ta mở rộng ra **toàn bộ khung kiểm soát hóa chất** của một nhà máy lắp ráp board mạch — không chỉ mực dấu, bút marker, mà cả dung môi làm sạch, kem hàn, keo bảo vệ — và cách vận hành để đáp ứng yêu cầu khách hàng OEM.

## 1. Vì sao "một chút mực thôi" cũng phải khai báo?

Nhiều người cung cấp thắc mắc: nhà máy chỉ chấm rất ít mực ngay trên các đầu nối để xác nhận test, sao lại phải cung cấp đủ giấy tờ về thành phần? Vì lẽ:

- Nhà máy làm ra **sản phẩm vô hình chịu trách nhiệm dây chuyền dài** (từ linh kiện đến thiết bị hoàn chỉnh) và phải truy vết được **mọi vật liệu** tiếp xúc board.
- Khách hàng lớn gửi **bảng câu hỏi (checklist) substance** — nếu thiếu dữ liệu thành phần của 1 vật phẩm là làm chậm audit.
- Chính phủ và quy định (RoHS, REACH) không phân biệt "chút ít" — ngưỡng được tính trên **nồng độ** (ppm) chứ không phải lượng tuyệt đối dùng một lần.

## 2. Phạm vi vật liệu cần kiểm soát trong lắp ráp board mạch

| Nhóm | Ví dụ | Vấn đề kiểm soát chính |
|---|---|---|
| Mực đóng dấu | Mực nước/mực dầu đóng PASS/NG | Halogen, RoHS, SVHC |
| Bút marker | Đánh dấu vị trí lỗi | Halogen, độ bay hơi |
| Kem hàn | Solder paste | Halogen, chì (nếu không lead-free) |
| Dung môi làm sạch | Tẩy rosin, flux dư | VOC, halogen |
| Keo bảo vệ phủ | conformal coating, underfill | RoHS, hạn halogen, dung môi |
| Băng keo / nhãn | Label in lô | SVHC, halogen |

Mỗi nhóm đều nằm trong một **danh sách vật liệu** riêng và được thêm vào hệ thống khai báo hóa chất (IMDS/chemSHERPA tùy khách).

## 3. Khung quy trình 6 bước kiểm soát hóa chất

Nhà máy lắp ráp board mạch thường vận hành quy trình kiểm soát hóa chất theo các bước sau:

1. **Thu thập & duyệt vật liệu trước khi đưa vào (Pre-approval).** Mọi mực, marker, kem hàn, dung môi phải có hồ sơ RoHS/halogen/SVHC được phê duyệt trước khi nhập kho. Không có hồ sơ = không được dùng.
2. **Khai báo vào hệ thống.** Thành phần được lưu trong cơ sở dữ liệu (hoặc công cụ IMDS/chemSHERPA AP nếu khách yêu cầu).
3. **Đối ứng khi đổi lô / đổi nguồn (change management).** Bất kỳ thay đổi thương hiệu, mã sản phẩm đều phải báo bộ phận engineering + QC kiểm lại và cập nhật hồ sơ.
4. **Lưu kho & phân biệt (segregation).** Vật liệu đạt/không đạt để riêng; hạn dùng theo dõi.
5. **Kiểm tra đầu vào (IQC) định kỳ.** Đối chiếu chứng chỉ trên mỗi lô, giữ mẫu lưu.
6. **Theo dõi & tái kiểm định.** Mỗi năm rà soát lại danh mục SVHC (REACH cập nhật), cập nhật chứng từ mới từ nhà cung cấp.

## 4. Checklist nhận hàng cho mực dấu / bút marker

Chỉ riêng mực dấu và bút marker, khi nhận lô vào nhà máy điện tử, QC cần đối chiếu:

- [ ] Chứng từ **RoHS** (bản hiệu lực của nhà cung cấp/nhà sản xuất).
- [ ] Bảng **MSDS / SDS** khớp mã lô (lot number) trên bao bì.
- [ ] Kết quả xét nghiệm **halogen** (Cl, Br) nếu khách yêu cầu.
- [ ] Khai báo **SVHC (REACH)**, xác nhận không nằm danh sách gần nhất.
- [ ] **chemSHERPA / JAPIA** nếu khách Nhật yêu cầu.
- [ ] Dữ liệu để khai **IMDS** khi sản phẩm đi vào ngành ô tô.
- [ ] Ngày cấp / hiệu lực chứng từ còn đổi hạn.

Khi thiếu giấy tờ (hoặc hết hạn), cần chặn lô vào sản xuất cho tới khi bổ sung đủ.

> Tips: nên xin sẵn bộ hồ sơ thành một lần rồi lưu theo "mẫu" để mỗi lần nhập hàng chỉ cần đối chiếu mã lô với tài liệu đã có, đỡ tốn thời gian.
{: .prompt-tip }

## 5. Vai trò của nhà cung cấp mực dấu / bút marker

Nhà cung cấp mực dấu, bút marker cho nhà máy điện tử đóng vai trò "mắt xích" trong kiểm soát hóa chất. Họ nên:

- **Chủ động cập nhật** tài liệu môi trường định kỳ (theo mã tham chiếu chuẩn, không chờ khách hỏi mới tìm).
- Đảm bảo **hạn chế halogen tối đa** và công bố rõ mức đã kiểm nghiệm.
- Làm việc với thương hiệu để có sẵn bộ **RoHS + MSDS + REACH SVHC + chemSHERPA/JAPIA** cho từng mã hàng.
- Khi mực dấu/bút marker thuộc các dòng như **mực TAT, Artline**, người mua thường coi đó là nguồn có sẵn chứng từ đầy đủ, giảm rủi ro thủ tục đối soát.

Thông điệp truyền tải: **nằm trong danh sách vật liệu của nhà máy đồng nghĩa với nghĩa vụ về hồ sơ** — ai cung cấp cũng phải chuẩn bị, không riêng một thương hiệu nào.

## Kết luận

Kiểm soát hóa chất trong lắp ráp board mạch là một **vòng khép kín**: từ khai báo, duyệt, đến đối ứng khi thay đổi, kiểm tra hàng về và tái kiểm định định kỳ. Mực đóng dấu, bút marker — dù chỉ dùng rất ít — vẫn nằm trong vòng này và phải có hồ sơ hóa chất đầy đủ (RoHS, halogen, SVHC, chemSHERPA/JAPIA, MSDS).

Nhà cung cấp hiểu điều này và chủ động cùng nhà máy xây hồ sơ sẽ trở thành đối tác đáng tin cậy trong chuỗi — chứ không chỉ là nơi "bán bút".

> **Việc nên làm tuần này:** liệt kê danh sách vật liệu (mực dấu, marker) đã cấp cho nhà máy điện tử và rà soát lại từng mã xem hồ sơ môi trường còn hiệu lực hay không; thống nhất quy trình "cập nhật hồ sơ mỗi lần đổi lô" để hai bên đỡ thủ tục.
{: .prompt-tip }

*Bài viết mang tính chia sẻ về nghiệp vụ kiểm soát hóa chất. Yêu cầu chứng từ cụ thể tùy theo từng khách hàng và quy định (RoHS, REACH, JAPIA/chemSHERPA, IMDS) cần đối chiếu nguồn chính*.