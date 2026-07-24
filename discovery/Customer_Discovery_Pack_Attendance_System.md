---
document_id: TBD
title: Customer Discovery Pack - Attendance System
status: Draft
version: 0.1
owner: Hoang Quy Nguyen
approver: Hoang Quy Nguyen
github_identity: frwkHoangQuy
last_updated: 2026-07-24
language: vi
authoritative_english_source: "N/A - tài liệu gốc được ủy quyền soạn bằng tiếng Việt, không phải bản dịch"
---

# Bộ tài liệu Discovery khách hàng — Hệ thống chấm công

> **Trạng thái kiểm soát:** Draft — chưa được phê duyệt, chưa phải cam kết về giải pháp, custom, tích hợp, kiến trúc, chi phí, tiến độ, SLA hoặc phạm vi hỗ trợ.
>
> **Quy tắc an toàn:** Kho Git này là công khai. Không điền tên khách hàng, dữ liệu cá nhân, dữ liệu sinh trắc học, thông tin liên hệ thật, địa chỉ nội bộ, IP/port cụ thể, sơ đồ mạng, cấu hình bảo mật, thông tin sản xuất, thông tin đăng nhập, mật khẩu, token, private key hoặc secret. Chỉ dùng mã đã khử định danh và tham chiếu đến kho evidence được phê duyệt, có kiểm soát truy cập. Thực hiện theo [Repository Agent Instructions](../AGENTS.md) và [Document Governance](../docs/00-project-control/document-governance.md).

## Mục lục

- [Hướng dẫn sử dụng](#hướng-dẫn-sử-dụng)
- [A — Thông tin kiểm soát tài liệu](#a--thông-tin-kiểm-soát-tài-liệu)
- [B — Mục tiêu và ranh giới buổi Discovery](#b--mục-tiêu-và-ranh-giới-buổi-discovery)
- [C — Thành phần tham gia và phân công](#c--thành-phần-tham-gia-và-phân-công)
- [D — Agenda buổi khảo sát](#d--agenda-buổi-khảo-sát)
- [E — Ma trận nội dung và câu hỏi khảo sát](#e--ma-trận-nội-dung-và-câu-hỏi-khảo-sát)
- [F — Ma trận Fit–Gap và yêu cầu custom](#f--ma-trận-fitgap-và-yêu-cầu-custom)
- [G — Thiết bị và khảo sát thực địa](#g--thiết-bị-và-khảo-sát-thực-địa)
- [H — Hạ tầng và network](#h--hạ-tầng-và-network)
- [I — Dữ liệu, tích hợp, bảo mật và quyền riêng tư](#i--dữ-liệu-tích-hợp-bảo-mật-và-quyền-riêng-tư)
- [J — Vận hành, đào tạo, hỗ trợ và bàn giao](#j--vận-hành-đào-tạo-hỗ-trợ-và-bàn-giao)
- [K — Checklist theo từng nhóm nội dung](#k--checklist-theo-từng-nhóm-nội-dung)
- [L — Checklist kiểm tra riêng cho BA](#l--checklist-kiểm-tra-riêng-cho-ba)
- [M — Checklist kiểm tra riêng cho Hạ tầng/Network](#m--checklist-kiểm-tra-riêng-cho-hạ-tầngnetwork)
- [N — Checklist kiểm soát của PM/Dev](#n--checklist-kiểm-soát-của-pmdev)
- [O — Issue, Risk, Assumption, Dependency và Decision Log](#o--issue-risk-assumption-dependency-và-decision-log)
- [P — Checklist đầu mối](#p--checklist-đầu-mối)
- [Q — Checklist kết quả bắt buộc sau khảo sát](#q--checklist-kết-quả-bắt-buộc-sau-khảo-sát)
- [R — Biên bản tổng kết cuối buổi](#r--biên-bản-tổng-kết-cuối-buổi)
- [S — Đánh giá mức độ hoàn thành Discovery](#s--đánh-giá-mức-độ-hoàn-thành-discovery)
- [Quality Review](#quality-review)

## Hướng dẫn sử dụng

1. Trước buổi khảo sát, PM điền Phần A–D, gán người hỏi cho từng ID và xác nhận người trả lời phù hợp phía khách hàng.
2. Trong buổi khảo sát, hỏi theo ID; ghi nguyên ý trả lời, nguồn, evidence và trạng thái xác minh. Không có xác nhận thì ghi `[CHƯA XÁC NHẬN]`.
3. Khi một thông tin được dùng ở nhiều phần, tham chiếu ID gốc; không hỏi lại hoặc sao chép thành một “sự thật” mới.
4. Phân loại từng ghi nhận: `FACT-ĐÃ XÁC NHẬN`, `THÔNG TIN-CHƯA XÁC MINH`, `ASSUMPTION`, `REQUIREMENT`, `WISH`, `ISSUE`, `CONSTRAINT`, `DECISION`, hoặc `OPEN`.
5. Cuối buổi, chạy checklist K–Q, đọc lại Phần R cho khách hàng và không biến việc “đã nghe/đã hỏi” thành “đã xác nhận/đã duyệt”.
6. Sau buổi, PM cập nhật Fit–Gap và các log bằng evidence đã được phép sử dụng; nội dung thiếu phải có đầu mối, hành động và hạn bổ sung.

### Quy ước

| Ký hiệu | Ý nghĩa |
|---|---|
| `Bắt buộc` | Cần trả lời hoặc phải ghi rõ lý do chưa thể trả lời. |
| `Nên có` | Cần nếu có thể; thiếu phải ghi ảnh hưởng. |
| `Có điều kiện` | Chỉ hỏi khi điều kiện nêu trong câu hỏi tiếp nối xảy ra. |
| `[ĐIỀN THÔNG TIN]` | Ô để đội khảo sát điền. |
| `[CHƯA XÁC NHẬN]` | Chưa có nguồn/evidence đủ thẩm quyền. |
| `[KHÔNG ÁP DỤNG – NÊU LÝ DO]` | Không áp dụng và phải nêu lý do. |
| Evidence | Bằng chứng phù hợp; trong tài liệu công khai chỉ ghi mã/tham chiếu đã khử định danh. |
| API | Cách phần mềm trao đổi dữ liệu tự động với hệ thống khác. |
| VLAN | Vùng mạng logic tách riêng các nhóm thiết bị. |
| UPS | Bộ lưu điện giúp thiết bị hoạt động tạm thời khi mất điện. |
| Fit–Gap | Đối chiếu nhu cầu với chức năng/cấu hình hiện có để xác định phần đáp ứng và khoảng trống. |

## A — Thông tin kiểm soát tài liệu

| Trường | Giá trị |
|---|---|
| Tên khách hàng | `[ĐIỀN MÃ KHÁCH HÀNG ĐÃ KHỬ ĐỊNH DANH]` `[CHƯA XÁC NHẬN]` |
| Địa điểm khảo sát | `[ĐIỀN MÃ ĐỊA ĐIỂM/KHO EVIDENCE]` `[CHƯA XÁC NHẬN]` |
| Ngày và giờ | `[ĐIỀN YYYY-MM-DD, HH:mm, Asia/Ho_Chi_Minh]` `[CHƯA XÁC NHẬN]` |
| Phiên bản tài liệu | `0.1 — Draft` |
| Người lập | `[ĐIỀN THÔNG TIN]` |
| PM phụ trách | `[ĐIỀN THÔNG TIN]` |
| BA phụ trách | `[ĐIỀN THÔNG TIN]` |
| Hạ tầng/Network phụ trách | `[ĐIỀN THÔNG TIN]` |
| Người rà soát | `[ĐIỀN THÔNG TIN]` |
| Trạng thái tài liệu | `Draft — [CHƯA XÁC NHẬN]/chưa phê duyệt` |
| Mục đích buổi khảo sát | Thu thập và xác minh hiện trạng, nhu cầu, ràng buộc, evidence và đầu mối cho hệ thống chấm công; không chốt giải pháp. |
| Phạm vi được phép trao đổi | Chức năng phần mềm hiện có ở mức được phép trình bày; nghiệp vụ, thiết bị, hạ tầng, dữ liệu, tích hợp, bảo mật, vận hành và nhu cầu cần đánh giá. |
| Những nội dung chưa được phép cam kết | Custom, tích hợp, kiến trúc, khả năng triển khai, chi phí, tiến độ, SLA, bảo hành/bảo trì, phạm vi hỗ trợ và ngày bàn giao. |
| Tài liệu tham chiếu | `[ĐIỀN MÃ TÀI LIỆU/ĐƯỜNG DẪN ĐÃ ĐƯỢC PHÉP]` `[CHƯA XÁC NHẬN]` |
| Ngày dự kiến phản hồi khách hàng | `[ĐIỀN YYYY-MM-DD SAU KHI PM XÁC NHẬN THẨM QUYỀN]` `[CHƯA XÁC NHẬN]` |

## B — Mục tiêu và ranh giới buổi Discovery

| Nội dung | Mô tả |
|---|---|
| Mục tiêu chính | Hiểu và xác minh nhu cầu, quy trình chấm công end-to-end, hiện trạng phần mềm/thiết bị/hạ tầng/dữ liệu, ràng buộc và thẩm quyền xác nhận. |
| Mục tiêu phụ | Xác định evidence, đầu mối, câu hỏi mở, mâu thuẫn, phụ thuộc, rủi ro và nội dung cần đánh giá Fit–Gap sau buổi làm việc. |
| Kết quả tối thiểu | Có mục tiêu, pain point, quy trình, quy mô, stakeholder/authority, yêu cầu ban đầu, thông tin thiết bị/network/dữ liệu, log còn mở và bước tiếp theo; nếu thiếu phải có owner và hạn bổ sung. |
| Ngoài phạm vi | Thiết kế kiến trúc chi tiết, thay đổi cấu hình, kết nối thử không được phép, truy cập dữ liệu thật, báo giá, ký nghiệm thu, duyệt custom hoặc chốt kế hoạch Delivery. |
| Quyết định không đưa ra tại buổi khảo sát | Chọn giải pháp kỹ thuật, xác nhận “có thể custom”, cam kết tích hợp, phạm vi hỗ trợ/SLA, chi phí, tiến độ, go-live hoặc nghiệm thu. |
| Điều kiện phải dừng/escalate | Yêu cầu truy cập dữ liệu hoặc hệ thống nhạy cảm; yêu cầu thay đổi cấu hình/kết nối/quét mạng; yêu cầu cam kết; thông tin mâu thuẫn ảnh hưởng phạm vi/bảo mật; người cung cấp không có thẩm quyền; phát hiện nguy cơ an toàn hoặc bảo mật. |

**Lời mở đầu đề xuất cho PM**

> Cảm ơn anh/chị đã dành thời gian. Hôm nay đội dự án mong muốn tìm hiểu và xác minh cách đơn vị đang quản lý chấm công, nhu cầu ưu tiên, điều kiện thiết bị, hạ tầng và vận hành. Chúng tôi sẽ ghi nhận đầy đủ để đối chiếu với chức năng phần mềm hiện có và đánh giá sau buổi làm việc. Buổi hôm nay chưa phải buổi chốt giải pháp; các đề nghị về custom, tích hợp, chi phí hoặc thời gian cần được kiểm tra và phê duyệt riêng trước khi phản hồi chính thức.

## C — Thành phần tham gia và phân công

### C1. Đội dự án

| Họ tên | Vai trò | Trách nhiệm | Nhóm câu hỏi phụ trách | Nội dung phải ghi nhận | Quyền được kết luận | Không được tự cam kết |
|---|---|---|---|---|---|---|
| `[ĐIỀN THÔNG TIN]` | PM/Dev | Chủ trì, kiểm soát phạm vi, điều phối, đánh giá sơ bộ chức năng hiện có | B, E1, E2, E6, F, N, Q–S | Ranh giới, Fit–Gap sơ bộ, cam kết phát sinh, quyết định/câu hỏi mở | Kết luận nội dung đã nghe và việc cần đánh giá; không kết luận khả năng triển khai khi thiếu evidence | Custom, kiến trúc, tích hợp, chi phí, tiến độ, SLA, nghiệm thu |
| `[ĐIỀN THÔNG TIN]` | BA | Khảo sát nghiệp vụ, yêu cầu, dữ liệu và truy vết | E1–E6, I, J, L | Câu trả lời, nguồn, fact/requirement/wish/assumption, ngoại lệ, acceptance criteria sơ bộ | Xác nhận cách hiểu đã được người có thẩm quyền đồng ý | Duyệt yêu cầu, phạm vi, custom hoặc thời hạn |
| `[ĐIỀN THÔNG TIN]` | Hạ tầng/Network | Khảo sát thực địa, thiết bị, nguồn, mạng, máy chủ, bảo mật, vận hành kỹ thuật | G, H, I, M | Hiện trạng, evidence được phép, giới hạn kỹ thuật, kiểm tra tiếp theo | Nêu quan sát và nội dung cần kiểm chứng | Tự kết nối, quét mạng, đổi cấu hình, cam kết kiến trúc/khả năng triển khai |
| `[ĐIỀN THÔNG TIN]` | Phối hợp/ghi biên bản | Theo dõi ID, thời gian, evidence và nội dung mở | Tất cả | Log, đầu mối, hạn, xác nhận cuối buổi | Không | Mọi cam kết vượt thẩm quyền |

### C2. Phía khách hàng

| Họ tên/mã định danh | Chức vụ | Đơn vị | Vai trò trong hệ thống | Loại thông tin có thể xác nhận | Quyền quyết định | Quyền nghiệm thu | Liên hệ an toàn | Thời gian tham gia |
|---|---|---|---|---|---|---|---|---|
| `[ĐIỀN THÔNG TIN]` | Sponsor/người quyết định | `[ĐIỀN]` | Tài trợ/định hướng | Mục tiêu, ưu tiên, phạm vi | `[CHƯA XÁC NHẬN]` | `[CHƯA XÁC NHẬN]` | `[THAM CHIẾU KHO ĐƯỢC PHÉP]` | `[ĐIỀN]` |
| `[ĐIỀN THÔNG TIN]` | HR/C&B | `[ĐIỀN]` | Chủ nghiệp vụ | Quy trình, quy tắc, ngoại lệ, báo cáo | `[CHƯA XÁC NHẬN]` | `[CHƯA XÁC NHẬN]` | `[THAM CHIẾU]` | `[ĐIỀN]` |
| `[ĐIỀN THÔNG TIN]` | Người vận hành | `[ĐIỀN]` | Thao tác hằng ngày | Hiện trạng, lỗi, khối lượng, workaround | Không mặc định | Không mặc định | `[THAM CHIẾU]` | `[ĐIỀN]` |
| `[ĐIỀN THÔNG TIN]` | IT/Network/Security | `[ĐIỀN]` | Quản trị kỹ thuật | Thiết bị, mạng, máy chủ, bảo mật, quyền truy cập | `[CHƯA XÁC NHẬN]` | `[CHƯA XÁC NHẬN]` | `[THAM CHIẾU]` | `[ĐIỀN]` |
| `[ĐIỀN THÔNG TIN]` | Kế toán/Tính lương | `[ĐIỀN]` | Nhận đầu ra chấm công | Dữ liệu đầu ra, đối soát, kỳ lương | `[CHƯA XÁC NHẬN]` | `[CHƯA XÁC NHẬN]` | `[THAM CHIẾU]` | `[ĐIỀN]` |
| `[ĐIỀN THÔNG TIN]` | Người kiểm thử/nghiệm thu | `[ĐIỀN]` | Xác nhận chất lượng | Tiêu chí kiểm thử/acceptance | `[CHƯA XÁC NHẬN]` | `[CHƯA XÁC NHẬN]` | `[THAM CHIẾU]` | `[ĐIỀN]` |
| `[ĐIỀN THÔNG TIN]` | Quản lý cơ sở | `[ĐIỀN]` | Điều phối địa điểm | Vị trí, lưu lượng, điều kiện lắp đặt | `[CHƯA XÁC NHẬN]` | Không mặc định | `[THAM CHIẾU]` | `[ĐIỀN]` |

> Một người có thể giữ nhiều vai trò nhưng phải ghi riêng phạm vi thông tin, quyền quyết định và quyền nghiệm thu. Người cung cấp thông tin không mặc nhiên là người quyết định hoặc nghiệm thu.

## D — Agenda buổi khảo sát

| Mục | Thời lượng | Chủ trì | Người cần tham gia | Đầu ra cần đạt |
|---|---:|---|---|---|
| Giới thiệu thành phần và nguyên tắc an toàn | 5 phút | PM/Dev | Tất cả | Vai trò, quyền ghi nhận/chụp ảnh và giới hạn được hiểu thống nhất |
| Xác nhận mục tiêu và ranh giới | 5 phút | PM/Dev | Sponsor, HR/C&B, IT | Mục tiêu buổi làm việc và nội dung không cam kết được xác nhận |
| Khách hàng trình bày hiện trạng | 10 phút | BA | Sponsor, HR/C&B, vận hành | Bức tranh hiện tại, pain point, ưu tiên ban đầu |
| Quy trình nghiệp vụ end-to-end | 20 phút | BA | HR/C&B, vận hành, tính lương | Luồng, actor, input/output, ngoại lệ, phê duyệt |
| Chức năng, yêu cầu và Fit–Gap sơ bộ | 15 phút | PM/Dev + BA | HR/C&B, người dùng, quyết định | Danh sách nhu cầu có nguồn; chưa cam kết custom |
| Thiết bị, thực địa, nguồn điện | 10 phút | Hạ tầng/Network | IT, quản lý cơ sở | Inventory/điều kiện lắp đặt/evidence cần bổ sung |
| Hạ tầng, mạng, bảo mật | 15 phút | Hạ tầng/Network | IT/Network/Security | Mô hình, kết nối, quyền, giới hạn, kiểm tra tiếp theo |
| Dữ liệu, tích hợp, vận hành và hỗ trợ | 10 phút | BA + Hạ tầng/Network | HR, IT, payroll, vận hành | Nguồn dữ liệu, tích hợp, owner, hỗ trợ/đào tạo chưa cam kết |
| Đi thực địa nếu được phép | 0–15 phút | Hạ tầng/Network | IT, quản lý cơ sở | Quan sát có phép; không tự kết nối/thay đổi |
| Tổng kết và xác nhận thiếu/mâu thuẫn | 10 phút | PM/Dev | Tất cả đầu mối | Danh sách fact, open item, conflict, evidence thiếu |
| Đầu mối, bước tiếp theo và lời kết | 5 phút | PM/Dev | Người xác nhận biên bản | Owner, hạn bổ sung, ngày phản hồi dự kiến `[CHƯA XÁC NHẬN]` |

**Tổng:** 100–115 phút tùy việc đi thực địa.

## E — Ma trận nội dung và câu hỏi khảo sát

Mỗi ID có đủ 18 trường bắt buộc, được tách thành hai bảng để dễ đọc: bảng **Câu hỏi** gồm 11 trường và bảng **Ghi nhận/kiểm soát** gồm 7 trường còn lại. Hai bảng nối với nhau bằng ID.

### E1. Bối cảnh, mục tiêu và vấn đề kinh doanh

| ID | Nhóm | Mức độ | Người hỏi | Người phù hợp trả lời | Nội dung cần tìm hiểu | Câu hỏi nói với khách hàng | Mục đích nội bộ | Giải thích với khách hàng | Câu hỏi tiếp nối/điều kiện | Evidence cần thu |
|---|---|---|---|---|---|---|---|---|---|---|
| BUS-01 | Bối cảnh | Bắt buộc | PM/Dev | Sponsor | Lý do cần hệ thống/sự kiện khởi phát | “Điều gì khiến đơn vị bắt đầu xem xét hệ thống chấm công vào thời điểm này?” | Xác định mandate và driver | “Để chúng tôi tập trung khảo sát đúng vấn đề cần giải quyết.” | Nếu có deadline: ai phê duyệt, sự kiện nào, mức linh hoạt? | Quyết định/đề bài đã được phép tham chiếu |
| BUS-02 | Vấn đề | Bắt buộc | BA | HR/C&B, vận hành | Pain point của cách hiện tại | “Trong quy trình hiện tại, bước nào mất nhiều thời gian hoặc dễ sai nhất? Anh/chị có thể kể một tình huống gần đây đã khử định danh?” | Hiểu nguyên nhân và tác động | “Ví dụ thực tế giúp tránh thiết kế theo giả định.” | Tần suất, ảnh hưởng, cách xử lý tạm, ai chịu ảnh hưởng? | Quy trình/báo cáo lỗi mẫu đã khử định danh |
| BUS-03 | Mục tiêu | Bắt buộc | PM/Dev + BA | Sponsor, HR/C&B | Mục tiêu ưu tiên | “Nếu chỉ chọn ba kết quả quan trọng nhất, anh/chị muốn hệ thống cải thiện điều gì?” | Xếp ưu tiên | “Để đánh giá Fit–Gap theo đúng giá trị mong đợi.” | Nếu các bên khác nhau: ghi CONFLICT và người quyết định | Mục tiêu/KPI đã được duyệt |
| BUS-04 | Kết quả | Bắt buộc | BA | Sponsor, nghiệm thu | Kết quả kỳ vọng/tiêu chí thành công | “Dấu hiệu hoặc số liệu nào cho thấy giải pháp đã mang lại kết quả mong muốn?” | Tạo acceptance criteria sơ bộ | “Để sau này hai bên có cùng cách đánh giá.” | Baseline? ngưỡng? ai đo? khi nào đo? | KPI/tiêu chí hiện hành |
| BUS-05 | Thời điểm | Nên có | PM/Dev | Sponsor | Deadline/sự kiện thúc đẩy | “Có mốc nghiệp vụ hoặc sự kiện nào cần lưu ý không? Mốc đó đã được ai xác nhận?” | Nhận biết constraint, không cam kết | “Để chúng tôi ghi nhận phụ thuộc khi đánh giá kế hoạch.” | Nếu chưa phê duyệt: ghi `[CHƯA XÁC NHẬN]`; mốc cứng hay mong muốn? | Lịch/mốc đã được phê duyệt |
| BUS-06 | Sản phẩm tặng | Bắt buộc | PM/Dev | Sponsor, người có thẩm quyền | Phạm vi và kỳ vọng về sản phẩm tặng | “Anh/chị hiểu phạm vi sản phẩm được tặng gồm những gì và nội dung nào chưa bao gồm?” | Phát hiện lệch kỳ vọng | “Để tránh hiểu nhầm giữa quà tặng, cấu hình và phần việc cần đánh giá riêng.” | Nguồn xác nhận? thiết bị/license/dịch vụ nào? | Văn bản phạm vi được phép tham chiếu |
| BUS-07 | Custom/hỗ trợ | Bắt buộc | PM/Dev | Sponsor, HR/C&B | Kỳ vọng custom, hỗ trợ, vận hành | “Anh/chị đang mong muốn thay đổi hoặc hỗ trợ thêm ở điểm nào? Chúng tôi sẽ ghi nhận để kiểm tra, chưa xác nhận khả năng tại buổi hôm nay.” | Lập danh sách đánh giá | “Để yêu cầu được đánh giá đúng chức năng, phụ thuộc và thẩm quyền.” | Giá trị, người dùng, ưu tiên, workaround, người duyệt? | Yêu cầu/biểu mẫu minh họa đã khử định danh |
| BUS-08 | Ràng buộc | Bắt buộc | Phối hợp | Sponsor, IT, HR | Ràng buộc pháp lý/chính sách/ngân sách/thời gian | “Có chính sách hoặc giới hạn nào đội dự án bắt buộc phải tuân thủ không?” | Nhận diện constraint | “Để không đề xuất phương án xung đột với quy định của đơn vị.” | Ai sở hữu/quyết định? tài liệu nào được xem? | Mã chính sách hoặc xác nhận có thẩm quyền |

| ID | Kết quả ghi nhận | Nguồn cung cấp | Trạng thái xác minh | Ảnh hưởng nếu thiếu | Người theo dõi | Hạn bổ sung | Ghi chú |
|---|---|---|---|---|---|---|---|
| BUS-01 | `[ĐIỀN THÔNG TIN]` | `[CHƯA XÁC NHẬN]` | Chưa hỏi | Không xác định mandate/driver | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` |
| BUS-02 | `[ĐIỀN THÔNG TIN]` | `[CHƯA XÁC NHẬN]` | Chưa hỏi | Không ưu tiên đúng pain point | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` |
| BUS-03 | `[ĐIỀN THÔNG TIN]` | `[CHƯA XÁC NHẬN]` | Chưa hỏi | Không xếp ưu tiên Fit–Gap | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` |
| BUS-04 | `[ĐIỀN THÔNG TIN]` | `[CHƯA XÁC NHẬN]` | Chưa hỏi | Không lập acceptance criteria | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` |
| BUS-05 | `[ĐIỀN THÔNG TIN]` | `[CHƯA XÁC NHẬN]` | Chưa hỏi | Không đánh giá phụ thuộc lịch | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` |
| BUS-06 | `[ĐIỀN THÔNG TIN]` | `[CHƯA XÁC NHẬN]` | Chưa hỏi | Có thể hiểu sai phạm vi quà tặng | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` |
| BUS-07 | `[ĐIỀN THÔNG TIN]` `[CHƯA CAM KẾT CUSTOM]` | `[CHƯA XÁC NHẬN]` | Chưa hỏi | Không lập được backlog đánh giá | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` |
| BUS-08 | `[ĐIỀN THÔNG TIN]` | `[CHƯA XÁC NHẬN]` | Chưa hỏi | Có thể đề xuất sai ràng buộc | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` |

**Checklist E1:** [ ] BUS-01–04, 06–08 đã hỏi; [ ] deadline được phân biệt “đã duyệt/mong muốn”; [ ] phạm vi sản phẩm tặng có nguồn; [ ] pain point có ví dụ/evidence; [ ] custom vẫn `[CHƯA CAM KẾT CUSTOM]`; [ ] mâu thuẫn mục tiêu đã vào Conflict Log.

### E2. Stakeholder, thẩm quyền và nghiệm thu

| ID | Nhóm | Mức độ | Người hỏi | Người phù hợp trả lời | Nội dung cần tìm hiểu | Câu hỏi nói với khách hàng | Mục đích nội bộ | Giải thích với khách hàng | Câu hỏi tiếp nối/điều kiện | Evidence cần thu |
|---|---|---|---|---|---|---|---|---|---|---|
| STK-01 | Sponsor | Bắt buộc | PM/Dev | Sponsor/đầu mối | Người bảo trợ và mục tiêu được bảo trợ | “Ai là người bảo trợ cho nhu cầu này và xác nhận mục tiêu tổng thể?” | Xác định escalation | “Để nội dung quan trọng được chuyển đúng người.” | Người thay thế? phạm vi quyền? | Xác nhận vai trò được phép tham chiếu |
| STK-02 | Quyết định | Bắt buộc | PM/Dev | Sponsor | Người quyết định phạm vi/ưu tiên | “Khi cần chọn phạm vi hoặc ưu tiên, ai có quyền quyết định cuối cùng?” | Kiểm soát authority | “Để không coi ý kiến cá nhân là quyết định chung.” | Quyết định riêng hay hội đồng? cách ghi nhận? | Ma trận thẩm quyền |
| STK-03 | Yêu cầu | Bắt buộc | BA | HR/C&B, quản lý | Người cung cấp/xác nhận yêu cầu | “Những ai cung cấp yêu cầu và ai xác nhận nội dung nghiệp vụ là đúng?” | Truy vết nguồn yêu cầu | “Để mỗi yêu cầu có nguồn và người xác nhận rõ.” | Nếu nhiều đơn vị: ai hợp nhất? | Danh sách vai trò/đầu mối |
| STK-04 | Sử dụng/quản trị | Bắt buộc | BA | HR, vận hành, IT | Người dùng trực tiếp và quản trị | “Những nhóm nào thao tác hằng ngày, nhóm nào quản trị hệ thống?” | Xác định actor/quyền | “Để khảo sát đúng tác vụ và phân quyền.” | Số lượng, ca làm, địa điểm, quyền đặc biệt? | Sơ đồ vai trò đã khử định danh |
| STK-05 | IT/HR/Payroll | Bắt buộc | Phối hợp | IT, HR/C&B, kế toán | Vai trò liên phòng ban | “IT, HR/C&B và bộ phận tính lương chịu trách nhiệm ở những điểm nào của quy trình?” | Xác định handoff | “Để tránh bỏ sót bước hoặc trách nhiệm giao nhau.” | Ai sở hữu dữ liệu? ai xử lý lỗi? | RACI/quy trình hiện hành |
| STK-06 | Kiểm thử | Nên có | BA | Người kiểm thử | Người chuẩn bị và thực hiện kiểm thử | “Ai sẽ chuẩn bị tình huống kiểm thử và xác nhận kết quả?” | Chuẩn bị UAT | “Để sau này có đúng người và đúng dữ liệu kiểm thử.” | Có môi trường/dữ liệu test? | Quy trình kiểm thử |
| STK-07 | Nghiệm thu/biên bản | Bắt buộc | PM/Dev | Sponsor, nghiệm thu | Người nghiệm thu và xác nhận biên bản | “Ai có quyền nghiệm thu và ai xác nhận biên bản buổi làm việc này?” | Tránh xác nhận sai thẩm quyền | “Để bản ghi nhận được gửi đúng người kiểm tra.” | Có nhiều cấp? hình thức xác nhận? | Ủy quyền/quy trình nghiệm thu |
| STK-08 | Mâu thuẫn | Bắt buộc | PM/Dev | Sponsor | Cơ chế xử lý yêu cầu mâu thuẫn | “Nếu hai bộ phận đưa ra yêu cầu khác nhau, ai điều phối và ai quyết định?” | Thiết lập conflict route | “Để đội dự án không tự chọn thay khách hàng.” | Thời hạn quyết định? evidence cần? | Quy trình escalation |

| ID | Kết quả ghi nhận | Nguồn cung cấp | Trạng thái xác minh | Ảnh hưởng nếu thiếu | Người theo dõi | Hạn bổ sung | Ghi chú |
|---|---|---|---|---|---|---|---|
| STK-01 | `[ĐIỀN]` | `[CHƯA XÁC NHẬN]` | Chưa hỏi | Không có escalation owner | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` |
| STK-02 | `[ĐIỀN]` | `[CHƯA XÁC NHẬN]` | Chưa hỏi | Không xác định quyết định hợp lệ | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` |
| STK-03 | `[ĐIỀN]` | `[CHƯA XÁC NHẬN]` | Chưa hỏi | Yêu cầu không có nguồn | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` |
| STK-04 | `[ĐIỀN]` | `[CHƯA XÁC NHẬN]` | Chưa hỏi | Thiếu actor/phân quyền | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` |
| STK-05 | `[ĐIỀN]` | `[CHƯA XÁC NHẬN]` | Chưa hỏi | Handoff và ownership mơ hồ | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` |
| STK-06 | `[ĐIỀN]` | `[CHƯA XÁC NHẬN]` | Chưa hỏi | Chưa chuẩn bị UAT | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` |
| STK-07 | `[ĐIỀN]` | `[CHƯA XÁC NHẬN]` | Chưa hỏi | Không thể xác nhận biên bản/nghiệm thu | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` |
| STK-08 | `[ĐIỀN]` | `[CHƯA XÁC NHẬN]` | Chưa hỏi | Đội dự án có thể xử lý sai mâu thuẫn | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` |

**Checklist E2:** [ ] Đủ người cung cấp/vận hành/quyết định/nghiệm thu; [ ] quyền của từng người có nguồn; [ ] IT–HR–Payroll handoff rõ; [ ] người xác nhận biên bản rõ; [ ] cơ chế xử lý mâu thuẫn đã ghi; [ ] chưa coi người tham dự là người có thẩm quyền nếu chưa xác minh.

### E3. Quy mô và cơ cấu sử dụng

| ID | Nhóm | Mức độ | Người hỏi | Người phù hợp trả lời | Nội dung cần tìm hiểu | Câu hỏi nói với khách hàng | Mục đích nội bộ | Giải thích với khách hàng | Câu hỏi tiếp nối/điều kiện | Evidence cần thu |
|---|---|---|---|---|---|---|---|---|---|---|
| SIZ-01 | Nhân sự | Bắt buộc | BA | HR/C&B | Số lượng và loại lao động | “Hiện có khoảng bao nhiêu nhân sự cần chấm công, gồm chính thức, thời vụ và cộng tác viên?” | Ước lượng tải và rule | “Mỗi nhóm có thể có quy tắc và cách quản lý khác nhau.” | Biến động theo mùa? người không chấm công? | Thống kê đã khử định danh |
| SIZ-02 | Cơ cấu | Bắt buộc | BA | HR/C&B | Phòng ban/đơn vị | “Các phòng ban hoặc đơn vị nào dùng chung và dùng khác quy tắc chấm công?” | Xác định cấu trúc/phân quyền | “Để không áp một quy tắc cho mọi nhóm khi thực tế khác nhau.” | Mã đơn vị chuẩn? thay đổi cơ cấu? | Sơ đồ tổ chức khử định danh |
| SIZ-03 | Cơ sở | Bắt buộc | BA + Hạ tầng | HR, quản lý cơ sở | Số cơ sở/địa điểm chấm | “Có bao nhiêu cơ sở và tại mỗi nơi nhân viên chấm công ở những vị trí nào?” | Xác định topology và inventory | “Để khảo sát đủ vị trí, kết nối và lưu lượng.” | Di chuyển giữa cơ sở? chấm ngoài cơ sở? | Danh sách mã cơ sở/vị trí |
| SIZ-04 | Ca làm | Bắt buộc | BA | HR/C&B | Số ca/nhóm ca | “Đơn vị đang dùng bao nhiêu loại ca và nhóm nào làm theo từng loại?” | Phạm vi business rules | “Để chọn đúng tình huống cần kiểm tra.” | Ca cố định/xoay/qua ngày? | Danh mục ca đã khử định danh |
| SIZ-05 | Quản trị | Nên có | BA | HR, IT | Số quản trị viên/phân cấp | “Có bao nhiêu người quản trị và quyền của họ được phân theo cơ sở hay phòng ban?” | Đánh giá role model | “Để tránh cấp quyền rộng hơn nhu cầu.” | Người dự phòng? tách nhiệm vụ? | Ma trận quyền |
| SIZ-06 | Tăng trưởng | Nên có | PM/Dev | Sponsor, HR | Tốc độ tăng trưởng/mở rộng | “Trong 12–36 tháng tới, số người dùng hoặc số cơ sở có dự kiến thay đổi không? Đây là kế hoạch đã duyệt hay ước tính?” | Đánh giá khả năng mở rộng | “Để ghi nhận nhu cầu tương lai mà không coi ước tính là cam kết.” | Mốc, độ chắc chắn, owner? | Kế hoạch đã duyệt nếu có |
| SIZ-07 | Cao điểm | Bắt buộc | Hạ tầng + BA | Vận hành, quản lý cơ sở | Lưu lượng giờ cao điểm | “Khung giờ nào đông nhất, khoảng bao nhiêu người chấm trong bao nhiêu phút tại từng vị trí?” | Đánh giá tải thiết bị/mạng | “Để tránh ùn tắc và xác định tình huống cần đo thực tế.” | Hàng đợi? nhiều thiết bị? sự kiện đặc biệt? | Quan sát/số liệu đã khử định danh |

| ID | Kết quả ghi nhận | Nguồn cung cấp | Trạng thái xác minh | Ảnh hưởng nếu thiếu | Người theo dõi | Hạn bổ sung | Ghi chú |
|---|---|---|---|---|---|---|---|
| SIZ-01 | `[ĐIỀN]` | `[CHƯA XÁC NHẬN]` | Chưa hỏi | Không ước lượng quy mô | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` |
| SIZ-02 | `[ĐIỀN]` | `[CHƯA XÁC NHẬN]` | Chưa hỏi | Không thiết kế được phân cấp | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` |
| SIZ-03 | `[ĐIỀN]` | `[CHƯA XÁC NHẬN]` | Chưa hỏi | Thiếu phạm vi địa điểm | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` |
| SIZ-04 | `[ĐIỀN]` | `[CHƯA XÁC NHẬN]` | Chưa hỏi | Thiếu phạm vi quy tắc ca | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` |
| SIZ-05 | `[ĐIỀN]` | `[CHƯA XÁC NHẬN]` | Chưa hỏi | Không đánh giá phân quyền | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` |
| SIZ-06 | `[ĐIỀN]` | `[CHƯA XÁC NHẬN]` | Chưa hỏi | Không đánh giá mở rộng | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` |
| SIZ-07 | `[ĐIỀN]` | `[CHƯA XÁC NHẬN]` | Chưa hỏi | Không đánh giá tải cao điểm | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` |

**Checklist E3:** [ ] Quy mô theo loại lao động; [ ] phòng ban/cơ sở/vị trí; [ ] ca và quản trị viên; [ ] tăng trưởng phân biệt kế hoạch/ước tính; [ ] lưu lượng cao điểm có nguồn/evidence; [ ] số liệu trong Git đã khử định danh.

### E4. Quy trình chấm công hiện tại

| ID | Nhóm | Mức độ | Người hỏi | Người phù hợp trả lời | Nội dung cần tìm hiểu | Câu hỏi nói với khách hàng | Mục đích nội bộ | Giải thích với khách hàng | Câu hỏi tiếp nối/điều kiện | Evidence cần thu |
|---|---|---|---|---|---|---|---|---|---|---|
| PRC-01 | Tạo nhân sự | Bắt buộc | BA | HR/C&B, IT | Actor, input, thao tác, công cụ, output, thời gian, lỗi | “Khi có nhân viên mới, ai tạo hồ sơ chấm công, lấy dữ liệu từ đâu, dùng công cụ nào và khi nào phải hoàn tất?” | Hiểu điểm bắt đầu/nguồn chuẩn | “Để tránh nhập trùng hoặc nhân viên chưa chấm được ngày đầu.” | Sai/trùng mã? thời vụ? nghỉ việc? ai duyệt? | Biểu mẫu/quy trình mẫu khử định danh |
| PRC-02 | Phân ca | Bắt buộc | BA | HR/C&B, quản lý | Luồng phân ca và thay đổi ca | “Ai lập và phân ca, dựa trên đầu vào nào, chốt trước bao lâu và xử lý thay đổi ra sao?” | Xác định rule/handoff | “Để hiểu dữ liệu nào quyết định cách tính công.” | Ca đột xuất? đổi ca? phê duyệt? | Lịch ca mẫu đã khử định danh |
| PRC-03 | Ghi nhận chấm công | Bắt buộc | BA + Hạ tầng | Vận hành, IT | Cách chấm, thiết bị/kênh, đầu ra | “Nhân viên chấm bằng cách nào, ở đâu, lúc nào và biết giao dịch đã ghi nhận thành công ra sao?” | Hiểu touchpoint/ngoại lệ | “Để kiểm tra trải nghiệm và các tình huống mất dữ liệu.” | Nhiều lần chấm? chấm hộ? offline? | Mô tả/ảnh có phép, log mẫu khử định danh |
| PRC-04 | Nhận dữ liệu | Bắt buộc | Hạ tầng + BA | IT, HR | Cách thu/chuyển dữ liệu, tần suất | “Dữ liệu từ thiết bị về đâu, tự động hay thủ công, theo thời gian thực hay theo lịch?” | Xác định data flow | “Để biết khi nào dữ liệu sẵn sàng cho HR kiểm tra.” | Mất mạng? file trung gian? ai giám sát? | Sơ đồ luồng được phép tham chiếu |
| PRC-05 | Phát hiện ngoại lệ | Bắt buộc | BA | HR/C&B, quản lý | Cách phát hiện thiếu/sai/muộn/sớm | “Ai kiểm tra bất thường, dùng báo cáo nào và thường phát hiện vào thời điểm nào?” | Xác định control | “Để không bỏ sót bước xử lý trước kỳ lương.” | Cảnh báo tự động? ngưỡng? backlog? | Báo cáo mẫu khử định danh |
| PRC-06 | Điều chỉnh | Bắt buộc | BA | HR, nhân viên, quản lý | Luồng đề nghị/sửa công | “Khi quên hoặc sai chấm công, ai tạo đề nghị, cần chứng từ gì và ai được phép sửa?” | Xác định workflow/audit | “Để bảo đảm điều chỉnh có căn cứ và truy vết.” | Sửa hàng loạt? hồi tố? lịch sử thay đổi? | Phiếu điều chỉnh mẫu |
| PRC-07 | Phê duyệt | Bắt buộc | BA | Quản lý, HR | Cấp duyệt, thứ tự, SLA hiện có | “Điều chỉnh hoặc tăng ca qua những cấp nào và trường hợp nào bị trả lại?” | Xác định approval rules | “Để mô tả đúng trách nhiệm và điểm chờ.” | Ủy quyền? quá hạn? mâu thuẫn? | Ma trận/phê duyệt mẫu |
| PRC-08 | Khóa/mở công | Bắt buộc | BA | HR/C&B, payroll | Thời điểm khóa, quyền mở lại | “Bảng công được khóa khi nào, ai khóa, và nếu phát hiện sai sau đó thì ai được mở lại?” | Xác định period control | “Để tránh thay đổi dữ liệu sau khi chuyển tính lương mà không có kiểm soát.” | Audit? thông báo payroll? | Lịch/quy trình khóa công |
| PRC-09 | Xuất dữ liệu/tính lương | Bắt buộc | BA | HR, payroll | Output, format, đối soát, handoff | “Dữ liệu nào được xuất cho tính lương, theo định dạng gì, ai đối soát và xử lý chênh lệch?” | Xác định integration/output | “Để đầu ra chấm công khớp nhu cầu tính lương.” | Import tự động? mapping? thời hạn? | File mẫu rỗng/schema được phép |
| PRC-10 | Lưu trữ/đối soát | Bắt buộc | BA + IT | HR, IT, audit | Lưu trữ, tra cứu, đối soát, thời hạn | “Sau kỳ lương, dữ liệu và bằng chứng được lưu ở đâu, trong bao lâu và ai được tra cứu?” | Xác định retention/audit | “Để ghi nhận yêu cầu kiểm tra lại và bảo vệ dữ liệu.” | Xóa dữ liệu? audit? tranh chấp? | Chính sách/mã tham chiếu |

| ID | Kết quả ghi nhận | Nguồn cung cấp | Trạng thái xác minh | Ảnh hưởng nếu thiếu | Người theo dõi | Hạn bổ sung | Ghi chú |
|---|---|---|---|---|---|---|---|
| PRC-01 | `[ĐIỀN: actor/input/thao tác/công cụ/output/thời gian/vấn đề/ngoại lệ/duyệt]` | `[CHƯA XÁC NHẬN]` | Chưa hỏi | Không hiểu nguồn master nhân sự | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` |
| PRC-02 | `[ĐIỀN: actor/input/thao tác/công cụ/output/thời gian/vấn đề/ngoại lệ/duyệt]` | `[CHƯA XÁC NHẬN]` | Chưa hỏi | Không hiểu cơ sở tính công | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` |
| PRC-03 | `[ĐIỀN: actor/input/thao tác/công cụ/output/thời gian/vấn đề/ngoại lệ/duyệt]` | `[CHƯA XÁC NHẬN]` | Chưa hỏi | Thiếu luồng giao dịch | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` |
| PRC-04 | `[ĐIỀN: actor/input/thao tác/công cụ/output/thời gian/vấn đề/ngoại lệ/duyệt]` | `[CHƯA XÁC NHẬN]` | Chưa hỏi | Không xác định data flow | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` |
| PRC-05 | `[ĐIỀN: actor/input/thao tác/công cụ/output/thời gian/vấn đề/ngoại lệ/duyệt]` | `[CHƯA XÁC NHẬN]` | Chưa hỏi | Không xác định control ngoại lệ | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` |
| PRC-06 | `[ĐIỀN: actor/input/thao tác/công cụ/output/thời gian/vấn đề/ngoại lệ/duyệt]` | `[CHƯA XÁC NHẬN]` | Chưa hỏi | Không truy vết điều chỉnh | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` |
| PRC-07 | `[ĐIỀN: actor/input/thao tác/công cụ/output/thời gian/vấn đề/ngoại lệ/duyệt]` | `[CHƯA XÁC NHẬN]` | Chưa hỏi | Không xác định cấp duyệt | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` |
| PRC-08 | `[ĐIỀN: actor/input/thao tác/công cụ/output/thời gian/vấn đề/ngoại lệ/duyệt]` | `[CHƯA XÁC NHẬN]` | Chưa hỏi | Không kiểm soát kỳ công | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` |
| PRC-09 | `[ĐIỀN: actor/input/thao tác/công cụ/output/thời gian/vấn đề/ngoại lệ/duyệt]` | `[CHƯA XÁC NHẬN]` | Chưa hỏi | Không xác định đầu ra payroll | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` |
| PRC-10 | `[ĐIỀN: actor/input/thao tác/công cụ/output/thời gian/vấn đề/ngoại lệ/duyệt]` | `[CHƯA XÁC NHẬN]` | Chưa hỏi | Không xác định retention/audit | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` |

**Checklist E4:** [ ] Đã đi đủ PRC-01→10; [ ] mỗi bước có actor/input/thao tác/công cụ/output/thời gian/vấn đề/ngoại lệ/phê duyệt/evidence; [ ] các handoff được đọc lại; [ ] quy trình thực tế và quy trình chính thức được phân biệt; [ ] workaround đã ghi là hiện trạng, không mặc nhiên là yêu cầu.

### E5. Quy tắc nghiệp vụ và ngoại lệ

| ID | Nhóm | Mức độ | Người hỏi | Người phù hợp trả lời | Nội dung cần tìm hiểu | Câu hỏi nói với khách hàng | Mục đích nội bộ | Giải thích với khách hàng | Câu hỏi tiếp nối/điều kiện | Evidence cần thu |
|---|---|---|---|---|---|---|---|---|---|---|
| RUL-01 | Ca | Bắt buộc | BA | HR/C&B | Hành chính, xoay, đêm, qua ngày, nghỉ giữa ca | “Anh/chị mô tả cách xác định giờ vào/ra và ngày công cho ca hành chính, xoay ca, ca đêm hoặc qua ngày; nghỉ giữa ca được tính thế nào?” | Bao phủ core rules | “Các loại ca có cách ghép giao dịch khác nhau.” | Ca bắt đầu/kết thúc linh hoạt? đổi ngày? | Quy định ca và ví dụ khử định danh |
| RUL-02 | Muộn/sớm | Bắt buộc | BA | HR/C&B | Đi muộn, về sớm, ngưỡng/làm tròn | “Đi muộn hoặc về sớm được xác định theo ngưỡng nào, có làm tròn hay ngoại lệ không?” | Xác định calculation | “Để kết quả hệ thống không khác quy định đang áp dụng.” | Theo nhóm/ca? cần duyệt? | Chính sách/quy tắc mẫu |
| RUL-03 | Tăng ca | Bắt buộc | BA | HR, quản lý, payroll | Đăng ký, duyệt, tính OT | “Tăng ca được đăng ký, phê duyệt và đối chiếu với giờ chấm như thế nào?” | Xác định workflow/rule | “Để phân biệt thời gian có mặt và thời gian tăng ca được duyệt.” | Trước/sau ca, ngày nghỉ/lễ, qua đêm? | Phiếu/quy định OT |
| RUL-04 | Nghỉ/vắng | Bắt buộc | BA | HR/C&B | Nghỉ phép, lễ, công tác, remote, làm bù | “Nghỉ phép, nghỉ lễ, công tác, làm từ xa và làm bù được đưa vào bảng công từ nguồn nào?” | Xác định nguồn sự kiện | “Để tránh coi thiếu giao dịch là vắng mặt sai.” | Hệ thống phép? duyệt? nửa ngày? | Danh mục mã công/quy trình |
| RUL-05 | Quên/sai chấm | Bắt buộc | BA | HR, vận hành | Quên chấm, chấm sai, chấm nhiều lần | “Khi quên hoặc chấm sai, nhân viên báo thế nào, ai xác minh và giới hạn điều chỉnh ra sao?” | Xác định exception control | “Để điều chỉnh có căn cứ và audit.” | Evidence? hạn gửi? sửa hàng loạt? | Biểu mẫu điều chỉnh |
| RUL-06 | Vòng đời nhân viên | Bắt buộc | BA | HR, IT | Mới vào, nghỉ việc, chuyển đơn vị | “Quyền chấm công được mở, đổi hoặc đóng khi nhân viên vào mới, chuyển đơn vị hoặc nghỉ việc như thế nào?” | Xác định lifecycle | “Để tránh thiếu quyền hoặc còn quyền sau khi nghỉ.” | Hiệu lực hồi tố? đồng bộ master? | Quy trình onboarding/offboarding |
| RUL-07 | Thay đổi ca | Bắt buộc | BA | HR, quản lý | Đổi ca, ca đột xuất, phê duyệt | “Ai được thay đổi ca, thay trước/sau ngày làm việc có được không và ai phê duyệt?” | Xác định rule/audit | “Để kết quả tính công dùng đúng phiên bản ca.” | Quá hạn? lịch sử thay đổi? | Quy trình/phiếu đổi ca |
| RUL-08 | Điều chỉnh/khóa | Bắt buộc | BA | HR, payroll | Điều chỉnh công, khóa, mở lại | “Sau khi khóa bảng công, trường hợp nào được mở lại, ai phê duyệt điều chỉnh công và thông báo cho tính lương ra sao?” | Kiểm soát period close | “Để thay đổi sau chốt được truy vết.” | Mở một người hay cả kỳ? audit? | Biên bản/quy trình |
| RUL-09 | Sự cố | Bắt buộc | Phối hợp | HR, IT, quản lý | Mất mạng, mất điện, hỏng thiết bị | “Khi mất mạng, mất điện hoặc thiết bị hỏng, nhân viên chấm thế nào và dữ liệu được bù/đối soát ra sao?” | Xác định continuity | “Để không mất công và biết trách nhiệm khôi phục.” | Offline capacity? giấy/Excel? ai nhập lại? | Quy trình sự cố/log mẫu |
| RUL-10 | Ưu tiên/xung đột | Nên có | PM/Dev + BA | HR, sponsor | Rule khác nhau/mâu thuẫn | “Nếu quy định giữa cơ sở hoặc bộ phận khác nhau, quy tắc nào được ưu tiên và ai quyết định?” | Xác định hierarchy | “Để đội dự án không tự chọn quy tắc.” | Văn bản nào có hiệu lực? ngày hiệu lực? | Chính sách/quyết định |

| ID | Kết quả ghi nhận | Nguồn cung cấp | Trạng thái xác minh | Ảnh hưởng nếu thiếu | Người theo dõi | Hạn bổ sung | Ghi chú |
|---|---|---|---|---|---|---|---|
| RUL-01 | `[ĐIỀN]` | `[CHƯA XÁC NHẬN]` | Chưa hỏi | Không xác định logic ca | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` |
| RUL-02 | `[ĐIỀN]` | `[CHƯA XÁC NHẬN]` | Chưa hỏi | Không tính muộn/sớm đúng | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` |
| RUL-03 | `[ĐIỀN]` | `[CHƯA XÁC NHẬN]` | Chưa hỏi | Không xác định OT | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` |
| RUL-04 | `[ĐIỀN]` | `[CHƯA XÁC NHẬN]` | Chưa hỏi | Sai công khi không có giao dịch | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` |
| RUL-05 | `[ĐIỀN]` | `[CHƯA XÁC NHẬN]` | Chưa hỏi | Thiếu kiểm soát điều chỉnh | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` |
| RUL-06 | `[ĐIỀN]` | `[CHƯA XÁC NHẬN]` | Chưa hỏi | Sai quyền/vòng đời dữ liệu | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` |
| RUL-07 | `[ĐIỀN]` | `[CHƯA XÁC NHẬN]` | Chưa hỏi | Dùng sai lịch ca | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` |
| RUL-08 | `[ĐIỀN]` | `[CHƯA XÁC NHẬN]` | Chưa hỏi | Thay đổi sau chốt không kiểm soát | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` |
| RUL-09 | `[ĐIỀN]` | `[CHƯA XÁC NHẬN]` | Chưa hỏi | Không có phương án continuity | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` |
| RUL-10 | `[ĐIỀN]` | `[CHƯA XÁC NHẬN]` | Chưa hỏi | Không xử lý được rule conflict | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` |

**Checklist E5:** [ ] Hành chính/xoay/đêm/qua ngày/nghỉ giữa ca; [ ] muộn/sớm/OT; [ ] phép/lễ/công tác/remote/làm bù; [ ] quên/sai chấm; [ ] nhân viên mới/nghỉ; [ ] đổi ca/điều chỉnh/khóa/mở; [ ] mất mạng/điện/hỏng thiết bị; [ ] mỗi rule có nguồn, hiệu lực, người duyệt và ví dụ.

### E6. Phần mềm hiện có và Fit–Gap

| ID | Nhóm | Mức độ | Người hỏi | Người phù hợp trả lời | Nội dung cần tìm hiểu | Câu hỏi nói với khách hàng | Mục đích nội bộ | Giải thích với khách hàng | Câu hỏi tiếp nối/điều kiện | Evidence cần thu |
|---|---|---|---|---|---|---|---|---|---|---|
| FUN-01 | Chức năng | Bắt buộc | PM/Dev + BA | HR, vận hành | Must-have/nice-to-have | “Trong các tác vụ đã nêu, chức năng nào bắt buộc để vận hành và chức năng nào là mong muốn cải thiện?” | Phân ưu tiên | “Để đánh giá đúng phần thiết yếu trước.” | Ai xác nhận ưu tiên? hậu quả nếu thiếu? | Danh sách yêu cầu có nguồn |
| FUN-02 | Báo cáo | Bắt buộc | BA | HR, payroll, quản lý | Báo cáo/biểu mẫu | “Mỗi vai trò cần xem hoặc xuất báo cáo nào, vào thời điểm nào và dùng để quyết định gì?” | Xác định output | “Để báo cáo phục vụ đúng người và đúng mục đích.” | Cột, lọc, kỳ, phê duyệt? | Mẫu rỗng/đã khử định danh |
| FUN-03 | Phân quyền/audit | Bắt buộc | BA + PM/Dev | HR, IT, security | Role, phạm vi dữ liệu, lịch sử thay đổi | “Ai được xem, tạo, sửa, duyệt và xuất dữ liệu; có cần xem lịch sử thay đổi không?” | Đánh giá authorization/audit | “Để bảo vệ dữ liệu và truy vết thay đổi.” | Tách nhiệm vụ? cấp tạm? | Ma trận quyền/chính sách |
| FUN-04 | Import/export | Bắt buộc | BA | HR, payroll, IT | Định dạng, tần suất, khối lượng | “Hiện cần nhập hoặc xuất dữ liệu gì, theo file nào, bao lâu một lần và ai kiểm tra?” | Xác định interface | “Để kiểm tra khả năng dùng chức năng có sẵn hoặc cấu hình.” | Mapping/lỗi/trùng? | Schema/file mẫu rỗng |
| FUN-05 | Thông báo/phê duyệt | Nên có | BA | HR, quản lý, người dùng | Alert, kênh, quy trình phê duyệt | “Ai cần được nhắc về ngoại lệ hoặc yêu cầu chờ duyệt, qua kênh nào và khi nào?” | Xác định notification | “Để tránh thông báo thừa hoặc bỏ sót việc.” | Escalation? opt-out? | Quy tắc thông báo |
| FUN-06 | Kênh sử dụng | Có điều kiện | PM/Dev + BA | Người dùng, IT | Web/mobile/kiosk | “Nhóm người dùng nào cần web, điện thoại hoặc kiosk, và họ dùng trong tình huống nào?” | Đánh giá channel fit | “Mỗi kênh có điều kiện sử dụng và bảo mật khác nhau.” | Nếu mobile: thiết bị cá nhân? mạng? MDM? | Use case/chính sách |
| FUN-07 | Tích hợp/API | Có điều kiện | PM/Dev + Hạ tầng | IT, owner hệ thống | Hệ thống liên quan/API | “Hệ thống nào cần trao đổi dữ liệu với chấm công, dữ liệu gì và hệ thống nào là nguồn chuẩn?” | Xác định dependency | “Để kiểm tra giao diện sẵn có và trách nhiệm hai phía.” | Owner, tần suất, lỗi, môi trường test? | Tài liệu API/schema được phép |
| FUN-08 | Giao diện/biểu mẫu riêng | Nên có | BA | HR, vận hành | Branding/form/layout | “Có biểu mẫu hoặc màn hình nào cần theo mẫu riêng? Mục đích nghiệp vụ của khác biệt đó là gì?” | Phân biệt nhu cầu/giải pháp | “Để kiểm tra có thể cấu hình hay cần đánh giá thêm.” | Bắt buộc pháp lý hay sở thích? | Mẫu minh họa |
| FUN-09 | Đối chiếu phần mềm | Bắt buộc | PM/Dev | Owner sản phẩm, BA | Mức đáp ứng hiện tại | “Chúng tôi đã ghi nhu cầu; sau buổi làm việc đội dự án sẽ đối chiếu chức năng và cấu hình hiện có. Có tình huống nào cần ưu tiên kiểm tra hoặc demo?” | Fit–Gap có evidence | “Để không kết luận custom trước khi kiểm tra sản phẩm.” | Demo scenario/data test? | Screenshot/manual/test result được phép |

| ID | Kết quả ghi nhận | Nguồn cung cấp | Trạng thái xác minh | Ảnh hưởng nếu thiếu | Người theo dõi | Hạn bổ sung | Ghi chú/phân loại ban đầu |
|---|---|---|---|---|---|---|---|
| FUN-01 | `[ĐIỀN]` | `[CHƯA XÁC NHẬN]` | Chưa hỏi | Không phân được must/nice | `[ĐIỀN]` | `[ĐIỀN]` | Chưa đủ thông tin |
| FUN-02 | `[ĐIỀN]` | `[CHƯA XÁC NHẬN]` | Chưa hỏi | Thiếu output/report | `[ĐIỀN]` | `[ĐIỀN]` | Chưa đủ thông tin |
| FUN-03 | `[ĐIỀN]` | `[CHƯA XÁC NHẬN]` | Chưa hỏi | Thiếu phân quyền/audit | `[ĐIỀN]` | `[ĐIỀN]` | Chưa đủ thông tin |
| FUN-04 | `[ĐIỀN]` | `[CHƯA XÁC NHẬN]` | Chưa hỏi | Không đánh giá import/export | `[ĐIỀN]` | `[ĐIỀN]` | Chưa đủ thông tin |
| FUN-05 | `[ĐIỀN]` | `[CHƯA XÁC NHẬN]` | Chưa hỏi | Không đánh giá alert/workflow | `[ĐIỀN]` | `[ĐIỀN]` | Chưa đủ thông tin |
| FUN-06 | `[ĐIỀN]` | `[CHƯA XÁC NHẬN]` | Chưa hỏi | Không xác định channel | `[ĐIỀN]` | `[ĐIỀN]` | Chưa đủ thông tin |
| FUN-07 | `[ĐIỀN]` | `[CHƯA XÁC NHẬN]` | Chưa hỏi | Không đánh giá integration | `[ĐIỀN]` | `[ĐIỀN]` | Có thể cần tích hợp — `[CHƯA CAM KẾT]` |
| FUN-08 | `[ĐIỀN]` | `[CHƯA XÁC NHẬN]` | Chưa hỏi | Không hiểu mục đích tùy biến | `[ĐIỀN]` | `[ĐIỀN]` | Có thể cấu hình/cần kiểm tra thêm |
| FUN-09 | `[ĐIỀN]` | `[CHƯA XÁC NHẬN]` | Chưa hỏi | Không có Fit–Gap có evidence | `[ĐIỀN]` | `[ĐIỀN]` | Chưa đủ thông tin |

Phân loại Fit–Gap ban đầu chỉ được dùng một trong: `Có sẵn`, `Có thể đáp ứng bằng cấu hình`, `Cần kiểm tra thêm`, `Có thể cần custom`, `Có thể cần tích hợp`, `Ngoài phạm vi hiện tại`, `Chưa đủ thông tin`. Không ghi `Cần custom` khi chưa kiểm tra chức năng và cấu hình hiện có.

**Checklist E6:** [ ] Must-have/nice-to-have có người xác nhận; [ ] báo cáo/phân quyền/import-export/audit/thông báo/kênh/phê duyệt; [ ] integration/API có owner; [ ] mọi nhu cầu có use case và giá trị; [ ] mức đáp ứng có evidence; [ ] chưa kết luận custom.

## F — Ma trận Fit–Gap và yêu cầu custom

| Requirement ID | Mô tả nhu cầu | Người dùng | Tình huống sử dụng | Giá trị mong đợi | Ưu tiên | Chức năng liên quan | Mức đáp ứng hiện tại | Bằng chứng kiểm tra | Cấu hình cần thiết | Khả năng cần custom | Phụ thuộc | Rủi ro | Người có quyền xác nhận | Trạng thái đánh giá | Quyết định tiếp theo |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| REQ-001 | `[ĐIỀN; tham chiếu BUS/FUN/PRC/RUL ID]` | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` | `[CHƯA XÁC NHẬN]` | `[ĐIỀN]` | Chưa đủ thông tin | `[ĐIỀN EVIDENCE]` | `[CHƯA XÁC NHẬN]` | `[CHƯA CAM KẾT CUSTOM]` | `[ĐIỀN]` | `[ĐIỀN]` | `[CHƯA XÁC NHẬN]` | Chưa đánh giá | Kiểm tra chức năng/cấu hình hiện có |
| REQ-002 | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` | `[CHƯA XÁC NHẬN]` | `[ĐIỀN]` | Chưa đủ thông tin | `[ĐIỀN EVIDENCE]` | `[CHƯA XÁC NHẬN]` | `[CHƯA CAM KẾT CUSTOM]` | `[ĐIỀN]` | `[ĐIỀN]` | `[CHƯA XÁC NHẬN]` | Chưa đánh giá | `[ĐIỀN]` |
| REQ-003 | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` | `[CHƯA XÁC NHẬN]` | `[ĐIỀN]` | Chưa đủ thông tin | `[ĐIỀN EVIDENCE]` | `[CHƯA XÁC NHẬN]` | `[CHƯA CAM KẾT CUSTOM]` | `[ĐIỀN]` | `[ĐIỀN]` | `[CHƯA XÁC NHẬN]` | Chưa đánh giá | `[ĐIỀN]` |
| REQ-004 | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` | `[CHƯA XÁC NHẬN]` | `[ĐIỀN]` | Chưa đủ thông tin | `[ĐIỀN EVIDENCE]` | `[CHƯA XÁC NHẬN]` | `[CHƯA CAM KẾT CUSTOM]` | `[ĐIỀN]` | `[ĐIỀN]` | `[CHƯA XÁC NHẬN]` | Chưa đánh giá | `[ĐIỀN]` |
| REQ-005 | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` | `[CHƯA XÁC NHẬN]` | `[ĐIỀN]` | Chưa đủ thông tin | `[ĐIỀN EVIDENCE]` | `[CHƯA XÁC NHẬN]` | `[CHƯA CAM KẾT CUSTOM]` | `[ĐIỀN]` | `[ĐIỀN]` | `[CHƯA XÁC NHẬN]` | Chưa đánh giá | `[ĐIỀN]` |

**Câu phản hồi chuẩn khi khách hàng đề nghị custom**

> Đội dự án đã ghi nhận nhu cầu này cùng tình huống sử dụng và giá trị mong đợi. Chúng tôi cần đối chiếu chức năng, khả năng cấu hình và các phụ thuộc hiện có trước khi kết luận. Vì vậy nội dung hiện được gắn nhãn **[CHƯA CAM KẾT CUSTOM]**; PM sẽ phản hồi qua đầu mối được thống nhất sau khi có đánh giá và phê duyệt cần thiết.

**Checklist F:** [ ] Mỗi requirement có nguồn, người dùng, use case và giá trị; [ ] ưu tiên do người có thẩm quyền xác nhận; [ ] đã kiểm tra chức năng/cấu hình bằng evidence; [ ] phụ thuộc/rủi ro có owner; [ ] mức đáp ứng dùng đúng nhãn; [ ] mọi custom vẫn `[CHƯA CAM KẾT CUSTOM]`; [ ] quyết định tiếp theo có người phụ trách và hạn.

## G — Thiết bị và khảo sát thực địa

| ID | Mức độ | Người hỏi | Người trả lời | Câu hỏi nói với khách hàng | Mục đích/giải thích | Tiếp nối | Evidence được phép | Kết quả/nguồn/trạng thái | Ảnh hưởng nếu thiếu | Theo dõi/hạn |
|---|---|---|---|---|---|---|---|---|---|---|
| DEV-01 | Bắt buộc | Hạ tầng/Network | IT, quản lý thiết bị | “Thiết bị nào đã có, thiết bị nào dự kiến cung cấp, ai sở hữu và quản lý?” | Xác định inventory/phạm vi; tránh giả định thiết bị có sẵn | Số lượng theo vị trí? dự phòng? bảo hành? | Danh mục model đã khử định danh | `[ĐIỀN] / [CHƯA XÁC NHẬN] / Chưa hỏi` | Không xác định inventory | `[ĐIỀN]/[ĐIỀN]` |
| DEV-02 | Bắt buộc | Hạ tầng/Network | IT/vendor được phép | “Anh/chị có thể xác nhận hãng, model và phiên bản firmware theo tài liệu được phép không?” | Kiểm tra tương thích; firmware là phần mềm bên trong thiết bị | Nếu khác phiên bản: nhóm theo lô | Datasheet/inventory; serial chỉ ghi khi được phép và không đưa vào Git công khai | `[ĐIỀN]` | Không đánh giá tương thích | `[ĐIỀN]/[ĐIỀN]` |
| DEV-03 | Bắt buộc | PM/Dev + Hạ tầng | IT | “Thiết bị nhận diện bằng thẻ, vân tay, khuôn mặt hay phương thức nào?” | Xác định luồng và rủi ro quyền riêng tư | Nếu sinh trắc học: chuyển I-03, không tiếp cận dữ liệu nếu chưa phê duyệt | Datasheet/chính sách | `[ĐIỀN]` | Không xác định data/privacy scope | `[ĐIỀN]/[ĐIỀN]` |
| DEV-04 | Bắt buộc | Hạ tầng/Network | IT/vendor | “Thiết bị hỗ trợ SDK, API hoặc giao thức nào và dữ liệu được lấy bằng cách nào?” | Đánh giá tích hợp; giải thích API/SDK là giao diện kỹ thuật để phần mềm giao tiếp | Push/pull/file? mã hóa? owner tài liệu? | Tài liệu kỹ thuật được phép | `[ĐIỀN]` | Không đánh giá kết nối | `[ĐIỀN]/[ĐIỀN]` |
| DEV-05 | Bắt buộc | Hạ tầng/Network | IT/vendor | “Khi mất kết nối, thiết bị có tiếp tục ghi nhận không và lưu được khoảng bao nhiêu giao dịch?” | Đánh giá offline/continuity | Đồng bộ lại thế nào? trùng/mất dữ liệu? | Datasheet/test được phép | `[ĐIỀN]` | Không biết rủi ro mất dữ liệu | `[ĐIỀN]/[ĐIỀN]` |
| DEV-06 | Bắt buộc | Hạ tầng/Network | Quản lý cơ sở, IT | “Vị trí lắp dự kiến ở đâu; trong nhà hay ngoài trời; chiều cao, ánh sáng, nhiệt/ẩm/bụi có gì cần lưu ý?” | Kiểm tra điều kiện vật lý và khả năng sử dụng | Nắng/mưa/ngược sáng/rung? accessibility? | Ảnh/sơ đồ chỉ khi có phép; tham chiếu access-controlled | `[ĐIỀN]` | Không xác định khả năng lắp đặt | `[ĐIỀN]/[ĐIỀN]` |
| DEV-07 | Bắt buộc | Hạ tầng/Network | Facility/IT | “Tại vị trí đó có nguồn điện ổn định và UPS không; ổ cắm/cáp cách bao xa?” | Xác định nguồn và dự phòng | Mất điện bao lâu? ai phụ trách? | Sơ đồ/quan sát có phép | `[ĐIỀN]` | Không đánh giá nguồn | `[ĐIỀN]/[ĐIỀN]` |
| DEV-08 | Bắt buộc | Hạ tầng/Network | Network | “Đường mạng đến vị trí dùng cáp hay Wi‑Fi, khoảng cách và vùng mạng dự kiến là gì?” | Xác định kết nối; không yêu cầu IP cụ thể trong Git | Nếu Wi‑Fi: phủ sóng/roaming; nếu cáp: port/switch? | Mô tả đã khử nhạy cảm | `[ĐIỀN]` | Không đánh giá connectivity | `[ĐIỀN]/[ĐIỀN]` |
| DEV-09 | Bắt buộc | BA + Hạ tầng | Vận hành | “Giờ cao điểm tại vị trí này có bao nhiêu người; có xếp hàng hoặc yêu cầu kiểm soát cửa không?” | Đánh giá throughput và tương tác access control | Nếu kiểm soát cửa: fail-safe, owner, dependency? | Quan sát/số liệu khử định danh | `[ĐIỀN]` | Không đánh giá công suất/an toàn | `[ĐIỀN]/[ĐIỀN]` |
| DEV-10 | Nên có | Hạ tầng/Network | IT, quản lý cơ sở | “Ai quản lý thiết bị, theo dõi lỗi, cập nhật firmware và cho phép thao tác kỹ thuật?” | Xác định ownership/change control | Vendor hỗ trợ? nhật ký thay đổi? | RACI/quy trình | `[ĐIỀN]` | Không có owner vận hành | `[ĐIỀN]/[ĐIỀN]` |

### G1. Phiếu kiểm kê theo vị trí

| Mã vị trí | Hãng/model | Firmware | Serial được phép ghi? | Nhận diện | SDK/API/giao thức | Offline/dung lượng | Vị trí/chiều cao/môi trường | Nguồn/UPS | Mạng/khoảng cách | Lưu lượng/kiểm soát cửa | Owner | Trạng thái |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| LOC-01 | `[ĐIỀN]` | `[ĐIỀN]` | `[KHÔNG GHI TRONG GIT CÔNG KHAI]` | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` | `[CHƯA XÁC NHẬN]` |
| LOC-02 | `[ĐIỀN]` | `[ĐIỀN]` | `[KHÔNG GHI TRONG GIT CÔNG KHAI]` | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` | `[CHƯA XÁC NHẬN]` |

### G2. Xin phép trước thao tác

| Thao tác | Có phê duyệt? | Người có thẩm quyền | Phạm vi/điều kiện | Evidence phê duyệt | Kết quả |
|---|---|---|---|---|---|
| Chụp ảnh hiện trạng | `[CHƯA XÁC NHẬN]` | `[ĐIỀN]` | Không chụp người/dữ liệu/màn hình nhạy cảm | `[THAM CHIẾU]` | Không thực hiện nếu chưa phép |
| Ghi lại cấu hình | `[CHƯA XÁC NHẬN]` | `[ĐIỀN]` | Chỉ trường không nhạy cảm, lưu đúng nơi được phép | `[THAM CHIẾU]` | Không thực hiện nếu chưa phép |
| Kết nối thử | `[CHƯA XÁC NHẬN]` | `[ĐIỀN]` | Phạm vi, cửa sổ, giám sát, rollback | `[THAM CHIẾU]` | Không thực hiện trong Discovery nếu chưa phê duyệt riêng |
| Quét mạng | `[CHƯA XÁC NHẬN]` | `[ĐIỀN]` | Phê duyệt bảo mật riêng | `[THAM CHIẾU]` | Không thực hiện nếu chưa phép |
| Cắm thiết bị | `[CHƯA XÁC NHẬN]` | `[ĐIỀN]` | Đúng port/vùng mạng/giám sát | `[THAM CHIẾU]` | Không thực hiện nếu chưa phép |
| Sao chép file | `[CHƯA XÁC NHẬN]` | `[ĐIỀN]` | Phân loại, khử định danh, kênh chuyển | `[THAM CHIẾU]` | Không sao chép vào Git công khai |
| Tiếp cận dữ liệu sinh trắc học | `[CHƯA XÁC NHẬN]` | `[ĐIỀN]` | Phê duyệt privacy/security riêng, tối thiểu hóa dữ liệu | `[THAM CHIẾU]` | Mặc định không tiếp cận |

**Checklist G:** [ ] DEV-01–10; [ ] inventory theo vị trí; [ ] nguồn/UPS/mạng/môi trường/lưu lượng; [ ] SDK/API/offline; [ ] owner thiết bị; [ ] mọi ảnh/kết nối/quét/cắm/sao chép/sinh trắc học có phê duyệt riêng; [ ] không ghi serial/dữ liệu nhạy cảm vào Git công khai.

## H — Hạ tầng và network

| ID | Mức độ | Câu hỏi nói với khách hàng | Lý do kỹ thuật nội bộ | Giải thích dễ hiểu | Evidence cần lấy | Cách xác nhận | Ảnh hưởng nếu thiếu | Phụ trách | Trạng thái |
|---|---|---|---|---|---|---|---|---|---|
| NET-01 | Bắt buộc | “Mô hình mong muốn là cloud, đặt tại đơn vị (on-premise) hay kết hợp? Nội dung này đã được ai quyết định?” | Xác định deployment boundary | “Mỗi mô hình có trách nhiệm vận hành và kết nối khác nhau.” | Quyết định/kiến trúc được phép tham chiếu | Owner kiến trúc xác nhận; nếu chưa, `[CHƯA XÁC NHẬN]` | Chặn kiến trúc và bảo mật | Hạ tầng + PM | Chưa hỏi |
| NET-02 | Bắt buộc | “Máy chủ hoặc máy trạm dự kiến dùng hệ điều hành và tài nguyên CPU/RAM/disk nào?” | Đánh giá compatibility/capacity | “Để kiểm tra điều kiện chạy phần mềm, chưa phải cấu hình cam kết.” | Inventory khử nhạy cảm | IT xác nhận + evidence | Chặn đánh giá hosting | Hạ tầng | Chưa hỏi |
| NET-03 | Bắt buộc | “Thiết bị và máy trạm dùng LAN hay Wi‑Fi; chất lượng kết nối tại các vị trí ra sao?” | Đánh giá link/reliability | “Kết nối ổn định giúp tránh chậm hoặc gián đoạn dữ liệu.” | Survey/mô tả được phép | Quan sát có phép + IT | Chưa đánh giá connectivity | Hạ tầng | Chưa hỏi |
| NET-04 | Bắt buộc | “Địa chỉ được cấp tự động (DHCP) hay dùng IP tĩnh; thiết bị nằm trong vùng VLAN nào theo mã đã khử nhạy cảm?” | Đánh giá addressing/segmentation | “Để thiết bị nhận đúng địa chỉ và nằm đúng vùng mạng.” | Mô tả/mã vùng không nhạy cảm | Network owner xác nhận | Chặn thiết kế kết nối | Hạ tầng | Chưa hỏi |
| NET-05 | Bắt buộc | “Có yêu cầu DNS, gateway hoặc định tuyến đặc biệt giữa thiết bị và server không?” | Xác định name resolution/routing | “Để hai đầu tìm thấy và giao tiếp được với nhau.” | Sơ đồ logic đã làm sạch | Network owner xác nhận | Không xác định đường truyền | Hạ tầng | Chưa hỏi |
| NET-06 | Bắt buộc | “Firewall hoặc proxy kiểm soát kết nối thế nào; quy trình đề nghị mở cổng kết nối là gì?” | Xác định egress/ingress/change | “Chúng tôi chỉ cần biết quy trình và luồng cần đánh giá, không cần mật khẩu hay secret.” | Chính sách/quy trình; không ghi port/IP nhạy cảm trong Git | Security/network phê duyệt riêng | Chặn kết nối/tích hợp | Hạ tầng | Chưa hỏi |
| NET-07 | Có điều kiện | “Kết nối Internet có ổn định và có giới hạn nào cho hệ thống này?” | Đánh giá cloud/sync dependency | “Nếu giải pháp cần Internet, giới hạn này ảnh hưởng đồng bộ và hỗ trợ.” | Chỉ số/monitoring được phép | IT xác nhận | Chặn mô hình cần Internet | Hạ tầng | Chưa hỏi |
| NET-08 | Có điều kiện | “Nếu cần VPN hoặc hỗ trợ từ xa, chính sách phê duyệt, thời gian và giám sát là gì?” | Xác định remote access control | “Để hỗ trợ đúng quy định; chưa đề nghị cấp quyền hôm nay.” | Policy/process | Security owner xác nhận | Chặn remote support | Hạ tầng | Chưa hỏi |
| NET-09 | Bắt buộc | “Các cơ sở kết nối với nhau bằng cách nào và khi đường liên cơ sở gián đoạn thì vận hành ra sao?” | Đánh giá WAN/continuity | “Để biết dữ liệu có thể bị chậm hoặc cần cơ chế offline.” | Sơ đồ logic/sự cố mẫu khử nhạy cảm | Network owner + evidence | Không đánh giá multi-site | Hạ tầng | Chưa hỏi |
| NET-10 | Bắt buộc | “Máy chấm công và server dự kiến nằm ở vùng mạng nào; luồng giữa các vùng do ai phê duyệt?” | Xác định segmentation/authority | “Để bảo đảm kết nối đúng vùng và đúng người phê duyệt.” | Zone mapping đã làm sạch | Security/network owner | Chặn security design | Hạ tầng | Chưa hỏi |
| NET-11 | Bắt buộc | “Ai có quyền quản trị, cài đặt và thay đổi cấu hình trên server, máy trạm và thiết bị?” | Xác định privilege/change ownership | “Để đội dự án không thao tác vượt quyền.” | RACI/quy trình cấp quyền | Owner hệ thống xác nhận | Chặn cài đặt/vận hành | Hạ tầng | Chưa hỏi |
| NET-12 | Nên có | “Hệ thống và kết nối được giám sát, lưu log và cảnh báo như thế nào?” | Đánh giá observability | “Để phát hiện và điều tra gián đoạn.” | Monitoring/log policy; không lấy production log | IT xác nhận | Khó hỗ trợ/sự cố | Hạ tầng | Chưa hỏi |
| NET-13 | Bắt buộc | “Backup thực hiện cho thành phần nào, tần suất ra sao và lần khôi phục gần nhất được kiểm chứng khi nào?” | Đánh giá recoverability | “Backup chỉ có giá trị khi có thể khôi phục; chúng tôi không cần dữ liệu backup.” | Policy/test result đã khử nhạy cảm | Owner backup xác nhận | Chặn readiness dữ liệu | Hạ tầng | Chưa hỏi |
| NET-14 | Có điều kiện | “Có yêu cầu dự phòng/HA không; mục tiêu phục hồi đã được phê duyệt chưa?” | Đánh giá availability requirement | “HA là cơ chế duy trì dịch vụ khi một thành phần lỗi; cần mục tiêu được duyệt.” | BCP/decision | Authority xác nhận | Không đánh giá availability | Hạ tầng + PM | Chưa hỏi |
| NET-15 | Bắt buộc | “Có môi trường test riêng với production không; ai cấp quyền và dữ liệu test được chuẩn bị thế nào?” | Tách môi trường/giảm rủi ro | “Để kiểm tra mà không tác động vận hành thật.” | Environment/process | IT/security xác nhận | Chặn kiểm thử an toàn | Hạ tầng | Chưa hỏi |
| NET-16 | Bắt buộc | “Quy trình đề nghị quyền và thay đổi cấu hình gồm bước nào, ai duyệt và cần thời gian chuẩn bị bao lâu?” | Xác định lead time/change control | “Để lập đầu việc đúng quy trình, không phải cam kết tiến độ.” | Request/change procedure | Process owner xác nhận | Không lập được dependency | Hạ tầng + PM | Chưa hỏi |

> Không yêu cầu hoặc ghi mật khẩu, private key, token, secret, chuỗi kết nối, IP/hostname nội bộ cụ thể hoặc ảnh chụp cấu hình nhạy cảm.

**Checklist H:** [ ] NET-01–16; [ ] cloud/on-premise/hybrid có thẩm quyền; [ ] server/workstation/OS/CPU/RAM/disk; [ ] LAN/Wi‑Fi/DHCP/static/VLAN/DNS/gateway; [ ] firewall/proxy/Internet/VPN; [ ] liên cơ sở/vùng mạng; [ ] quyền/log/monitoring; [ ] backup/restore/HA; [ ] test/production; [ ] cấp quyền/change control; [ ] không thu credential/secret; [ ] item thiếu có impact, owner, hạn.

## I — Dữ liệu, tích hợp, bảo mật và quyền riêng tư

| ID | Mức độ | Người hỏi | Người trả lời | Câu hỏi nói với khách hàng | Mục đích/giải thích | Tiếp nối | Evidence | Phân loại ghi nhận | Kết quả/trạng thái/ảnh hưởng/owner/hạn |
|---|---|---|---|---|---|---|---|---|---|
| DAT-01 | Bắt buộc | BA | HR, data owner | “Những trường dữ liệu nhân viên nào thực sự cần cho chấm công và hệ thống nào là nguồn chuẩn?” | Tối thiểu hóa dữ liệu và xác định master | Mã nhân viên duy nhất? đổi mã? owner? | Data dictionary khử định danh | Có thể ghi: tên trường/mục đích; không ghi bản ghi thật | `[ĐIỀN]/Chưa hỏi/[ĐIỀN]/[ĐIỀN]/[ĐIỀN]` |
| DAT-02 | Bắt buộc | BA + IT | HR, IT | “Dữ liệu chấm công và lịch sử hiện có gồm giai đoạn nào, chất lượng và khối lượng ra sao?” | Đánh giá migration/retention | Thiếu/trùng/sai/timezone? | Profile thống kê không định danh | Chỉ xác nhận tại chỗ nếu chứa chi tiết nhạy cảm | `[ĐIỀN]` |
| DAT-03 | Có điều kiện | PM + Security | Privacy/data owner | “Có dùng dữ liệu sinh trắc học không; mục đích, căn cứ, thời hạn lưu, quyền truy cập và cơ chế xóa đã được phê duyệt thế nào?” | Dữ liệu nhạy cảm cần kiểm soát riêng | Template hay ảnh gốc? lưu ở đâu? consent/notice? | Chỉ mã policy/approval | Không sao chép; cần phê duyệt riêng trước tiếp cận | `[ĐIỀN]` |
| DAT-04 | Bắt buộc | BA | HR, payroll | “Đơn vị nhập/xuất dữ liệu theo định dạng nào, ai tạo, ai kiểm tra và xử lý lỗi ra sao?” | Xác định interface/data quality | CSV/XLSX/API? encoding? mapping? | Schema/file mẫu rỗng | Có thể ghi cấu trúc đã làm sạch | `[ĐIỀN]` |
| DAT-05 | Có điều kiện | PM/Dev + BA | IT, owner hệ thống | “Cần đồng bộ với HRM, payroll hoặc ERP nào; chiều dữ liệu, tần suất và nguồn chuẩn là gì?” | Xác định integration scope | Realtime/batch? create/update/delete? | Context diagram/API docs được phép | Chi tiết endpoint/credential không ghi/sao chép | `[ĐIỀN]` |
| DAT-06 | Có điều kiện | PM/Dev + Hạ tầng | IT | “API hoặc cơ chế trao đổi hiện có xử lý xác thực, lỗi, retry và dữ liệu trùng thế nào?” | Đánh giá reliability/security | Rate limit? idempotency? monitoring? | Tài liệu đã loại secret | Chỉ xác nhận tại chỗ nếu nhạy cảm | `[ĐIỀN]` |
| DAT-07 | Bắt buộc | BA + Security | Data owner | “Dữ liệu phải lưu bao lâu, ở môi trường nào và khi hết hạn hoặc có yêu cầu xóa thì xử lý ra sao?” | Retention/deletion compliance | Backup có xóa theo? legal hold? | Policy/decision | Có thể ghi mã chính sách; không ghi dữ liệu | `[ĐIỀN]` |
| DAT-08 | Bắt buộc | BA + IT | Security, data owner | “Vai trò nào được xem/sửa/xuất dữ liệu và việc truy cập có được ghi audit log không?” | Authorization/audit | Cấp/thu hồi/soát quyền định kỳ? | Access matrix/policy | Không ghi tài khoản cá nhân | `[ĐIỀN]` |
| DAT-09 | Bắt buộc | PM + Security | Data owner | “Loại dữ liệu nào được phép đưa ra ngoài, loại nào chỉ xem tại chỗ, không được sao chép hoặc cần phê duyệt truy cập riêng?” | Lập handling rule | Kênh truyền/lưu nào được phép? | Classification policy | Gắn: ghi biên bản / tại chỗ / không sao chép / phê duyệt riêng | `[ĐIỀN]` |
| DAT-10 | Bắt buộc | PM + Security | Security/IT | “Khi có sự cố dữ liệu, ai tiếp nhận, ai quyết định thông báo sự cố và quy trình escalation là gì?” | Incident ownership | Thời hạn theo policy? evidence cần giữ? | Incident process | Chỉ ghi quy trình đã khử nhạy cảm | `[ĐIỀN]` |

### I1. Quy tắc xử lý thông tin

| Loại | Được ghi vào biên bản công khai? | Cách xử lý |
|---|---|---|
| Thông tin có thể ghi | Chỉ khi đã khử định danh và được phép | Ghi mã nguồn/evidence, owner theo vai trò, trạng thái xác minh |
| Chỉ xác nhận tại chỗ | Không ghi chi tiết | Ghi “đã xem tại chỗ”, người có thẩm quyền và kết luận tối thiểu |
| Không được sao chép | Không | Không chụp/tải/copy; chỉ ghi hạn chế xử lý |
| Cần phê duyệt riêng | Không cho đến khi được phê duyệt | Ghi người phê duyệt, phạm vi, điều kiện, thời hạn; không coi im lặng là đồng ý |

**Checklist I:** [ ] Nhân viên/chấm công/sinh trắc học/lịch sử; [ ] nguồn chuẩn/data owner/mã nhân viên; [ ] import/export/chất lượng; [ ] HRM/payroll/ERP/API/tần suất/trùng-sai; [ ] retention/backup/xóa; [ ] phân quyền/audit; [ ] quy tắc đưa dữ liệu ra ngoài; [ ] incident notification; [ ] không sao chép dữ liệu nhạy cảm; [ ] mọi truy cập có approval.

## J — Vận hành, đào tạo, hỗ trợ và bàn giao

| ID | Mức độ | Người hỏi | Người trả lời | Câu hỏi nói với khách hàng | Mục đích/giải thích | Tiếp nối | Evidence | Kết quả/nguồn/trạng thái | Ảnh hưởng nếu thiếu | Owner/hạn |
|---|---|---|---|---|---|---|---|---|---|---|
| OPS-01 | Bắt buộc | BA | HR, IT | “Ai quản trị hệ thống, quản lý nhân viên và tạo ca; có người dự phòng không?” | Xác định operating roles | Phân theo cơ sở? cấp/thu hồi quyền? | RACI | `[ĐIỀN]/[CHƯA XÁC NHẬN]/Chưa hỏi` | Không có ownership | `[ĐIỀN]/[ĐIỀN]` |
| OPS-02 | Bắt buộc | BA | HR, quản lý | “Ai kiểm tra công, xử lý lỗi và phê duyệt điều chỉnh ở từng bước?” | Xác định support/approval flow | Quá hạn/escalation? | Quy trình | `[ĐIỀN]` | Không vận hành ngoại lệ | `[ĐIỀN]/[ĐIỀN]` |
| OPS-03 | Bắt buộc | BA | HR, training owner | “Nhóm nào cần đào tạo, cần thực hiện được tác vụ nào và đánh giá kết quả ra sao?” | Xác định training outcome | Train-the-trainer? ca/địa điểm/ngôn ngữ? | Training matrix | `[ĐIỀN]` | Chưa có readiness người dùng | `[ĐIỀN]/[ĐIỀN]` |
| OPS-04 | Nên có | BA | HR, vận hành | “Cần tài liệu hướng dẫn nào, cho vai trò nào và ai duy trì sau bàn giao?” | Xác định documentation ownership | Video/quick guide/SOP? | Danh mục tài liệu | `[ĐIỀN]` | Thiếu hỗ trợ tự phục vụ | `[ĐIỀN]/[ĐIỀN]` |
| OPS-05 | Bắt buộc | PM/Dev | Sponsor, IT | “Kênh và giờ hỗ trợ mong muốn là gì? Nội dung này hiện là mong muốn hay đã có thỏa thuận?” | Ghi nhu cầu, không tạo SLA | Ai được mở ticket? escalation? | Thỏa thuận hiện có nếu được phép | `[ĐIỀN] [CHƯA CAM KẾT SLA]` | Không đánh giá support model | `[ĐIỀN]/[ĐIỀN]` |
| OPS-06 | Bắt buộc | PM/Dev | IT, vận hành | “Đơn vị phân loại mức độ ưu tiên sự cố như thế nào và ai quyết định?” | Xác định incident taxonomy | Ví dụ impact/urgency? | Process | `[ĐIỀN]` | Không triage thống nhất | `[ĐIỀN]/[ĐIỀN]` |
| OPS-07 | Nên có | PM/Dev | Sponsor, procurement/IT | “Kỳ vọng bảo hành, bảo trì và trách nhiệm hai bên là gì? Chúng tôi ghi nhận để kiểm tra thẩm quyền.” | Tránh tạo phạm vi hỗ trợ | Thiết bị/phần mềm? ngoài giờ? | Contract/source được phép | `[ĐIỀN] [CHƯA CAM KẾT]` | Dễ lệch kỳ vọng | `[ĐIỀN]/[ĐIỀN]` |
| OPS-08 | Bắt buộc | Hạ tầng | IT | “Ai thực hiện backup/restore, thay đổi cấu hình và bằng cách nào kiểm chứng kết quả?” | Xác định operational control | Test restore/change approval/rollback? | Runbook/test result | `[ĐIỀN]` | Không bảo đảm recoverability | `[ĐIỀN]/[ĐIỀN]` |
| OPS-09 | Bắt buộc | PM + BA | Sponsor, HR, IT | “Yêu cầu mới sau bàn giao được gửi, đánh giá, ưu tiên và phê duyệt thế nào?” | Xác định change intake | Ai chịu chi phí/phạm vi? | Change process | `[ĐIỀN] [CHƯA CAM KẾT]` | Scope creep | `[ĐIỀN]/[ĐIỀN]` |
| OPS-10 | Bắt buộc | PM/Dev | Nghiệm thu, HR, IT | “Tiêu chí sẵn sàng đưa hệ thống vào sử dụng là gì; trách nhiệm của khách hàng và trách nhiệm của đội dự án ở từng tiêu chí là gì?” | Xác định readiness/acceptance sơ bộ | Data/device/network/training/support? | Checklist/acceptance source | `[ĐIỀN] [CHƯA XÁC NHẬN]` | Chưa xác định gate bàn giao | `[ĐIỀN]/[ĐIỀN]` |

**Checklist J:** [ ] Owner quản trị/nhân viên/ca/công/lỗi/duyệt; [ ] nhóm đào tạo/tài liệu; [ ] kênh/giờ hỗ trợ và severity chỉ là nhu cầu nếu chưa thỏa thuận; [ ] bảo hành/bảo trì `[CHƯA CAM KẾT]`; [ ] backup/restore/change; [ ] intake yêu cầu mới; [ ] readiness và trách nhiệm hai bên có authority/evidence.

## K — Checklist theo từng nhóm nội dung

Các checklist chuyên biệt đã đặt ngay sau E1, E2, E3, E4, E5, E6, G, H, I và J. Với **mỗi nhóm**, người phụ trách phải hoàn thành thêm checklist chung sau:

| Nhóm | Đã hỏi câu bắt buộc | Đã xác định nguồn | Đã ghi trả lời | Đã phân loại fact/requirement/assumption | Đã thu/yêu cầu evidence | Đã ghi phần thiếu | Đã có owner | Đã có hạn | Đã đọc lại xác nhận | Không cam kết vượt quyền | Kết luận |
|---|---|---|---|---|---|---|---|---|---|---|---|
| E1 — Kinh doanh | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | `[ĐIỀN]` |
| E2 — Stakeholder | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | `[ĐIỀN]` |
| E3 — Quy mô | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | `[ĐIỀN]` |
| E4 — Quy trình | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | `[ĐIỀN]` |
| E5 — Quy tắc | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | `[ĐIỀN]` |
| E6/F — Chức năng/Fit–Gap | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | `[ĐIỀN]` |
| G — Thiết bị | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | `[ĐIỀN]` |
| H — Hạ tầng/Network | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | `[ĐIỀN]` |
| I — Dữ liệu/Bảo mật | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | `[ĐIỀN]` |
| J — Vận hành/Bàn giao | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | `[ĐIỀN]` |

## L — Checklist kiểm tra riêng cho BA

| ID | Tiêu chí kiểm tra | Trạng thái | Evidence/ID liên quan | Thiếu thông tin gì | Ai bổ sung | Hạn bổ sung | Ghi chú của PM |
|---|---|---|---|---|---|---|---|
| BA-01 | Đã xác định mục tiêu kinh doanh | Chưa thực hiện | BUS-01, BUS-03, BUS-04 | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` |
| BA-02 | Đã xác định pain point và tác động | Chưa thực hiện | BUS-02 | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` |
| BA-03 | Đã mô tả quy trình end-to-end | Chưa thực hiện | PRC-01–10 | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` |
| BA-04 | Đã xác định actor của từng bước | Chưa thực hiện | PRC-01–10, STK-03–05 | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` |
| BA-05 | Đã ghi input/output của từng bước | Chưa thực hiện | PRC-01–10 | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` |
| BA-06 | Đã khảo sát quy tắc nghiệp vụ | Chưa thực hiện | RUL-01–10 | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` |
| BA-07 | Đã khảo sát ngoại lệ | Chưa thực hiện | RUL-02–09 | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` |
| BA-08 | Đã xác định người phê duyệt | Chưa thực hiện | STK-02, STK-07, PRC-07 | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` |
| BA-09 | Đã xác định báo cáo cần thiết | Chưa thực hiện | FUN-02 | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` |
| BA-10 | Đã xác định dữ liệu import/export | Chưa thực hiện | FUN-04, DAT-04 | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` |
| BA-11 | Đã xác định nhu cầu tích hợp | Chưa thực hiện | FUN-07, DAT-05–06 | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` |
| BA-12 | Đã phân biệt must-have/nice-to-have | Chưa thực hiện | FUN-01, F | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` |
| BA-13 | Đã ghi nguồn của từng yêu cầu | Chưa thực hiện | F, STK-03 | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` |
| BA-14 | Đã phát hiện và ghi yêu cầu mâu thuẫn | Chưa thực hiện | STK-08, Conflict Log | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` |
| BA-15 | Đã ghi assumption | Chưa thực hiện | Assumption Log | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` |
| BA-16 | Đã ghi open question | Chưa thực hiện | Open Question Log | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` |
| BA-17 | Đã xác định acceptance criteria sơ bộ | Chưa thực hiện | BUS-04, OPS-10, F | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` |
| BA-18 | Đã đọc lại kết quả để khách hàng xác nhận cách hiểu | Chưa thực hiện | R | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` |
| BA-19 | Chưa biến mong muốn thành yêu cầu được duyệt | Chưa kiểm tra | F/O | `[ĐIỀN]` | PM | `[ĐIỀN]` | `[ĐIỀN]` |
| BA-20 | Chưa hứa custom hoặc thời hạn | Chưa kiểm tra | F/R | `[ĐIỀN]` | PM | `[ĐIỀN]` | `[ĐIỀN]` |

**Quy tắc PM đánh giá BA:** Không đánh dấu `Hoàn thành` chỉ vì BA đã hỏi. Phải có câu trả lời đủ rõ, nguồn, phân loại, evidence phù hợp hoặc open item có owner/hạn.

## M — Checklist kiểm tra riêng cho Hạ tầng/Network

| ID | Tiêu chí kiểm tra | Trạng thái | Evidence/ID liên quan | Thiếu thông tin gì | Ai bổ sung | Hạn bổ sung | Ghi chú của PM |
|---|---|---|---|---|---|---|---|
| NW-01 | Đã xác định mô hình triển khai | Chưa thực hiện | NET-01 | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` |
| NW-02 | Đã kiểm tra vị trí thiết bị | Chưa thực hiện | DEV-06, G1 | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` |
| NW-03 | Đã kiểm tra nguồn điện/UPS | Chưa thực hiện | DEV-07 | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` |
| NW-04 | Đã xác định loại kết nối | Chưa thực hiện | DEV-08, NET-03 | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` |
| NW-05 | Đã xác định IP/DHCP/VLAN liên quan | Chưa thực hiện | NET-04 | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` | Không ghi IP nhạy cảm |
| NW-06 | Đã xác định firewall/port cần đánh giá | Chưa thực hiện | NET-06 | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` | Không tự mở port |
| NW-07 | Đã xác định khả năng truy cập Internet | Chưa thực hiện | NET-07 | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` |
| NW-08 | Đã xác định kết nối giữa các cơ sở | Chưa thực hiện | NET-09 | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` |
| NW-09 | Đã xác định máy chủ/máy trạm | Chưa thực hiện | NET-02 | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` |
| NW-10 | Đã xác định quyền cài đặt/quản trị | Chưa thực hiện | NET-11, NET-16 | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` |
| NW-11 | Đã xác định chính sách remote support | Chưa thực hiện | NET-08 | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` | `[CHƯA CAM KẾT]` |
| NW-12 | Đã xác định yêu cầu bảo mật | Chưa thực hiện | NET-06, NET-10, DAT-08–10 | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` |
| NW-13 | Đã xác định backup/restore | Chưa thực hiện | NET-13, OPS-08 | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` |
| NW-14 | Đã xác định đầu mối IT/network/security | Chưa thực hiện | C2, P | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` |
| NW-15 | Đã thu sơ đồ/mô tả mạng nếu được phép | Chưa thực hiện | NET-05, NET-09–10 | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` | Chỉ tham chiếu đã làm sạch |
| NW-16 | Đã ghi giới hạn kỹ thuật | Chưa thực hiện | H/O | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` |
| NW-17 | Đã ghi kiểm tra cần thực hiện sau | Chưa thực hiện | H/Open Question Log | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` |
| NW-18 | Không thu mật khẩu/private key/secret | Chưa kiểm tra | G2/H/I | `[ĐIỀN]` | PM | `[ĐIỀN]` | Bắt buộc |
| NW-19 | Không tự ý kết nối/thay đổi cấu hình | Chưa kiểm tra | G2, NET-16 | `[ĐIỀN]` | PM | `[ĐIỀN]` | Bắt buộc |
| NW-20 | Không kết luận khả năng triển khai khi thiếu evidence | Chưa kiểm tra | H/S | `[ĐIỀN]` | PM | `[ĐIỀN]` | Bắt buộc |

**Quy tắc PM đánh giá Network:** Quan sát không có phép hoặc lời nói không có nguồn không đủ để đánh dấu hoàn thành; nội dung ảnh hưởng kiến trúc, bảo mật hoặc kết nối thiếu evidence phải là `Blocked/Cần xác minh`.

## N — Checklist kiểm soát của PM/Dev

| ID | Nội dung kiểm soát | Trạng thái | Evidence/ID | Vấn đề hoặc hành động |
|---|---|---|---|---|
| PM-01 | Mục tiêu buổi làm việc và phạm vi đã được thông báo | Chưa thực hiện | B | `[ĐIỀN]` |
| PM-02 | Stakeholder và authority đã được phân biệt | Chưa thực hiện | C, E2, P | `[ĐIỀN]` |
| PM-03 | Chức năng phần mềm hiện có được đối chiếu bằng evidence | Chưa thực hiện | E6, F | `[ĐIỀN]` |
| PM-04 | Fit–Gap có nguồn và không kết luận vượt evidence | Chưa thực hiện | F | `[ĐIỀN]` |
| PM-05 | Nội dung cần demo có use case/dữ liệu test an toàn | Chưa thực hiện | FUN-09 | `[ĐIỀN]` |
| PM-06 | Custom request đều gắn `[CHƯA CAM KẾT CUSTOM]` | Chưa kiểm tra | BUS-07, F | `[ĐIỀN]` |
| PM-07 | Phụ thuộc và rủi ro đã ghi owner/hạn | Chưa thực hiện | O | `[ĐIỀN]` |
| PM-08 | Vấn đề cần quyết định có đúng authority | Chưa thực hiện | Decision Log | `[ĐIỀN]` |
| PM-09 | Yêu cầu chưa rõ có câu hỏi tiếp nối | Chưa thực hiện | F/Open Question Log | `[ĐIỀN]` |
| PM-10 | Cam kết phát sinh trong lời nói/tài liệu đã được ghi | Chưa thực hiện | R/O | `[ĐIỀN]` |
| PM-11 | Nếu thành viên lỡ cam kết: đã đính chính ngay, ghi biên bản và escalate | `[KHÔNG ÁP DỤNG – NÊU LÝ DO]` | R/Issue Log | Câu đính chính: “Xin phép làm rõ: nội dung vừa nêu là nhận định sơ bộ, chưa phải cam kết. Đội dự án sẽ đánh giá và phản hồi qua đầu mối có thẩm quyền.” |
| PM-12 | Người xác nhận biên bản đã rõ | Chưa thực hiện | STK-07, R | `[ĐIỀN]` |
| PM-13 | Kế hoạch phản hồi khách hàng có owner và ngày dự kiến được phép | Chưa thực hiện | A, R | `[ĐIỀN]` |
| PM-14 | Điều kiện chuyển sang thiết kế Delivery đã được kiểm tra | Chưa thực hiện | Q, S | Chỉ chuyển khi không còn blocker về scope/security/integration/architecture và có thẩm quyền |
| PM-15 | Không phát sinh cam kết chi phí/tiến độ/kiến trúc/SLA | Chưa kiểm tra | Toàn tài liệu | `[ĐIỀN]` |

## O — Issue, Risk, Assumption, Dependency và Decision Log

### O1. Issue Log

| ID | Mô tả | Loại/nguồn | Thời điểm | Ảnh hưởng/mức độ | Evidence | Người xử lý | Người quyết định | Hành động tiếp theo | Hạn | Trạng thái | Kết quả/ngày xác nhận |
|---|---|---|---|---|---|---|---|---|---|---|---|
| ISS-001 | `[ĐIỀN]` | ISSUE / `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` / `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` | Open | `[CHƯA XÁC NHẬN]` |

### O2. Risk Log

| ID | Mô tả/nguyên nhân/sự kiện/tác động | Nguồn/thời điểm | Xác suất | Tác động | Mức độ | Evidence | Owner | Ứng phó/hành động | Hạn | Trạng thái | Kết quả/ngày xác nhận |
|---|---|---|---|---|---|---|---|---|---|---|---|
| RSK-001 | `[ĐIỀN]` | `[ĐIỀN]` | `[CHƯA XÁC NHẬN]` | `[CHƯA XÁC NHẬN]` | `[CHƯA XÁC NHẬN]` | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` | Open | `[CHƯA XÁC NHẬN]` |

### O3. Assumption Log

| ID | Giả định | Nguồn/thời điểm | Vì sao cần giả định | Ảnh hưởng nếu sai | Evidence cần | Người xác minh | Hành động/hạn | Trạng thái | Kết quả/ngày xác nhận |
|---|---|---|---|---|---|---|---|---|---|
| ASM-001 | `[ĐIỀN — không viết như fact]` | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` | Chưa xác minh | `[CHƯA XÁC NHẬN]` |

### O4. Dependency Log

| ID | Phụ thuộc | Loại/nguồn | Bên cung cấp | Điều kiện/kết quả cần | Ảnh hưởng | Evidence | Owner theo dõi | Hành động/hạn | Trạng thái | Kết quả/ngày xác nhận |
|---|---|---|---|---|---|---|---|---|---|---|
| DEP-001 | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` | Open | `[CHƯA XÁC NHẬN]` |

### O5. Decision Log

| ID | Quyết định cần/đã đưa ra | Nguồn/thời điểm | Các lựa chọn | Evidence | Người có quyền quyết định | Hành động/hạn | Trạng thái | Kết quả | Ngày xác nhận |
|---|---|---|---|---|---|---|---|---|---|
| DEC-001 | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` | `[CHƯA XÁC NHẬN]` | `[ĐIỀN]` | Decision required | `[CHƯA XÁC NHẬN]` | `[CHƯA XÁC NHẬN]` |

### O6. Open Question Log

| ID | Câu hỏi còn mở | Nguồn/thời điểm | Liên kết ID | Ảnh hưởng/mức độ | Evidence cần | Người trả lời | Người theo dõi | Hành động/hạn | Trạng thái | Kết quả/ngày xác nhận |
|---|---|---|---|---|---|---|---|---|---|---|
| OQ-001 | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` | Open | `[CHƯA XÁC NHẬN]` |

### O7. Conflict Log

| ID | Nội dung không thống nhất | Bên/nguồn A | Bên/nguồn B | Thời điểm | Ảnh hưởng/mức độ | Evidence cần | Người điều phối | Người quyết định | Hành động/hạn | Trạng thái | Kết quả/ngày xác nhận |
|---|---|---|---|---|---|---|---|---|---|---|---|
| CFL-001 | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` | PM | `[CHƯA XÁC NHẬN]` | `[ĐIỀN]` | Cần xác minh | `[CHƯA XÁC NHẬN]` |

## P — Checklist đầu mối

> Trong Git công khai, không điền tên, điện thoại hoặc email thật. Dùng mã đầu mối và tham chiếu đến danh bạ được phê duyệt.

| Lĩnh vực | Đầu mối chính | Dự phòng | Đơn vị/chức vụ | Điện thoại | Email | Kênh ưu tiên | Thông tin có quyền xác nhận | Quyết định | Phê duyệt | Nghiệm thu | Tài liệu phải cung cấp | Hạn | Trạng thái/ghi chú |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| Nghiệp vụ chấm công | `[MÃ]` | `[MÃ]` | `[ĐIỀN]` | `[THAM CHIẾU]` | `[THAM CHIẾU]` | `[ĐIỀN]` | Quy trình/rule `[CHƯA XÁC NHẬN]` | `[CHƯA XÁC NHẬN]` | `[CHƯA XÁC NHẬN]` | `[CHƯA XÁC NHẬN]` | `[ĐIỀN]` | `[ĐIỀN]` | Chưa xác nhận |
| HR/C&B | `[MÃ]` | `[MÃ]` | `[ĐIỀN]` | `[THAM CHIẾU]` | `[THAM CHIẾU]` | `[ĐIỀN]` | HR/rule | `[CHƯA XÁC NHẬN]` | `[CHƯA XÁC NHẬN]` | `[CHƯA XÁC NHẬN]` | `[ĐIỀN]` | `[ĐIỀN]` | Chưa xác nhận |
| Tính lương | `[MÃ]` | `[MÃ]` | `[ĐIỀN]` | `[THAM CHIẾU]` | `[THAM CHIẾU]` | `[ĐIỀN]` | Payroll/output | `[CHƯA XÁC NHẬN]` | `[CHƯA XÁC NHẬN]` | `[CHƯA XÁC NHẬN]` | `[ĐIỀN]` | `[ĐIỀN]` | Chưa xác nhận |
| IT | `[MÃ]` | `[MÃ]` | `[ĐIỀN]` | `[THAM CHIẾU]` | `[THAM CHIẾU]` | `[ĐIỀN]` | Hệ thống/quyền | `[CHƯA XÁC NHẬN]` | `[CHƯA XÁC NHẬN]` | `[CHƯA XÁC NHẬN]` | `[ĐIỀN]` | `[ĐIỀN]` | Chưa xác nhận |
| Network | `[MÃ]` | `[MÃ]` | `[ĐIỀN]` | `[THAM CHIẾU]` | `[THAM CHIẾU]` | `[ĐIỀN]` | Kết nối/network | `[CHƯA XÁC NHẬN]` | `[CHƯA XÁC NHẬN]` | `[CHƯA XÁC NHẬN]` | `[ĐIỀN]` | `[ĐIỀN]` | Chưa xác nhận |
| Thiết bị | `[MÃ]` | `[MÃ]` | `[ĐIỀN]` | `[THAM CHIẾU]` | `[THAM CHIẾU]` | `[ĐIỀN]` | Inventory/vận hành | `[CHƯA XÁC NHẬN]` | `[CHƯA XÁC NHẬN]` | `[CHƯA XÁC NHẬN]` | `[ĐIỀN]` | `[ĐIỀN]` | Chưa xác nhận |
| Bảo mật | `[MÃ]` | `[MÃ]` | `[ĐIỀN]` | `[THAM CHIẾU]` | `[THAM CHIẾU]` | `[ĐIỀN]` | Policy/approval | `[CHƯA XÁC NHẬN]` | `[CHƯA XÁC NHẬN]` | `[CHƯA XÁC NHẬN]` | `[ĐIỀN]` | `[ĐIỀN]` | Chưa xác nhận |
| Dữ liệu | `[MÃ]` | `[MÃ]` | `[ĐIỀN]` | `[THAM CHIẾU]` | `[THAM CHIẾU]` | `[ĐIỀN]` | Master/quality/access | `[CHƯA XÁC NHẬN]` | `[CHƯA XÁC NHẬN]` | `[CHƯA XÁC NHẬN]` | `[ĐIỀN]` | `[ĐIỀN]` | Chưa xác nhận |
| Quản trị hệ thống | `[MÃ]` | `[MÃ]` | `[ĐIỀN]` | `[THAM CHIẾU]` | `[THAM CHIẾU]` | `[ĐIỀN]` | Vận hành/config | `[CHƯA XÁC NHẬN]` | `[CHƯA XÁC NHẬN]` | `[CHƯA XÁC NHẬN]` | `[ĐIỀN]` | `[ĐIỀN]` | Chưa xác nhận |
| Đào tạo | `[MÃ]` | `[MÃ]` | `[ĐIỀN]` | `[THAM CHIẾU]` | `[THAM CHIẾU]` | `[ĐIỀN]` | Nhóm/tài liệu | `[CHƯA XÁC NHẬN]` | `[CHƯA XÁC NHẬN]` | `[CHƯA XÁC NHẬN]` | `[ĐIỀN]` | `[ĐIỀN]` | Chưa xác nhận |
| Hỗ trợ vận hành | `[MÃ]` | `[MÃ]` | `[ĐIỀN]` | `[THAM CHIẾU]` | `[THAM CHIẾU]` | `[ĐIỀN]` | Incident/support | `[CHƯA XÁC NHẬN]` | `[CHƯA XÁC NHẬN]` | `[CHƯA XÁC NHẬN]` | `[ĐIỀN]` | `[ĐIỀN]` | Chưa xác nhận |
| Quyết định phạm vi | `[MÃ]` | `[MÃ]` | `[ĐIỀN]` | `[THAM CHIẾU]` | `[THAM CHIẾU]` | `[ĐIỀN]` | Scope/priority | `[CHƯA XÁC NHẬN]` | `[CHƯA XÁC NHẬN]` | `[CHƯA XÁC NHẬN]` | `[ĐIỀN]` | `[ĐIỀN]` | Chưa xác nhận |
| Nghiệm thu | `[MÃ]` | `[MÃ]` | `[ĐIỀN]` | `[THAM CHIẾU]` | `[THAM CHIẾU]` | `[ĐIỀN]` | Acceptance | `[CHƯA XÁC NHẬN]` | `[CHƯA XÁC NHẬN]` | `[CHƯA XÁC NHẬN]` | `[ĐIỀN]` | `[ĐIỀN]` | Chưa xác nhận |

## Q — Checklist kết quả bắt buộc sau khảo sát

| ID | Mức yêu cầu | Kết quả cần có | Trạng thái | Evidence | Người xác nhận | Thông tin còn thiếu | Chặn bước tiếp theo? |
|---|---|---|---|---|---|---|---|
| OUT-01 | Bắt buộc để kết thúc buổi | Mục tiêu khách hàng | Chưa hoàn thành | BUS-01/03/04 | `[CHƯA XÁC NHẬN]` | `[ĐIỀN]` | Có nếu không rõ mandate |
| OUT-02 | Bắt buộc để kết thúc buổi | Vấn đề hiện tại | Chưa hoàn thành | BUS-02 | `[CHƯA XÁC NHẬN]` | `[ĐIỀN]` | Có nếu không rõ pain point |
| OUT-03 | Bắt buộc trước Delivery Plan | Quy trình end-to-end | Chưa hoàn thành | PRC-01–10 | `[CHƯA XÁC NHẬN]` | `[ĐIỀN]` | Có |
| OUT-04 | Bắt buộc trước Delivery Plan | Ngoại lệ quan trọng | Chưa hoàn thành | RUL-01–10 | `[CHƯA XÁC NHẬN]` | `[ĐIỀN]` | Có |
| OUT-05 | Bắt buộc để kết thúc buổi | Quy mô sử dụng sơ bộ | Chưa hoàn thành | SIZ-01–07 | `[CHƯA XÁC NHẬN]` | `[ĐIỀN]` | Có nếu ảnh hưởng tải/phạm vi |
| OUT-06 | Bắt buộc để kết thúc buổi | Stakeholder và authority | Chưa hoàn thành | STK-01–08, P | `[CHƯA XÁC NHẬN]` | `[ĐIỀN]` | Có |
| OUT-07 | Bắt buộc để kết thúc buổi | Danh sách yêu cầu ban đầu có nguồn | Chưa hoàn thành | F | `[CHƯA XÁC NHẬN]` | `[ĐIỀN]` | Có |
| OUT-08 | Có thể bổ sung sau | Fit–Gap sơ bộ | Chưa hoàn thành | E6/F | `[CHƯA XÁC NHẬN]` | `[ĐIỀN]` | Có trước Delivery Plan |
| OUT-09 | Có thể bổ sung sau | Danh sách nội dung cần đánh giá custom | Chưa hoàn thành | F | `[CHƯA XÁC NHẬN]` | `[ĐIỀN]` | Không mặc định; tùy ưu tiên |
| OUT-10 | Bắt buộc trước Delivery Plan | Thông tin thiết bị | Chưa hoàn thành | G | `[CHƯA XÁC NHẬN]` | `[ĐIỀN]` | Có nếu dùng thiết bị |
| OUT-11 | Bắt buộc trước Delivery Plan | Thông tin hạ tầng/network | Chưa hoàn thành | H | `[CHƯA XÁC NHẬN]` | `[ĐIỀN]` | Có |
| OUT-12 | Bắt buộc trước Delivery Plan | Yêu cầu dữ liệu/tích hợp | Chưa hoàn thành | I | `[CHƯA XÁC NHẬN]` | `[ĐIỀN]` | Có |
| OUT-13 | Bắt buộc trước Delivery Plan | Ràng buộc bảo mật/privacy | Chưa hoàn thành | H/I | `[CHƯA XÁC NHẬN]` | `[ĐIỀN]` | Có |
| OUT-14 | Bắt buộc để kết thúc buổi | Đầu mối theo nhóm | Chưa hoàn thành | P | `[CHƯA XÁC NHẬN]` | `[ĐIỀN]` | Có nếu không thể follow-up |
| OUT-15 | Bắt buộc để kết thúc buổi | Danh sách evidence cần bổ sung | Chưa hoàn thành | E–J/O | `[CHƯA XÁC NHẬN]` | `[ĐIỀN]` | Tùy evidence |
| OUT-16 | Bắt buộc để kết thúc buổi | Issue/Risk/Assumption/Open Question/Conflict | Chưa hoàn thành | O | PM | `[ĐIỀN]` | Tùy mức độ |
| OUT-17 | Bắt buộc để kết thúc buổi | Người xác nhận biên bản | Chưa hoàn thành | STK-07/R | `[CHƯA XÁC NHẬN]` | `[ĐIỀN]` | Có |
| OUT-18 | Bắt buộc để kết thúc buổi | Bước tiếp theo và owner | Chưa hoàn thành | R | PM | `[ĐIỀN]` | Có |
| OUT-19 | Có thể bổ sung sau | Thời điểm phản hồi dự kiến | Chưa hoàn thành | A/R | PM | `[ĐIỀN]` | Không, nếu chưa được phép cam kết |
| OUT-20 | Bắt buộc để kết thúc buổi | Không có cam kết chưa phê duyệt; nếu có đã đính chính | Chưa kiểm tra | N/R | PM | `[ĐIỀN]` | Có |

## R — Biên bản tổng kết cuối buổi

| Nội dung đọc lại | Ghi nhận |
|---|---|
| Những gì đội dự án đã hiểu | `[ĐIỀN; dẫn ID và phân loại]` |
| Mục tiêu được xác nhận | `[ĐIỀN BUS-xx]` `[CHƯA XÁC NHẬN nếu thiếu authority/evidence]` |
| Vấn đề chính | `[ĐIỀN BUS-02/ISS-xx]` |
| Yêu cầu chính | `[ĐIỀN REQ-xxx; phân biệt must-have/nice-to-have và nguồn]` |
| Nội dung chưa xác nhận | `[ĐIỀN OQ/ASM/CFL ID]` |
| Yêu cầu custom cần đánh giá | `[ĐIỀN REQ-xxx]` `[CHƯA CAM KẾT CUSTOM]` |
| Tài liệu/evidence khách hàng cần bổ sung | `[ĐIỀN mã tài liệu, không chép nội dung nhạy cảm]` |
| Đầu mối | `[ĐIỀN mã đầu mối P]` |
| Hành động tiếp theo | `[ĐIỀN]` |
| Người chịu trách nhiệm | `[ĐIỀN]` |
| Thời hạn | `[ĐIỀN]` `[CHƯA XÁC NHẬN nếu chưa có thẩm quyền]` |
| Nội dung đội dự án chưa cam kết | Custom, tích hợp, kiến trúc, chi phí, tiến độ, SLA, phạm vi hỗ trợ, bảo hành/bảo trì, go-live và nghiệm thu. |
| Người xác nhận biên bản | `[ĐIỀN MÃ/VAI TRÒ]` `[CHƯA XÁC NHẬN THẨM QUYỀN]` |
| Cách thức/ngày xác nhận | `[ĐIỀN]` |

**Lời kết đề xuất cho PM**

> Cảm ơn anh/chị. Đội dự án xin đọc lại các nội dung chính để bảo đảm không hiểu sai. Những điểm đã rõ sẽ được ghi cùng nguồn xác nhận; các điểm còn thiếu hoặc mâu thuẫn sẽ có đầu mối và hạn bổ sung. Các đề nghị về custom, tích hợp, giải pháp kỹ thuật, chi phí hoặc thời gian hiện chỉ là nội dung cần đánh giá, chưa phải cam kết. Sau khi kiểm tra evidence và chức năng hiện có, PM sẽ phản hồi qua đầu mối và thời điểm đã được thống nhất.

## S — Đánh giá mức độ hoàn thành Discovery

### S1. Quy tắc trạng thái

| Trạng thái | Điều kiện |
|---|---|
| Complete | Câu trả lời đủ rõ, có nguồn phù hợp, evidence cần thiết và không còn open item ảnh hưởng kết luận. |
| Partially Complete | Đã có một phần thông tin nhưng còn thiếu owner/evidence/chi tiết; ảnh hưởng đã được ghi. |
| Not Started | Chưa hỏi hoặc chưa có ghi nhận. |
| Blocked | Thiếu/mâu thuẫn thông tin ảnh hưởng phạm vi, bảo mật, tích hợp, kiến trúc, chi phí hoặc tiến độ; hoặc thiếu thẩm quyền/evidence bắt buộc. |
| Not Applicable | Có lý do rõ, người phù hợp xác nhận và ghi `[KHÔNG ÁP DỤNG – NÊU LÝ DO]`. |
| Cần xác minh | Các nguồn mâu thuẫn hoặc câu trả lời chưa có authority/evidence đủ. Không được coi là Complete. |

Không đánh dấu hoàn thành chỉ vì đã hỏi. Thiếu thông tin ảnh hưởng phạm vi, bảo mật, tích hợp, kiến trúc, chi phí hoặc tiến độ phải là `Blocked`. Không dùng tỷ lệ phần trăm thay cho đánh giá nội dung.

### S2. Bảng đánh giá

| Nhóm | Trạng thái | Nội dung còn thiếu | Ảnh hưởng | Ai bổ sung | Hạn | Được chuyển bước? | Điều kiện |
|---|---|---|---|---|---|---|---|
| E1 — Bối cảnh/mục tiêu | Not Started | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` | Không | BUS bắt buộc có nguồn |
| E2 — Stakeholder/authority | Not Started | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` | Không | Người quyết định/nghiệm thu rõ |
| E3 — Quy mô | Not Started | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` | Số liệu đủ đánh giá tải |
| E4 — Quy trình | Not Started | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` | Không | PRC-01–10 đủ |
| E5 — Quy tắc/ngoại lệ | Not Started | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` | Không | Rule có nguồn/effective date |
| E6/F — Chức năng/Fit–Gap | Not Started | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` | Không | Không còn kết luận thiếu evidence |
| G — Thiết bị | Not Started | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` | Inventory/điều kiện lắp rõ |
| H — Hạ tầng/Network | Not Started | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` | Không | Không còn blocker kỹ thuật |
| I — Dữ liệu/Bảo mật | Not Started | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` | Không | Data owner, handling, approval rõ |
| J — Vận hành/Bàn giao | Not Started | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` | Ownership/readiness rõ |
| O — Logs/Decision | Not Started | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` | `[ĐIỀN]` | Mỗi item có owner/hạn |
| Q — Kết quả bắt buộc | Not Started | `[ĐIỀN]` | `[ĐIỀN]` | PM | `[ĐIỀN]` | Không | OUT-01–20 được đánh giá |

## Quality Review

| Câu kiểm tra | Kết quả tự kiểm tra trước khi phát hành | Evidence/hành động nếu chưa đạt |
|---|---|---|
| Có nhóm thông tin nào bị thiếu không? | `[CHƯA XÁC NHẬN — rà A–S và E1–J]` | `[ĐIỀN]` |
| Có câu hỏi quan trọng nào không nêu rõ lý do/giải thích không? | `[CHƯA XÁC NHẬN — rà cột mục đích/giải thích]` | `[ĐIỀN]` |
| Có nội dung nào chưa xác định người phụ trách hỏi không? | `[CHƯA XÁC NHẬN — rà owner PM/BA/Hạ tầng/Phối hợp]` | `[ĐIỀN]` |
| Có yêu cầu nào bị hiểu nhầm thành cam kết không? | `[CHƯA XÁC NHẬN — rà F, J, N, R]` | Mọi custom/tích hợp/kiến trúc/chi phí/tiến độ/SLA phải là chưa cam kết |
| BA có thể chứng minh đã hỏi đủ không? | `[CHƯA XÁC NHẬN — hoàn thành L bằng evidence]` | `[ĐIỀN]` |
| Network có thể chứng minh đã khảo sát đủ không? | `[CHƯA XÁC NHẬN — hoàn thành M bằng evidence]` | `[ĐIỀN]` |
| PM xác định được thông tin nào chặn bước tiếp theo không? | `[CHƯA XÁC NHẬN — rà Q/S]` | `[ĐIỀN]` |
| Tất cả vấn đề có đầu mối và hành động tiếp theo chưa? | `[CHƯA XÁC NHẬN — rà O/P/R]` | `[ĐIỀN]` |
| Mọi dữ liệu chưa được xác nhận có gắn `[CHƯA XÁC NHẬN]` hoặc trạng thái tương đương không? | `[CHƯA XÁC NHẬN]` | `[ĐIỀN]` |
| Tài liệu có chứa dữ liệu định danh/nhạy cảm hoặc credential không? | Không được phép | Xóa khỏi Git; chỉ để mã/tham chiếu access-controlled |
| Mọi relative Markdown link có tồn tại không? | `[CHƯA XÁC NHẬN — chạy link validation]` | `[ĐIỀN]` |
| Người rà soát đã xác nhận tài liệu vẫn là Draft và không tạo cam kết? | `[CHƯA XÁC NHẬN]` | `[ĐIỀN NGƯỜI/NGÀY]` |

**Kết luận Quality Review:** `[CHƯA XÁC NHẬN — chỉ đổi khi tất cả mục bắt buộc đã có evidence và người rà soát có thẩm quyền xác nhận]`.
