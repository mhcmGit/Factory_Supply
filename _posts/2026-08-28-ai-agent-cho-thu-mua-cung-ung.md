---
title: "AI Agent cho Thu mua & Cung ứng: Khi 'nhân viên số' tự động hóa toàn bộ quy trình mua hàng"
description: "Chuyên sâu về AI Agent (agentic AI) trong thu mua & cung ứng: khác gì chatbot/RPA, kiến trúc hoạt động, ví dụ xử lý đề nghị mua end-to-end, 8 use case theo mức tự động hóa, dự báo Gartner, rủi ro & lộ trình áp dụng 5 bước cho phòng thu mua."
date: 2026-08-28 09:00:00 +0700
categories: [logistics, thu-mua]
tags: [AI Agent, agentic AI, thu mua, procurement, tự động hóa, RFQ, tail spend, Gartner, supply chain]
author: factory_supply_team
---

Nếu [AI trong logistics](/posts/ai-trong-logistics-cach-ap-dung-hieu-qua/) là câu chuyện về **dự báo và tối ưu**, thì làn sóng 2025–2026 mang đến một chương mới gây chấn động hơn: **AI Agent (agentic AI)** — phần mềm không chỉ *trả lời* hay *dự báo*, mà **tự lên kế hoạch, tự ra quyết định trong giới hạn, và tự thực hiện** chuỗi công việc mua hàng từ đầu đến cuối.

Gartner gọi đây là "làn sóng agentic shift": phần mềm chuỗi cung ứng tích hợp agentic AI được dự báo tăng từ **dưới 2 tỷ USD (2025) lên 53 tỷ USD (2030)**; và dự đoán táo bạo hơn: đến **2028, AI Agent sẽ trực tiếp thực hiện các giao dịch B2B trị giá 15.000 tỷ USD**. Nhưng cùng Gartner cũng cảnh báo: **hơn 40% dự án agentic AI sẽ bị hủy trước hết 2027** vì chi phí đội lên, giá trị không rõ ràng và thiếu kiểm soát rủi ro.

Bài này tách bạch hype khỏi thực tế: AI Agent là gì, vận hành thế nào, làm được gì cho phòng thu mua, rủi ro ở đâu — và lộ trình áp dụng đúng cho doanh nghiệp Việt Nam.

## 1. AI Agent là gì? Khác gì ChatGPT và RPA mà ta đã biết?

Ba công nghệ, ba mức độ "tự chủ" hoàn toàn khác nhau:

| | Chatbot / GenAI (ChatGPT) | RPA (Robot quy trình) | **AI Agent (Agentic AI)** |
|---|---|---|---|
| Làm gì | Trả lời, viết, tổng hợp theo từng câu hỏi | Lặp lại đúng các bước được lập trình sẵn | **Tự lập kế hoạch và thực hiện** mục tiêu nhiều bước |
| Hiểu ngữ cảnh | Có, nhưng bị động | Không — kịch bản cứng | Có — theo dõi trạng thái, thích ứng |
| Xử lý ngoại lệ | Gợi ý cho người xử lý | Đứng im khi gặp tình huống lạ | **Tự đổi hướng** hoặc leo thang đúng người |
| Kết nối hệ thống | Không (trừ plugin đơn lẻ) | Có, nhưng theo kịch bản cố định | Có — gọi API ERP/NCC/hệ thống một cách linh hoạt |

Định nghĩa gọn cho thu mua: **AI Agent là hệ thống tự chủ có khả năng cảm nhận dữ liệu từ các hệ thống thu mua, ra quyết định theo chính sách/ngưỡng được cấp, và thực hiện chuỗi hành động nhiều bước mà không cần người hướng dẫn từng bước.**

Về mặt kỹ thuật, một agent gồm 4 khối: **LLM (bộ não suy luận ngôn ngữ)** + **Planning** (phân rã mục tiêu thành các bước) + **Memory** (ghi nhớ ngữ cảnh, trạng thái) + **Tools** (kết nối ERP, cổng NCC, email, cơ sở dữ liệu để *hành động* thật). Khác biệt quyết định so với ChatGPT: agent không dừng ở câu trả lời — nó **thực thi** qua các hệ thống.
## 2. Một ngày làm việc của AI Agent trong phòng thu mua: ví dụ end-to-end

Hãy đi qua **một quy trình hoàn chỉnh** để thấy agent khác gì một công cụ thông thường. Tình huống: dây chuyền gửi **Đề nghị mua hàng (PR)** cho 500 bộ vòng bi, cần trong 10 ngày.

**Cách hiện tại (thủ công):** planner nhập PR → thu mua nhận → tra Excel xem tồn kho → mở danh sách NCC → gửi email hỏi giá 3–5 NCC → chờ trả lời 2–3 ngày → lập bảng so sánh → xin duyệt → lập PO trên ERP → theo dõi xác nhận... **tổng cộng 3–7 ngày làm việc.**

**Cách AI Agent xử lý (trong vài giờ, có người duyệt ở các điểm mấu chốt):**

```text
Bước 1 – Cảm nhận:  Agent đọc PR mới từ ERP, hiểu: "vòng bi 6205-2RS, 500 cái, cần 10 ngày"
Bước 2 – Kiểm tra:  Tra tồn kho & MRP → không đủ → xác nhận cần mua ngoài
Bước 3 – Lập kế hoạch: Chọn 5 NCC đủ tiêu chí (đã duyệt, có lịch sử tốt, đúng vùng)
Bước 4 – Hành động: Tự động gửi RFQ qua email/cổng NCC kèm bản vẽ & điều kiện
Bước 5 – So sánh:   Thu hồi báo giá, chuẩn hóa về cùng một mặt bằng (giá, lead time,
                    điều khoản), lập bảng so sánh kèm khuyến nghị
Bước 6 – Leo thang: Gửi bảng so sánh + khuyến nghị cho thu mua duyệt  ← NGƯỜI QUYẾT ĐỊNH
Bước 7 – Thực thi:  Sau duyệt → tự lập PO trên ERP, gửi NCC, theo dõi xác nhận
Bước 8 – Theo dõi:  Nhắc NCC trước hạn giao, cảnh báo nếu trễ, cập nhật lịch sử
```

Điểm mấu chốt: agent **không tự ý ký hợp đồng** — nó thực hiện toàn bộ phần việc lặp lại và chuẩn bị dữ liệu, con người chỉ chạm vào các điểm quyết định (duyệt giá, duyệt NCC). Đây gọi là mô hình **human-in-the-loop với guardrails** (rào chắn phê duyệt theo ngưỡng: dưới X triệu và NCC đã duyệt → agent tự chạy; vượt ngưỡng → dừng chờ người).

## 3. Bản đồ use case: việc gì nên giao cho Agent trước?

Không phải việc thu mua nào cũng phù hợp. Nguyên tắc: **khối lượng lớn + quy tắc rõ + rủi ro thấp** → agent; **chiến lược + quan hệ + phán đoán** → con người.

| Use case | Mức phù hợp với Agent | Ghi chú |
|---|---|---|
| **Tự động tạo RFQ & tìm NCC** | ⭐⭐⭐⭐⭐ | Use case ROI cao nhất 2026 — rút chu kỳ sourcing từ nhiều ngày xuống vài giờ |
| **Xử lý PR/PO trên ERP** | ⭐⭐⭐⭐⭐ | Tạo đơn, kiểm tra chính sách, đối chiếu ngân sách |
| **Tail spend** (chi tiêu nhỏ lẻ, nhiều NCC lẻ tẻ) | ⭐⭐⭐⭐⭐ | Nơi thu mua "chán nhất" — agent gom, hỏi giá, đặt hộ |
| **Đối chiếu 3 chiều PO–GR–Invoice** | ⭐⭐⭐⭐ | Phát hiện lệch giá/số lượng tự động, chỉ leo thang khi lệch |
| **Giám sát rủi ro & hiệu suất NCC liên tục** | ⭐⭐⭐⭐ | Quét tin tức, tài chính NCC, OTIF — cảnh báo sớm |
| **Đọc & soạn hợp đồng/tài liệu đấu thầu** | ⭐⭐⭐ | Hỗ trợ soạn thảo, rà điều khoản — luật sư/vụ pháp duyệt |
| **Đàm phán giá trong "rào chắn"** | ⭐⭐⭐ | Agent đàm phán trong khung giá/điều kiện được cấp |
| **Sourcing chiến lược, chọn NCC chiến lược** | ⭐ | Việc của con người — quan hệ, chiến lược, đánh giá rủi ro dài hạn |

Các nền tảng lớn đã đưa agent vào sản phẩm thương mại: **SAP Joule** (agent tự kiểm tra và phát hành lệnh sản xuất), **Coupa, Ivalua, SAP Ariba, Zip, GEP** (agentic sourcing), cùng các giải pháp chuyên tactical sourcing rút chu kỳ RFQ **từ nhiều ngày xuống vài giờ**. Một case được trích dẫn: nền tảng sourcing dược phẩm quản lý 1.800 loại tá dược / 7.500 SKU chạy RFQ tự động kèm xử lý hồ sơ chất lượng – quy định.
## 4. Thị trường nói gì? Những con số cần nhớ

- **> 40% dự án agentic AI sẽ bị hủy trước cuối 2027** (Gartner, khảo sát 3.400 tổ chức) — do chi phí leo thang, giá trị không rõ ràng, kiểm soát rủi ro yếu.
- Phần mềm chuỗi cung ứng tích hợp agentic AI: **từ < 2 tỷ USD (2025) → 53 tỷ USD (2030)** (Gartner dự báo 1/2026).
- Agent dự kiến quản lý **60–70% khâu thu mua giao dịch (transactional procurement)** từ đầu đến cuối — tail spend, sự kiện sourcing chuẩn hóa, giám sát NCC liên tục, cảnh báo rủi ro sớm.
- Đến **2028, AI Agent trực tiếp thực hiện giao dịch B2B trị giá ~15.000 tỷ USD** (Gartner).
- Đến 2027, khoảng cách chi phí–giá trị của hợp đồng dịch vụ quy trình giảm **≥ 50%** nhờ tái cấu trúc bằng agentic AI.

Đọc cẩn thận hai con số đối lập trên sẽ thấy thông điệp thật: **công nghệ là thật, nhưng đa số cách làm sẽ thất bại.** Người thực chiến mô tả mode thất bại phổ biến nhất không phải crash — mà là *agent tự tin chạy tiếp trên dữ liệu sai và không ai nhận ra cho đến 3 ngày sau khi số liệu lệch*. Vì vậy quản trị rủi ro là phần quan trọng nhất của cả bài.

## 5. Rủi ro & khung quản trị: làm sao để agent không "tự do quá tay"?

| Rủi ro | Biểu hiện | Biện pháp kiểm soát |
|---|---|---|
| **Ảo giác (hallucination)** | Agent "bịa" thông số, mã hàng, điều khoản | Bắt buộc trích dẫn nguồn dữ liệu (ERP/master data); chặn hành động nếu thiếu dữ liệu xác thực |
| **Chạy trên dữ liệu sai** | Lệch số tích lũy âm thầm nhiều ngày | Đối soát định kỳ; cảnh báo bất thường; log toàn bộ hành động |
| **Vượt thẩm mỹ** | Tự đặt PO vượt ngân sách, chọn NCC chưa duyệt | **Guardrails**: ngưỡng giá, danh sách NCC duyệt sẵn, quy tắc dừng-bắt-buộc |
| **Thiếu trách nhiệm** | "AI làm, không ai lỗi" | Mỗi hành động gắn người duyệt; audit trail đầy đủ; phân quyền rõ |
| **Bảo mật & dữ liệu** | Rò rỉ giá, thông tin NCC | Kiểm soát quyền truy cập API; không đưa dữ liệu mật vào LLM công cộng |

Nguyên tắc thiết kế an toàn, theo đúng khuyến nghị của các hướng dẫn triển khai 2026: **bắt đầu từ quy trình lặp lại có rủi ro thấp → tích hợp ERP & hệ thống hợp đồng → định nghĩa guardrails phê duyệt → con người giám sát → pilot trước rồi scale**. Agent nào "làm được nhiều việc" nhưng không nói rõ được guardrails ở đâu — đừng dùng.

## 6. Lộ trình 5 bước cho phòng thu mua Việt Nam

**Bước 1 – Vẽ bản đồ quy trình & tìm phần việc lặp lại.** Liệt kê mọi việc thu mua làm hằng ngày; đánh dấu những việc: lặp lại nhiều lần/ngày, có quy tắc rõ, tốn thời gian nhất. Đó là "mỏ vàng" của agent.

**Bước 2 – Sạch hóa dữ liệu & quy trình trước.** Danh mục NCC duyệt sẵn, ngưỡng phê duyệt, master data mã hàng — agent chỉ hoạt động tốt khi quy tắc tồn tại. (Đây cũng chính là nền tảng đã bàn trong [bài AI trong logistics](/posts/ai-trong-logistics-cach-ap-dung-hieu-qua/).)

**Bước 3 – Chọn 1 use case pilot có rào chắn.** Gợi ý an toàn nhất: **tự động gửi & thu hồi RFQ cho nhóm hàng tiêu chuẩn**, hoặc **đối chiếu 3 chiều PO–GR–Invoice**. Phạm vi hẹp, đo được (thời gian xử lý, số RFQ/lần chạy), rủi ro thấp.

**Bước 4 – Thiết kế guardrails & human-in-the-loop ngay từ đầu.** Xác định rõ: agent tự làm gì, dừng chờ duyệt ở đâu, ai duyệt, leo thang thế nào. Không bao giờ để agent "tự do hoàn toàn" ngay từ pilot.

**Bước 5 – Đo lường & mở rộng.** Sau pilot: so thời gian chu kỳ trước/sau, tỷ lệ xử lý tự động, số lỗi. Đạt → mở rộng sang tail spend, giám sát NCC. Không đạt → sửa dữ liệu/quy trình rồi thử lại — đừng vứt bỏ cả hướng đi.

> 💡 **Lưu ý chi phí – nhân lực**: với doanh nghiệp vừa và nhỏ, chưa cần mua nền tảng agentic đắt tiền. Nhiều việc "agent-like" đầu tiên có thể bắt đầu bằng công cụ AI phổ thông (tự soạn RFQ, so sánh báo giá, tóm tắt hợp đồng) kết hợp quy trình kỷ luật — rồi nâng cấp lên agent thật khi dữ liệu và quy trình đã sẵn sàng.
{: .prompt-tip }

## Kết luận

AI Agent không phải "ChatGPT cho thu mua" — đó là bước nhảy từ công cụ *trả lời* sang **nhân viên số tự thực hiện** phần việc giao dịch của chuỗi mua hàng: đọc PR, hỏi giá, so sánh, lập PO, theo dõi NCC. Thị trường dự báo phần mềm agentic cho chuỗi cung ứng tăng gấp 25 lần trong 5 năm, và agent sẽ gánh 60–70% khâu thu mua giao dịch.

Nhưng Gartner cũng cảnh báo 40% dự án sẽ chết — không vì công nghệ yếu, mà vì làm sai thứ tự: chạy đua công nghệ trước khi có dữ liệu sạch, quy trình rõ và guardrails chặt. Công thức đúng vẫn là công thức quen thuộc của mọi cải tiến: **quy trình chuẩn → dữ liệu sạch → pilot nhỏ → con người giám sát → nhân rộng.**

> **Việc nên làm tuần này**: mở danh sách công việc hằng ngày của phòng thu mua, khoanh những việc *lặp lại ≥ 5 lần/tuần và có quy tắc rõ* (gửi RFQ, nhắc NCC, đối chiếu hóa đơn...). Danh sách đó chính là "job description" đầu tiên cho AI Agent của bạn — và là bài kiểm tra xem quy trình của bạn đã đủ chuẩn để agent chạy hay chưa.
{: .prompt-tip }

---

*Bài viết tổng hợp từ các dự báo và thực tiễn agentic AI trong procurement 2025–2026 (Gartner, SupplyChainBrain, các nền tảng SAP Joule/Coupa/Ivalua...). Khả năng và mức tự động hóa thực tế tùy thuộc vào độ trưởng thành của dữ liệu, quy trình và nền tảng của từng doanh nghiệp.*