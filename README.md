# Phân tích nghiệp vụ theo BACCM: Cải tiến quản lý nhân sự và giám sát vận hành quầy thuê PongChee tại Emart

Case study Business Analysis ứng dụng **BACCM (Business Analysis Core Concept Model)** của BABOK v3 để tiếp cận có cấu trúc một yêu cầu cải tiến còn mơ hồ: hệ thống quản trị nhân sự cũ, nhiều nghiệp vụ còn làm thủ công.


---

## 1. Bối cảnh

PongChee là đối tác của ThisoMall, cung cấp và vận hành các quầy thuê trong hệ thống siêu thị Emart. Nhân viên PongChee làm việc tại quầy, chịu sự quản lý của leader PongChee và phải tuân thủ quy định vận hành của Emart.

Hiện trạng:

- Hồ sơ nhân viên lưu giấy tại văn phòng nhân sự Emart, PongChee giữ bản sao sơ yếu lý lịch và hợp đồng lao động.
- Dữ liệu chấm công nằm trên ứng dụng riêng của nhà phân phối; tổng hợp và tính lương bằng Excel.
- Lịch ca do leader quản lý bằng Excel và gửi ảnh chụp màn hình cho nhân viên.
- Quản lý ngành hàng Emart không thể túc trực liên tục tại quầy, khi có sự cố phải liên hệ leader qua Zalo để xác minh và gửi bằng chứng.

Vấn đề không chỉ nằm ở công nghệ mà còn ở cách tổ chức quy trình, khả năng tiếp cận thông tin, trách nhiệm xử lý và cơ chế phối hợp giữa PongChee và Emart.

## 2. Mục tiêu phân tích

- Làm rõ bối cảnh nghiệp vụ và các vấn đề hiện tại.
- Xác định các bên liên quan, vai trò, quyền hạn và nhu cầu.
- Phân tích nguyên nhân gốc rễ bằng phương pháp **5 Whys**.
- Xác định nhu cầu nghiệp vụ thực sự cần giải quyết.
- Làm rõ thay đổi cần thiết về quy trình, dữ liệu và trách nhiệm.
- Đề xuất giải pháp phù hợp với nguồn lực và đặc thù vận hành.
- Xác định giá trị kỳ vọng và các KPI đo lường sau triển khai.

## 3. Cách áp dụng BACCM

| Thành phần | Nội dung chính trong case study |
|---|---|
| **Context** | 5 quy trình hiện tại (hồ sơ, phân ca, chấm công và giám sát, xử lý vi phạm và sự cố, tính lương); con người, cấu trúc tổ chức, dữ liệu, chính sách và tiêu chuẩn, 12 quy tắc nghiệp vụ (BR-01 đến BR-12) |
| **Stakeholders** | Ban giám đốc, leader, nhân sự, quản lý khu vực, nhân viên PongChee; quản lý ngành hàng, quản lý siêu thị, nhân sự và kế toán Emart; bộ phận IT hoặc nhà cung cấp giải pháp |
| **Needs** | 11 nhu cầu (N-01 đến N-11) có liên kết với nguyên nhân gốc rễ, phân biệt rõ nhu cầu nghiệp vụ với giải pháp công nghệ |
| **Changes** | 10 thay đổi AS-IS sang TO-BE (C-01 đến C-10), phạm vi ưu tiên giai đoạn đầu |
| **Solutions** | Hệ thống quản lý lịch ca và xử lý sự cố, kết hợp số hóa hồ sơ nhân sự thiết yếu và phân quyền dữ liệu |
| **Value** | Giá trị theo từng stakeholder và bộ KPI đánh giá hiệu quả |

## 4. Phân tích nguyên nhân gốc rễ (5 Whys)

**Vấn đề 1: Quản lý lịch ca và xác minh sự cố còn phụ thuộc thao tác thủ công.**
Nguyên nhân gốc rễ: quy trình phối hợp giữa PongChee và Emart chưa được chuẩn hóa; chưa quy định thời hạn phản hồi và đầu mối thay thế khi leader vắng mặt.

**Vấn đề 2: Dữ liệu nhân sự chưa được khai thác hiệu quả cho quản trị.**
Nguyên nhân gốc rễ: dữ liệu được quản lý chủ yếu để phục vụ nghiệp vụ và lưu trữ, chưa có cơ chế chuẩn hóa và khai thác cho phân tích, báo cáo. Đây là cơ hội cải tiến, không phải bằng chứng hệ thống hiện tại làm mất hoặc sai hồ sơ.

## 5. Giải pháp được lựa chọn

**Hệ thống quản lý lịch ca và xử lý sự cố**, gồm 5 phân hệ:

1. Quản lý lịch ca
2. Ghi nhận và xử lý sự cố
3. Thông báo và chuyển giao xử lý
4. Quản lý hồ sơ nhân sự thiết yếu (sơ yếu lý lịch, hợp đồng lao động, bậc lương)
5. Báo cáo

Nguyên tắc thiết kế:

- Ưu tiên cải thiện quy trình và cơ chế phối hợp trước, không bắt đầu bằng công nghệ giám sát phức tạp (camera AI).
- Phân quyền theo vai trò; quản lý ngành hàng Emart không truy cập dữ liệu lương và hồ sơ cá nhân.
- Hệ thống chỉ ghi nhận và quản lý quy trình, không tự động kết luận vi phạm hay quyết định nhân sự vượt thẩm quyền.
- Tự động hóa tính lương, tích hợp sâu ứng dụng chấm công và camera AI xem xét ở giai đoạn sau.

**Quy trình TO-BE (8 bước):** Phân ca, Chia sẻ lịch, Ghi nhận sự cố, Thông báo, Chuyển giao, Xác minh, Xử lý, Đóng sự cố.

**Kế hoạch triển khai:** Khảo sát và chuẩn hóa, Thử nghiệm hệ thống, Đánh giá và mở rộng.

## 6. KPI đề xuất

| Mục tiêu | KPI |
|---|---|
| Rút ngắn thời gian xác minh | Thời gian trung bình từ ghi nhận sự cố đến phản hồi đầu tiên |
| Nâng cao hiệu quả xử lý | Thời gian trung bình hoàn tất một sự cố |
| Giảm sự cố bị bỏ sót | Tỷ lệ sự cố được ghi nhận và có kết quả xử lý |
| Tăng khả năng kiểm soát | Tỷ lệ sự cố đủ thông tin và bằng chứng |
| Cải thiện quản lý lịch ca | Tỷ lệ lịch ca cập nhật và chia sẻ đúng hạn |
| Cải thiện quản lý hồ sơ | Tỷ lệ hồ sơ ưu tiên được số hóa và đầy đủ |
| Tăng khả năng truy vết | Tỷ lệ điều chỉnh hoặc xử lý có người thực hiện và lịch sử ghi nhận |
| Bảo vệ dữ liệu | Số trường hợp truy cập sai quyền hoặc chia sẻ dữ liệu không phù hợp |


## 7. Cấu trúc repository

```
.
├── README.md
├── docs/
│   └── BACCM_PongChee_Emart_Full_Case_Study.pdf   # Báo cáo đầy đủ
└── diagrams/                                       # (tùy chọn) Sơ đồ BPMN AS-IS / TO-BE
```



## 8. Mục lục báo cáo

1. Tổng quan bài toán
2. Context
3. Root Cause Analysis
4. Stakeholders
5. Needs
6. Changes
7. Solutions
8. Value
9. Tổng hợp BACCM
10. Kết luận

## 9. Hướng phát triển tiếp theo

Case study là nền tảng để xây dựng các tài liệu chi tiết hơn:

- BPMN AS-IS / TO-BE
- Business Requirements Document (BRD)
- Use Case
- Đặc tả quy tắc nghiệp vụ
- Tiêu chí nghiệm thu hệ thống (UAT)

## 10. Kiến thức và kỹ năng thể hiện

`Business Analysis` `BACCM` `BABOK v3` `Root Cause Analysis (5 Whys)` `Stakeholder Analysis` `Requirements Elicitation` `Business Rules` `Process Improvement` `KPI Design` `Data Governance`

## 11. Tác giả

**Nguyen Ho Tuyet Tran**: Business Analysis / BACCM Case Study



