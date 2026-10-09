# Bài tập 2: User Story, Acceptance Criteria và theo dõi trên Trello

## Bối cảnh

RikkeiCare là ứng dụng đặt lịch khám, kết nối bệnh nhân với các phòng khám đối tác. Nhóm sử dụng Trello để quản lý Product Backlog qua các cột:

`Product Backlog → Ready for Sprint → Sprint Backlog → In Progress → In Review/QA → Done`

Yêu cầu được thực hiện trong bài là **R5: “Phòng khám muốn tự cập nhật giá các gói khám.”**

# Bước 1. Viết User Story cho R5

## User Story

**Là một quản lý phòng khám, tôi muốn tự cập nhật giá các gói khám trên hệ thống, để thông tin giá hiển thị cho bệnh nhân luôn chính xác mà không phải nhờ admin RikkeiCare cập nhật qua email.**

## Giải thích vai trò

Vai trò phù hợp là **quản lý phòng khám** vì đây là người sở hữu và chịu trách nhiệm về thông tin giá của các gói khám tại phòng khám. Người này có quyền biết giá mới và cần cập nhật trực tiếp khi giá thay đổi.

Không chọn **admin RikkeiCare** vì admin hiện chỉ đang cập nhật hộ qua email. Đây là cách vận hành hiện tại, không phải người hưởng lợi chính của yêu cầu R5. Nếu chọn admin, User Story sẽ mô tả giải pháp trung gian cũ thay vì mục tiêu trao quyền tự phục vụ cho phòng khám.

# Bước 2. Viết Acceptance Criteria cho R5

## AC 1 — Cập nhật giá thành công

**Given** quản lý phòng khám đã đăng nhập và có quyền chỉnh sửa gói khám,  
**When** nhập một mức giá hợp lệ cho gói khám rồi nhấn **“Lưu”**,  
**Then** hệ thống lưu giá mới, hiển thị thông báo **“Cập nhật giá thành công”** và giá mới được hiển thị trên trang thông tin của gói khám.

## AC 2 — Cập nhật giá thất bại khi bỏ trống

**Given** quản lý phòng khám để trống ô giá,  
**When** nhấn **“Lưu”**,  
**Then** hệ thống không lưu dữ liệu, hiển thị thông báo **“Vui lòng nhập giá”** ngay tại ô giá và giữ quản lý ở lại màn hình cập nhật để bổ sung thông tin.

Hai tiêu chí trên có thể kiểm thử được: Tester biết dữ liệu đầu vào, thao tác cần thực hiện và kết quả mong đợi trong cả trường hợp thành công lẫn thất bại.

# Bước 3. Kiểm tra thẻ R5 đã sẵn sàng chưa

## Kết luận

**Chưa thể kéo thẻ R5 sang “Ready for Sprint” nếu thẻ mới chỉ có User Story và 2 Acceptance Criteria.**

| Điều kiện Definition of Ready | Trạng thái | Nhận xét |
| :--- | :---: | :--- |
| Có User Story đủ 3 vế | Đạt | Có vai trò, hành động và lợi ích rõ ràng. |
| Có tiêu chí nghiệm thu | Đạt | Đã có 2 AC theo mẫu Given – When – Then. |
| Đã được ước lượng | Chưa xác nhận | Đề bài chưa cho biết nhóm đã chấm Story Point hay chưa. |
| Đủ nhỏ để làm xong trong 1 Sprint | Chưa xác nhận | Cần nhóm thống nhất phạm vi và xác nhận không bao gồm các chức năng khác như phân quyền phức tạp, lịch sử giá hoặc duyệt giá. |

Vì còn thiếu ít nhất thông tin **ước lượng** và chưa xác nhận điều kiện **đủ nhỏ**, PO cần đưa thẻ vào buổi Backlog Refinement để nhóm chấm điểm và thống nhất phạm vi. Sau khi hoàn tất, R5 mới đủ điều kiện vào **Ready for Sprint**. Trong phần theo dõi Sprint, nhóm đã chọn R5 và thống nhất ước lượng là **3 point**.

# Bước 4. Hoàn thiện thẻ R5 trên Trello

## Thông tin thẻ

| Trường thông tin | Nội dung điền trên Trello |
| :--- | :--- |
| **Tên thẻ** | **R5 – Quản lý phòng khám tự cập nhật giá gói khám** |
| **Nhãn** | **Xanh dương – Feature** |
| **Người phụ trách** | **Nguyễn Văn A – Developer phụ trách module Quản lý phòng khám** *(thay bằng tên thành viên thực tế của nhóm)* |
| **Story Point** | **3 point** |
| **Hạn hoàn thành** | **Ngày cuối của Sprint**; nếu Sprint bắt đầu ngày 07/10/2026 thì đặt hạn **16/10/2026** |
| **Cột khi bắt đầu Sprint** | **Sprint Backlog** |

## Checklist đề xuất

1. Thiết kế màn hình và quyền cập nhật giá cho quản lý phòng khám.
2. Lập trình chức năng nhập, lưu và hiển thị giá mới.
3. Kiểm thử AC 1, AC 2 và chuyển thẻ qua In Review/QA.

## Vị trí trong cột

Vì R5 là việc **ưu tiên cao nhất**, thẻ nên được đặt **ở đầu cột “Sprint Backlog”**. Cách đặt này giúp nhóm nhận biết R5 là thẻ cần được xử lý trước trong Sprint, nhưng vẫn phải tuân thủ năng lực và sự thống nhất của cả nhóm.

# Bước 5. Đọc Burndown Chart

Sprint dài 10 ngày, nhóm cam kết 30 point. Đường lý tưởng giảm 3 point mỗi ngày, vì vậy:

| Ngày | 0 | 2 | 4 | 6 |
| :---: | ---: | ---: | ---: | ---: |
| Point còn lại theo thực tế | 30 | 26 | 23 | 20 |
| Point còn lại theo lý tưởng | 30 | 24 | 18 | 12 |

## a) So sánh ở ngày 6

Ở ngày 6:

- Theo đường lý tưởng, nhóm còn **12 point**.
- Theo thực tế, nhóm còn **20 point**.
- Chênh lệch: **20 − 12 = 8 point**.

Như vậy, nhóm đang **chậm 8 point** so với tiến độ lý tưởng. Burndown thực tế nằm cao hơn đường lý tưởng, nghĩa là nhóm đã hoàn thành ít công việc hơn mức kế hoạch tại thời điểm ngày 6.

## b) Có nên trừ 3 point khi thẻ R5 mới xong 80% không?

**Không nên.** Story Point được ghi nhận khi User Story hoàn thành theo Definition of Done, đã đáp ứng toàn bộ Acceptance Criteria và được QA nghiệm thu. “Xong 80%” chỉ cho thấy công việc đang thực hiện, chưa tạo ra một phần điểm có thể nghiệm thu độc lập.

Vì vậy, khi R5 mới hoàn thành 80%, nhóm vẫn giữ nguyên **3 point** trên biểu đồ. Chỉ khi R5 hoàn tất 100%, vượt qua AC 1 và AC 2, được review/QA chấp nhận và chuyển sang **Done** thì mới trừ toàn bộ 3 point khỏi Burndown Chart. Cách làm này giúp biểu đồ phản ánh đúng lượng giá trị đã hoàn thành, tránh tạo cảm giác nhóm đang nhanh hơn thực tế.

# Kết luận

R5 cần được viết lại thành User Story của **quản lý phòng khám**, có Acceptance Criteria rõ ràng cho cả trường hợp thành công và thất bại. Thẻ chỉ được đưa vào **Ready for Sprint** sau khi đã có đủ tiêu chí nghiệm thu, được ước lượng và xác nhận đủ nhỏ trong một Sprint. Khi vào Sprint, thẻ được gắn nhãn **Feature màu xanh dương**, giao cho Developer phụ trách, có checklist, hạn hoàn thành và đặt ở đầu cột Sprint Backlog do là ưu tiên cao nhất.
