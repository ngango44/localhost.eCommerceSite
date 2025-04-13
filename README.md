# localhost.eCommerceSite
1. Các thư mục chính:
    - src: Chứa source code của project
        - src/main/java: Chứa mã nguồn Java
        - src/main/resources: Chứa các file cấu hình và tài nguyên
        - src/test: Chứa mã nguồn test
    - target: Thư mục chứa các file được build
    - .github: Chứa các file cấu hình cho GitHub
    - docs: chứa tài liệu
2. Các file quan trọng:
   - pom.xml: File cấu hình Maven, định nghĩa dependencies và các cài đặt build
   - README.md: Tài liệu hướng dẫn sử dụng project
   - CHANGELOG.txt: Lịch sử các thay đổi của project
   - .gitignore: Danh sách các file/thư mục không theo dõi bởi Git
3. Công nghệ sử dụng
   - Java
   - Maven
   - Git
   - Có tích hợp với GitHub (có thư mục .github)
4. Phân tích chi tiết
   - **src/main/java/constants**: chứa các class bao gồm các hằng số (constant) của framework. Mục đích:
      - Lưu giữ các giá trị cố định được sử dụng cho toàn bộ framework
      - Tập trung quản lý các cấu hình và thông số quan trọng
      - Giúp code dễ bảo trì và mở rộng
   - **src/main/java/driver**:
     - Là một phần quan trọng của framework automation testing
     - Chịu trách nhiệm quản lý và khởi tạo WebDriver
     - Cung cấp các cơ chế để chạy test trên nhiều browser và môi trường khác nhau
   - **src/main/java/Helpers**:
     - Tập trung vào các thao tác cốt lõi của framework
     - Thường có phạm vi lớn hơn
     - Liên quan trực tiếp đến việc test automation
     - Ví dụ: ExcelHelpers, PropertiesHelpers, CaptureHelpers
   - **src/main/java/Utils**:
     - Tập trung vào các tiện ích nhỏ, cụ thể
     - Thường có phạm vi nhỏ hơn
     - Có thể tái sử dụng trong nhiều ngữ cảnh
     - Ví dụ: DateUtils, ZipUtils, LogUtils
   - **src\test\java\com\[có thể tên cty hoặc mô hình TDD, BDD -tái sử dụng src\java ở trên]\dataprovider**
     - Quản lý và cung cấp dữ liệu test
     - Tách biệt dữ liệu test khỏi code test
     - Hỗ trợ data-driven testing
     - Dễ dàng mở rộng và bảo trì
   - **src\test\java\com\[có thể tên cty hoặc mô hình TDD, BDD -tái sử dụng src\java ở trên]\listeners** : Việc sử dụng listeners giúp test automation linh hoạt và mạnh mẽ hơn, đặc biệt trong việc xử lý các tình huống đặc biệt và cải thiện reporting.
     - Tự động hóa các thao tác trong test
     - Cải thiện reporting
     - Xử lý lỗi hiệu quả
     - Tăng tính ổn định của test
   - **src\test\java\com\[có thể tên cty hoặc mô hình TDD, BDD -tái sử dụng src\java ở trên]\project**:  page object và testcase
   - **src\test\java\com\[có thể tên cty hoặc mô hình TDD, BDD -tái sử dụng src\java ở trên]\resource**:  suites, data test,config