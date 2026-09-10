# REQUIREMENTS

# EngCoach -- Hệ thống luyện thi tiếng Anh

## 1. Product Goal

Xây dựng **EngCoach**, một hệ thống luyện thi tiếng Anh trên nền tảng
Web, hỗ trợ người học luyện tập, kiểm tra và theo dõi năng lực tiếng Anh
thông qua hệ thống câu hỏi, bài thi và các chức năng hỗ trợ bởi AI.

Hệ thống hướng đến việc giúp người học:

-   Luyện tập tiếng Anh theo từng kỹ năng và chủ đề.
-   Làm bài thi thử và nhận kết quả ngay sau khi hoàn thành.
-   Theo dõi quá trình và kết quả học tập.
-   Xác định những chủ đề còn yếu.
-   Nhận giải thích cho các câu trả lời sai.
-   Nhận đề xuất nội dung luyện tập phù hợp với năng lực.

------------------------------------------------------------------------

## 2. Actors / User Roles

### 2.1. Student -- Người học

Người sử dụng chính của hệ thống.

Có thể:

-   Đăng ký và đăng nhập.
-   Làm bài luyện tập.
-   Làm bài thi thử.
-   Xem kết quả.
-   Xem lịch sử làm bài.
-   Theo dõi tiến độ.
-   Xem các chủ đề còn yếu.
-   Sử dụng AI để giải thích câu hỏi.
-   Nhận đề xuất bài luyện tập.

### 2.2. Admin -- Quản trị viên

Quản lý nội dung và hoạt động của hệ thống.

Có thể:

-   Quản lý tài khoản người dùng.
-   Quản lý câu hỏi.
-   Quản lý chủ đề.
-   Quản lý bài thi.
-   Quản lý nội dung AI sinh ra.
-   Xem thống kê hệ thống.

### 2.3. AI Assistant

Không phải người dùng trực tiếp nhưng là thành phần hỗ trợ của hệ thống.

Có nhiệm vụ:

-   Giải thích câu hỏi.
-   Phân tích kết quả.
-   Xác định điểm yếu.
-   Đề xuất nội dung luyện tập.
-   Có thể hỗ trợ sinh câu hỏi theo yêu cầu của hệ thống.

------------------------------------------------------------------------

# 3. Product Backlog

## Epic 1 -- User Authentication & Profile

### US-01 -- Đăng ký tài khoản

**As a:** Student\
**I want to:** đăng ký tài khoản\
**So that:** tôi có thể sử dụng và lưu lại quá trình luyện thi.

**Acceptance Criteria:**

-   Người dùng nhập email, username và password.
-   Hệ thống kiểm tra các trường bắt buộc.
-   Email/username không được trùng.
-   Password phải đáp ứng yêu cầu bảo mật.
-   Đăng ký thành công thì tài khoản được tạo trong hệ thống.
-   Nếu dữ liệu không hợp lệ, hệ thống hiển thị thông báo lỗi.

### US-02 -- Đăng nhập

**As a:** Student\
**I want to:** đăng nhập vào hệ thống\
**So that:** tôi có thể sử dụng các chức năng cá nhân.

**Acceptance Criteria:**

-   Người dùng nhập username/email và password.
-   Hệ thống xác thực thông tin.
-   Đăng nhập thành công thì chuyển đến trang chính.
-   Sai thông tin thì hiển thị thông báo lỗi.

### US-03 -- Quản lý hồ sơ cá nhân

**As a:** Student\
**I want to:** xem và cập nhật thông tin cá nhân\
**So that:** thông tin tài khoản của tôi luôn chính xác.

**Acceptance Criteria:**

-   Xem được thông tin cá nhân.
-   Có thể cập nhật thông tin được phép.
-   Hệ thống lưu thông tin sau khi cập nhật thành công.

------------------------------------------------------------------------

## Epic 2 -- Question Bank

### US-04 -- Xem danh sách câu hỏi

**As a:** Student\
**I want to:** xem các câu hỏi luyện tập\
**So that:** tôi có thể lựa chọn nội dung muốn luyện.

**Acceptance Criteria:**

-   Hiển thị danh sách câu hỏi.
-   Có thể lọc theo kỹ năng.
-   Có thể lọc theo chủ đề.
-   Có thể lọc theo mức độ khó.
-   Mỗi câu hỏi hiển thị đầy đủ nội dung và các lựa chọn.

### US-05 -- Làm bài luyện tập

**As a:** Student\
**I want to:** làm các câu hỏi luyện tập\
**So that:** tôi có thể cải thiện kiến thức.

**Acceptance Criteria:**

-   Người dùng có thể chọn đáp án.
-   Có thể chuyển giữa các câu hỏi.
-   Hệ thống ghi nhận câu trả lời.
-   Người dùng có thể nộp bài.
-   Hệ thống tính kết quả sau khi nộp.

### US-06 -- Xem đáp án và giải thích

**As a:** Student\
**I want to:** xem đáp án và lời giải\
**So that:** tôi hiểu nguyên nhân mình trả lời sai.

**Acceptance Criteria:**

-   Hiển thị đáp án đúng.
-   Hiển thị đáp án người dùng đã chọn.
-   Nếu trả lời sai, hiển thị giải thích.
-   Người dùng có thể yêu cầu AI giải thích sâu hơn.

------------------------------------------------------------------------

## Epic 3 -- Mock Exam

### US-07 -- Làm bài thi thử

**As a:** Student\
**I want to:** làm một bài thi thử\
**So that:** tôi có thể đánh giá trình độ của mình.

**Acceptance Criteria:**

-   Người dùng chọn bài thi.
-   Hệ thống hiển thị thông tin bài thi.
-   Bài thi có thời gian làm bài.
-   Hệ thống ghi nhận câu trả lời.
-   Người dùng có thể nộp bài.
-   Hệ thống tự động tính điểm.

### US-08 -- Theo dõi thời gian làm bài

**As a:** Student\
**I want to:** biết thời gian còn lại\
**So that:** tôi có thể quản lý thời gian khi làm bài.

**Acceptance Criteria:**

-   Hiển thị thời gian còn lại.
-   Thời gian được cập nhật liên tục.
-   Khi hết thời gian, hệ thống tự động nộp bài.

### US-09 -- Xem kết quả thi

**As a:** Student\
**I want to:** xem kết quả sau khi hoàn thành bài thi\
**So that:** tôi biết mức độ làm bài của mình.

**Acceptance Criteria:**

-   Hiển thị tổng điểm.
-   Hiển thị số câu đúng/sai.
-   Hiển thị tỷ lệ chính xác.
-   Hiển thị kết quả theo từng kỹ năng/chủ đề nếu có dữ liệu.

------------------------------------------------------------------------

## Epic 4 -- Learning Progress

### US-10 -- Xem lịch sử làm bài

**As a:** Student\
**I want to:** xem lịch sử các bài đã làm\
**So that:** tôi có thể theo dõi quá trình luyện tập.

**Acceptance Criteria:**

-   Hiển thị danh sách các bài đã hoàn thành.
-   Hiển thị thời gian làm bài.
-   Hiển thị điểm số.
-   Có thể xem lại chi tiết kết quả.

### US-11 -- Theo dõi tiến độ học tập

**As a:** Student\
**I want to:** xem tiến độ học tập\
**So that:** tôi biết mình đang cải thiện như thế nào.

**Acceptance Criteria:**

-   Hiển thị số lượng bài đã hoàn thành.
-   Hiển thị điểm trung bình.
-   Hiển thị tỷ lệ chính xác.
-   Hiển thị sự thay đổi kết quả theo thời gian.

### US-12 -- Xác định chủ đề yếu

**As a:** Student\
**I want to:** biết những chủ đề mình còn yếu\
**So that:** tôi có thể tập trung luyện tập.

**Acceptance Criteria:**

-   Hệ thống phân tích kết quả các bài đã làm.
-   Tính tỷ lệ chính xác theo từng chủ đề.
-   Xác định các chủ đề có kết quả thấp.
-   Hiển thị danh sách chủ đề cần cải thiện.

------------------------------------------------------------------------

## Epic 5 -- AI Assistant

### US-13 -- AI giải thích câu hỏi

**As a:** Student\
**I want to:** yêu cầu AI giải thích câu hỏi\
**So that:** tôi hiểu kiến thức đằng sau câu hỏi.

**Acceptance Criteria:**

-   Người dùng có thể gửi câu hỏi cho AI.
-   AI nhận biết nội dung câu hỏi và đáp án.
-   AI giải thích lý do lựa chọn đáp án đúng.
-   AI giải thích lỗi của đáp án sai.
-   Nội dung giải thích phải phù hợp với ngữ cảnh câu hỏi.

### US-14 -- AI phân tích kết quả

**As a:** Student\
**I want to:** nhận phân tích kết quả bằng AI\
**So that:** tôi biết mình cần cải thiện kỹ năng nào.

**Acceptance Criteria:**

-   AI sử dụng kết quả luyện tập của người dùng.
-   Phân tích điểm mạnh.
-   Phân tích điểm yếu.
-   Xác định các chủ đề cần ưu tiên.
-   Đưa ra nhận xét dễ hiểu đối với người học.

### US-15 -- AI đề xuất bài luyện tập

**As a:** Student\
**I want to:** nhận đề xuất bài luyện tập cá nhân hóa\
**So that:** tôi có thể luyện tập đúng những nội dung mình còn yếu.

**Acceptance Criteria:**

-   Hệ thống sử dụng lịch sử kết quả của người dùng.
-   AI xác định các nội dung cần cải thiện.
-   Hệ thống đề xuất chủ đề/bài luyện phù hợp.
-   Đề xuất có thể thay đổi khi kết quả học tập thay đổi.

### US-16 -- AI sinh câu hỏi

**As a:** Admin\
**I want to:** sử dụng AI để hỗ trợ tạo câu hỏi\
**So that:** tôi có thể nhanh chóng bổ sung ngân hàng câu hỏi.

**Acceptance Criteria:**

-   Admin nhập chủ đề.
-   Admin chọn kỹ năng và mức độ khó.
-   AI tạo câu hỏi và các lựa chọn.
-   AI cung cấp đáp án và giải thích.
-   Admin có thể chỉnh sửa.
-   Admin phải kiểm tra và phê duyệt trước khi câu hỏi được đưa vào ngân
    hàng chính thức.

------------------------------------------------------------------------

## Epic 6 -- Admin Management

### US-17 -- Quản lý câu hỏi

**As a:** Admin\
**I want to:** thêm, sửa, xóa và xem câu hỏi\
**So that:** tôi có thể quản lý ngân hàng câu hỏi.

**Acceptance Criteria:**

-   Admin có thể tạo câu hỏi.
-   Có thể cập nhật câu hỏi.
-   Có thể xóa câu hỏi.
-   Có thể thiết lập đáp án đúng.
-   Có thể thiết lập chủ đề và độ khó.
-   Hệ thống kiểm tra dữ liệu trước khi lưu.

### US-18 -- Quản lý chủ đề

**As a:** Admin\
**I want to:** quản lý các chủ đề luyện thi\
**So that:** câu hỏi được phân loại rõ ràng.

**Acceptance Criteria:**

-   Thêm chủ đề.
-   Sửa chủ đề.
-   Xóa chủ đề.
-   Gán câu hỏi vào chủ đề.

### US-19 -- Quản lý bài thi

**As a:** Admin\
**I want to:** tạo và quản lý các bài thi\
**So that:** người học có thể thực hiện các bài thi thử.

**Acceptance Criteria:**

-   Tạo bài thi.
-   Thiết lập thời gian.
-   Chọn số lượng câu hỏi.
-   Chọn chủ đề/kỹ năng.
-   Chỉnh sửa bài thi.
-   Xóa bài thi.

### US-20 -- Xem thống kê hệ thống

**As a:** Admin\
**I want to:** xem thống kê hoạt động\
**So that:** tôi có thể đánh giá tình trạng sử dụng hệ thống.

**Acceptance Criteria:**

-   Số lượng người dùng.
-   Số lượng bài thi.
-   Số lượng câu hỏi.
-   Số lượt làm bài.
-   Điểm trung bình của người dùng.

------------------------------------------------------------------------

# 4. Non-Functional Requirements

## NFR-01 -- Performance

-   Thời gian phản hồi các API thông thường nên ở mức chấp nhận được đối
    với ứng dụng Web.
-   Kết quả chấm điểm phải được trả về ngay sau khi người dùng hoàn
    thành bài.
-   Hệ thống không được tải lại toàn bộ trang khi thực hiện các thao tác
    thông thường.

## NFR-02 -- Security

-   Password phải được mã hóa trước khi lưu.
-   Các API yêu cầu đăng nhập phải được xác thực.
-   Phân quyền giữa Student và Admin.
-   Người dùng chỉ được truy cập dữ liệu cá nhân của mình.
-   Các API quản trị chỉ được phép truy cập bởi Admin.

## NFR-03 -- Usability

-   Giao diện đơn giản và dễ sử dụng.
-   Có thể sử dụng trên máy tính và thiết bị có màn hình nhỏ.
-   Câu hỏi và đáp án phải được hiển thị rõ ràng.
-   Thông báo lỗi phải dễ hiểu.

## NFR-04 -- Reliability

-   Hệ thống phải lưu kết quả sau khi người dùng hoàn thành bài.
-   Không làm mất kết quả nếu người dùng hoàn thành và nộp bài thành
    công.
-   Dữ liệu câu hỏi và kết quả phải được lưu trữ nhất quán.

## NFR-05 -- AI Reliability

-   Kết quả do AI tạo ra không được đưa trực tiếp vào hệ thống mà không
    kiểm tra trong các nội dung quan trọng.
-   Nội dung AI sinh câu hỏi phải được Admin kiểm duyệt.
-   Nội dung AI giải thích phải được giới hạn trong ngữ cảnh của câu
    hỏi.
-   Hệ thống phải có cơ chế xử lý khi AI không thể đưa ra câu trả lời
    phù hợp.

------------------------------------------------------------------------

# 5. MVP -- Minimum Viable Product

Để tránh phạm vi quá lớn, phiên bản đầu tiên của EngCoach nên tập trung
vào:

## Student

-   Đăng ký/đăng nhập.
-   Làm bài luyện tập.
-   Làm bài thi thử.
-   Chấm điểm.
-   Xem đáp án và giải thích.
-   Xem lịch sử kết quả.
-   Xem tiến độ.
-   Xác định chủ đề yếu.
-   AI giải thích câu hỏi.
-   AI đề xuất nội dung luyện tập.

## Admin

-   Quản lý câu hỏi.
-   Quản lý chủ đề.
-   Quản lý bài thi.
-   Kiểm duyệt câu hỏi do AI sinh.

## AI

-   AI Question Explanation.
-   AI Weakness Analysis.
-   AI Personalized Recommendation.
-   AI Question Generation.

------------------------------------------------------------------------

# 6. Product Backlog ưu tiên

    Priority ID      User Story              Ưu tiên
  ---------- ------- ----------------------- ---------
           1 US-01   Đăng ký                 Must
           2 US-02   Đăng nhập               Must
           3 US-04   Xem câu hỏi             Must
           4 US-05   Làm bài luyện tập       Must
           5 US-07   Làm bài thi thử         Must
           6 US-09   Xem kết quả             Must
           7 US-10   Lịch sử làm bài         Must
           8 US-17   Quản lý câu hỏi         Must
           9 US-19   Quản lý bài thi         Must
          10 US-13   AI giải thích câu hỏi   Must
          11 US-12   Phân tích chủ đề yếu    Should
          12 US-14   AI phân tích kết quả    Should
          13 US-15   AI đề xuất bài luyện    Should
          14 US-16   AI sinh câu hỏi         Should
          15 US-11   Theo dõi tiến độ        Should
          16 US-20   Thống kê Admin          Could
          17 US-03   Quản lý hồ sơ           Could
          18 US-18   Quản lý chủ đề          Could

------------------------------------------------------------------------

# 7. Định hướng Sprint

## Sprint 1 -- Foundation

-   Authentication
-   User
-   Database
-   Phân quyền Student/Admin
-   Project architecture

## Sprint 2 -- Question Bank

-   Question
-   Topic
-   Question management
-   Practice mode

## Sprint 3 -- Exam

-   Mock exam
-   Timer
-   Submit exam
-   Scoring
-   Result

## Sprint 4 -- Learning Analytics

-   History
-   Progress
-   Topic performance
-   Weakness analysis

## Sprint 5 -- AI

-   AI explanation
-   AI result analysis
-   AI recommendation

## Sprint 6 -- AI Content & Finalization

-   AI question generation
-   Admin approval
-   Testing
-   Bug fixing
-   Deployment
-   Documentation

------------------------------------------------------------------------

# 8. Product Scope

## In Scope

-   Web-based English exam preparation.
-   User authentication.
-   Question bank.
-   Practice.
-   Mock exams.
-   Scoring.
-   Result history.
-   Learning progress.
-   Topic/skill analysis.
-   AI explanation.
-   AI analysis.
-   AI recommendation.
-   AI-assisted question generation.
-   Admin management.

## Out of Scope for MVP

-   Thanh toán trực tuyến.
-   Livestream lớp học.
-   Video course.
-   Social network.
-   Marketplace.
-   Hệ thống thi có giám sát bằng camera.
-   Nhận diện khuôn mặt.
-   AI chấm Speaking/Pronunciation chuyên sâu.
-   AI chấm Writing chuyên sâu.

Các chức năng này có thể được xem xét ở các phiên bản sau nếu còn thời
gian và nguồn lực.

------------------------------------------------------------------------

# 9. Product Success Criteria

EngCoach được xem là đạt yêu cầu MVP khi:

-   Student có thể đăng ký, đăng nhập và sử dụng hệ thống.
-   Student có thể hoàn thành một bài luyện tập và bài thi thử.
-   Hệ thống chấm điểm chính xác theo đáp án được cấu hình.
-   Kết quả được lưu và có thể xem lại.
-   Hệ thống có thể phân tích kết quả theo chủ đề/kỹ năng.
-   AI có thể giải thích câu hỏi trong phạm vi được yêu cầu.
-   AI có thể đưa ra đề xuất luyện tập dựa trên kết quả.
-   Admin có thể quản lý ngân hàng câu hỏi và bài thi.
-   Câu hỏi do AI sinh ra được kiểm duyệt trước khi sử dụng.
-   Sản phẩm có thể vận hành và được trình bày/demo hoàn chỉnh.
