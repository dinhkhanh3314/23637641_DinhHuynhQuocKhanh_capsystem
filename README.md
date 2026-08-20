# CAB System – Phân tích yêu cầu
# Bước 1: Hiểu rõ hệ thống

## 1. Bối cảnh nghiệp vụ và lý do hệ thống cũ không đáp ứng được

Công ty ABC là một doanh nghiệp cung cấp dịch vụ đặt xe trực tuyến. Hiện tại khách hàng có thể liên hệ với tổng đài hoặc sử dụng một ứng dụng đơn giản để yêu cầu xe.

Hệ thống hiện tại còn một số hạn chế:

- Việc phân công tài xế chủ yếu được thực hiện thủ công.
- Khách hàng khó theo dõi trạng thái chuyến đi.
- Thông tin thanh toán chưa được quản lý tập trung.
- Bộ phận vận hành gặp khó khăn khi muốn mở rộng hệ thống.
- Hệ thống hiện tại khó đáp ứng khi số lượng khách hàng và tài xế tăng.

Những hạn chế này ảnh hưởng đến quá trình vận hành dịch vụ, trải nghiệm của khách hàng và khả năng mở rộng của doanh nghiệp.

## 2. Giải pháp mới và hệ thống mới

Công ty ABC mong muốn xây dựng **CAB System – Nền tảng đặt xe** nhằm hỗ trợ quy trình đặt xe từ khi khách hàng tạo yêu cầu cho đến khi chuyến đi hoàn thành.

Hệ thống mới hỗ trợ các hoạt động chính:

- Khách hàng đăng ký tài khoản, đăng nhập và cập nhật thông tin cá nhân.
- Khách hàng nhập điểm đón, điểm đến và lựa chọn loại xe.
- Khách hàng gửi yêu cầu đặt xe.
- Hệ thống xác định các tài xế phù hợp dựa trên vị trí, trạng thái sẵn sàng và một số tiêu chí vận hành khác.
- Hệ thống ưu tiên tài xế phù hợp và gần khách hàng.
- Tài xế nhận được thông báo và có thể chấp nhận hoặc từ chối chuyến.
- Nếu tài xế được đề xuất không phản hồi hoặc từ chối, hệ thống tiếp tục tìm tài xế khác mà không yêu cầu khách hàng tạo lại yêu cầu.
- Nếu không tìm được tài xế, khách hàng được thông báo rõ ràng.
- Khách hàng biết tài xế nào đã nhận chuyến và thời gian dự kiến tài xế đến.
- Tài xế cập nhật trạng thái chuyến gồm đã đến điểm đón, đã đón khách, đang di chuyển và hoàn thành chuyến.
- Khách hàng theo dõi được trạng thái hiện tại của chuyến đi.
- Sau khi chuyến đi hoàn thành, hệ thống xác định số tiền khách hàng phải trả dựa trên loại dịch vụ và thông tin chuyến đi.
- Khách hàng có thể thanh toán bằng tiền mặt hoặc phương thức thanh toán điện tử.
- Thanh toán điện tử được thực hiện thông qua nhà cung cấp thanh toán bên ngoài.
- Hệ thống CAB không lưu trực tiếp thông tin nhạy cảm của thẻ hoặc tài khoản thanh toán.
- Khách hàng nhận được thông báo khi yêu cầu đặt xe được tiếp nhận, khi có tài xế nhận chuyến, khi tài xế đến điểm đón, khi chuyến hoàn thành và khi thanh toán có kết quả.
- Tài xế nhận được thông báo về các chuyến mới hoặc những thay đổi liên quan đến chuyến đang thực hiện.
- Khách hàng có thể xem lịch sử chuyến đi, số tiền phải trả và đánh giá tài xế sau khi hoàn thành chuyến.
- Nhân viên vận hành có thể quản lý khách hàng, tài xế, phương tiện và chuyến đi.
- Nhân viên vận hành có thể xem các chuyến đang diễn ra, kiểm tra trạng thái tài xế, hỗ trợ xử lý các trường hợp chuyến bị lỗi và tra cứu lịch sử giao dịch.

Quy trình cốt lõi của hệ thống:

**Đặt xe → Tìm tài xế → Nhận chuyến → Thực hiện chuyến → Hoàn thành chuyến → Tính cước → Thanh toán → Đánh giá**

## 3. Các đối tượng tham gia hệ thống

| Đối tượng | Vai trò |
|---|---|
| Khách hàng | Đăng ký, đăng nhập, đặt xe, theo dõi chuyến đi, thanh toán và đánh giá tài xế |
| Tài xế | Quản lý hồ sơ, thông tin phương tiện, nhận hoặc từ chối chuyến và thực hiện chuyến |
| Nhân viên vận hành | Quản lý khách hàng, tài xế, phương tiện, chuyến đi và hỗ trợ xử lý các trường hợp chuyến bị lỗi |
| Nhà cung cấp thanh toán bên ngoài | Xử lý các giao dịch thanh toán điện tử |
| Nhà cung cấp dịch vụ thông báo | Hỗ trợ gửi thông báo đến khách hàng và tài xế |

## 4. Giá trị kinh doanh của hệ thống mới

| Đối tượng | Giá trị kinh doanh |
|---|---|
| Khách hàng | Đặt xe thuận tiện hơn, theo dõi được trạng thái chuyến đi, biết thông tin tài xế, thanh toán và đánh giá tài xế |
| Tài xế | Nhận yêu cầu chuyến, chủ động chấp nhận hoặc từ chối chuyến và cập nhật trạng thái chuyến |
| Nhân viên vận hành | Quản lý tập trung khách hàng, tài xế, phương tiện và chuyến đi; theo dõi và hỗ trợ xử lý các chuyến |
| Doanh nghiệp | Giảm sự phụ thuộc vào phân công tài xế thủ công, hỗ trợ tự động hóa việc tìm và phân công tài xế, cải thiện trải nghiệm khách hàng và hỗ trợ phục vụ số lượng lớn khách hàng và tài xế |

Giá trị cốt lõi của hệ thống là hỗ trợ Công ty ABC vận hành quy trình đặt xe từ khi khách hàng tạo yêu cầu, hệ thống tìm và phân công tài xế, tài xế thực hiện chuyến, chuyến hoàn thành, tính cước, thanh toán đến đánh giá tài xế.

# BƯỚC 2: XÁC ĐỊNH STAKEHOLDER, VAI TRÒ VÀ THIẾT LẬP STAKEHOLDER MATRIX

## 1. Xác định Stakeholder và vai trò

| Stakeholder | Vai trò trong hệ thống |
|---|---|
| Ban giám đốc | Chủ sở hữu sản phẩm, quyết định mục tiêu và định hướng của CAB System |
| Khách hàng | Người sử dụng dịch vụ đặt xe |
| Tài xế | Người cung cấp dịch vụ vận chuyển |
| Nhân viên vận hành | Người quản lý và giám sát hoạt động đặt xe |
| Nhà cung cấp thanh toán bên ngoài | Đối tác xử lý thanh toán điện tử |
| Nhà cung cấp dịch vụ thông báo | Đối tác hỗ trợ gửi thông báo |

## 2. Phân tích mức độ ảnh hưởng và quan tâm

| Stakeholder | Power | Interest | Lý do |
|---|---|---|---|
| Ban giám đốc | Cao | Cao | Có quyền quyết định và chịu trách nhiệm về sản phẩm |
| Nhân viên vận hành | Cao | Cao | Trực tiếp quản lý và giám sát hoạt động đặt xe |
| Khách hàng | Thấp | Cao | Sử dụng trực tiếp sản phẩm |
| Tài xế | Thấp | Cao | Sử dụng trực tiếp hệ thống để nhận và thực hiện chuyến |
| Nhà cung cấp thanh toán bên ngoài | Cao | Thấp | Có ảnh hưởng đến hoạt động thanh toán nhưng không tham gia trực tiếp vào quy trình đặt xe |
| Nhà cung cấp dịch vụ thông báo | Thấp | Thấp | Hỗ trợ một phần hoạt động của hệ thống |

## 3. Stakeholder Matrix

```mermaid
quadrantChart
    title Stakeholder Matrix - Power / Interest
    x-axis "Interest thấp" --> "Interest cao"
    y-axis "Power thấp" --> "Power cao"
    "Nhà cung cấp dịch vụ thông báo": [0.25, 0.25]
    "Khách hàng": [0.85, 0.30]
    "Tài xế": [0.80, 0.35]
    "Nhà cung cấp thanh toán": [0.30, 0.80]
    "Nhân viên vận hành": [0.85, 0.85]
    "Ban giám đốc": [0.90, 0.90]
```

## 4. Chiến lược quản lý Stakeholder

| Nhóm | Stakeholder | Chiến lược |
|---|---|---|
| Power cao – Interest cao | Ban giám đốc, Nhân viên vận hành | Quản lý chặt chẽ, trao đổi thường xuyên và tham gia vào các quyết định quan trọng |
| Power thấp – Interest cao | Khách hàng, Tài xế | Duy trì sự tham gia, thường xuyên thu thập nhu cầu và phản hồi |
| Power cao – Interest thấp | Nhà cung cấp thanh toán bên ngoài | Duy trì sự hài lòng và phối hợp khi có vấn đề liên quan đến tích hợp |
| Power thấp – Interest thấp | Nhà cung cấp dịch vụ thông báo | Theo dõi và phối hợp khi phát sinh vấn đề |

## Bước 3. Mục đích nghiệp vụ

CAB System được xây dựng nhằm giải quyết các hạn chế của hệ thống đặt xe hiện tại và hỗ trợ Công ty ABC cải thiện hoạt động cung cấp dịch vụ đặt xe trực tuyến.

### Mục đích chính

- **Tự động hóa quá trình đặt xe và tìm tài xế**, giảm sự phụ thuộc vào việc phân công tài xế thủ công.
- **Cải thiện trải nghiệm khách hàng** bằng cách cho phép khách hàng chủ động đặt xe và theo dõi trạng thái chuyến đi.
- **Hỗ trợ tài xế tiếp nhận và thực hiện chuyến** thông qua hệ thống thay vì phụ thuộc vào quá trình điều phối thủ công.
- **Quản lý tập trung thông tin** về khách hàng, tài xế, phương tiện, chuyến đi và giao dịch.
- **Hỗ trợ thanh toán** bằng tiền mặt và phương thức thanh toán điện tử thông qua nhà cung cấp bên ngoài.
- **Cải thiện khả năng theo dõi và xử lý hoạt động vận hành** thông qua giao diện dành cho nhân viên vận hành.
- **Giảm thời gian xử lý khi tìm tài xế** bằng cách tự động tiếp tục tìm tài xế khác khi tài xế được đề xuất không phản hồi hoặc từ chối.
- **Cung cấp thông tin và dữ liệu cần thiết cho doanh nghiệp** để theo dõi hoạt động đặt xe và tình hình vận hành.

### Kết quả nghiệp vụ mong muốn

| Mục đích | Kết quả mong muốn |
|---|---|
| Tự động hóa đặt xe | Khách hàng có thể tạo yêu cầu và hệ thống tự động xử lý quá trình tìm tài xế |
| Cải thiện trải nghiệm khách hàng | Khách hàng có thể biết trạng thái yêu cầu, thông tin tài xế và trạng thái chuyến đi |
| Nâng cao hiệu quả tìm tài xế | Hệ thống có thể tiếp tục tìm tài xế khác khi tài xế được đề xuất không nhận chuyến |
| Quản lý tập trung | Thông tin khách hàng, tài xế, phương tiện, chuyến đi và giao dịch được quản lý trong hệ thống |
| Hỗ trợ thanh toán | Khách hàng có thể thanh toán bằng tiền mặt hoặc phương thức điện tử |
| Hỗ trợ vận hành | Nhân viên vận hành có thể theo dõi chuyến và hỗ trợ xử lý các trường hợp phát sinh |
| Hỗ trợ hoạt động kinh doanh | Doanh nghiệp có nền tảng để phục vụ số lượng lớn khách hàng và tài xế hơn hệ thống hiện tại |

### Mục tiêu tổng quát

**Xây dựng một nền tảng đặt xe giúp Công ty ABC tự động hóa quy trình từ khi khách hàng tạo yêu cầu, tìm và phân công tài xế, thực hiện chuyến, tính cước, thanh toán đến đánh giá sau chuyến, đồng thời hỗ trợ doanh nghiệp quản lý và theo dõi hoạt động đặt xe hiệu quả hơn.**

# BƯỚC 4: XÁC ĐỊNH PHẠM VI DỰ ÁN

## 1. Các module trong phạm vi

### Module 1: Quản lý tài khoản

- Đăng ký tài khoản khách hàng.
- Đăng nhập.
- Cập nhật thông tin cá nhân.
- Quản lý thông tin tài xế.
- Quản lý thông tin phương tiện.

### Module 2: Đặt xe

- Nhập điểm đón.
- Nhập điểm đến.
- Lựa chọn loại xe.
- Gửi yêu cầu đặt xe.
- Theo dõi trạng thái yêu cầu đặt xe.

### Module 3: Tìm và phân công tài xế

- Tìm tài xế phù hợp.
- Ưu tiên tài xế gần khách hàng.
- Gửi yêu cầu chuyến đến tài xế.
- Tài xế chấp nhận hoặc từ chối chuyến.
- Tiếp tục tìm tài xế khác khi tài xế từ chối hoặc không phản hồi.
- Thông báo khi không tìm được tài xế.

### Module 4: Quản lý chuyến đi

- Tài xế cập nhật trạng thái chuyến.
- Khách hàng theo dõi trạng thái chuyến.
- Lưu thông tin chuyến đi.
- Hoàn thành chuyến.

### Module 5: Tính cước và thanh toán

- Tính số tiền khách hàng phải trả.
- Thanh toán bằng tiền mặt.
- Thanh toán điện tử thông qua nhà cung cấp bên ngoài.
- Xử lý kết quả thanh toán.
- Thông báo kết quả thanh toán.

### Module 6: Thông báo

- Thông báo yêu cầu đặt xe được tiếp nhận.
- Thông báo khi tài xế nhận chuyến.
- Thông báo khi tài xế đến điểm đón.
- Thông báo khi chuyến hoàn thành.
- Thông báo kết quả thanh toán.
- Thông báo chuyến mới cho tài xế.

### Module 7: Lịch sử và đánh giá

- Xem lịch sử chuyến đi.
- Xem số tiền phải trả.
- Đánh giá tài xế sau chuyến.

### Module 8: Quản lý vận hành

- Quản lý khách hàng.
- Quản lý tài xế.
- Quản lý phương tiện.
- Theo dõi chuyến đang diễn ra.
- Kiểm tra trạng thái tài xế.
- Tra cứu lịch sử giao dịch.
- Hỗ trợ xử lý các trường hợp chuyến bị lỗi.
  
## Bước 5. Yêu cầu nghiệp vụ

| Yêu cầu nghiệp vụ | Yêu cầu hệ thống |
|---|---|
| Cung cấp dịch vụ đặt xe trực tuyến | Hệ thống phải cho phép khách hàng nhập điểm đón, điểm đến, lựa chọn loại xe và gửi yêu cầu đặt xe. |
| Tự động tìm và phân công tài xế | Hệ thống phải tự động xác định và lựa chọn tài xế phù hợp dựa trên vị trí, trạng thái sẵn sàng và các tiêu chí được xác định. |
| Xử lý trường hợp tài xế không nhận chuyến | Hệ thống phải tự động tìm tài xế khác khi tài xế được đề xuất từ chối hoặc không phản hồi. |
| Quản lý quá trình thực hiện chuyến | Hệ thống phải cho phép tài xế cập nhật trạng thái chuyến và cho phép khách hàng theo dõi trạng thái hiện tại của chuyến. |
| Quản lý khách hàng, tài xế và phương tiện | Hệ thống phải cho phép quản lý thông tin khách hàng, tài xế và phương tiện. |
| Tính cước chuyến đi | Hệ thống phải xác định số tiền khách hàng phải trả dựa trên thông tin chuyến đi và loại dịch vụ. |
| Hỗ trợ thanh toán | Hệ thống phải hỗ trợ thanh toán bằng tiền mặt và thanh toán điện tử thông qua nhà cung cấp thanh toán bên ngoài. |
| Quản lý kết quả thanh toán | Hệ thống phải tiếp nhận và lưu trạng thái giao dịch thanh toán, đồng thời thông báo kết quả cho khách hàng. |
| Cung cấp thông báo | Hệ thống phải gửi thông báo đến khách hàng và tài xế khi xảy ra các sự kiện quan trọng trong quá trình đặt và thực hiện chuyến. |
| Quản lý lịch sử chuyến đi | Hệ thống phải lưu trữ thông tin chuyến để khách hàng có thể tra cứu lịch sử và số tiền phải trả. |
| Đánh giá tài xế | Hệ thống phải cho phép khách hàng đánh giá tài xế sau khi chuyến đi hoàn thành. |
| Hỗ trợ nhân viên vận hành | Hệ thống phải cung cấp giao diện quản trị để nhân viên vận hành quản lý khách hàng, tài xế, phương tiện và chuyến đi. |
| Theo dõi và xử lý chuyến | Hệ thống phải cho phép nhân viên vận hành xem các chuyến đang diễn ra, kiểm tra trạng thái tài xế và hỗ trợ xử lý các trường hợp chuyến bị lỗi. |
| Phân quyền quản trị | Hệ thống phải kiểm soát quyền truy cập đối với các chức năng quản trị theo quyền của từng nhân viên. |
| Bảo vệ dữ liệu | Hệ thống phải bảo vệ thông tin cá nhân, thông tin phương tiện, dữ liệu vị trí và dữ liệu giao dịch khỏi truy cập trái phép. |
| Lưu vết hoạt động | Hệ thống phải ghi nhận các thao tác quan trọng để phục vụ kiểm tra khi có sự cố. |
| Đảm bảo tính ổn định | Hệ thống phải hạn chế việc lỗi tại một thành phần như thanh toán hoặc thông báo làm dừng toàn bộ quy trình đặt xe. |
| Hỗ trợ khả năng mở rộng | Hệ thống phải có khả năng mở rộng khi số lượng khách hàng và tài xế tăng và hỗ trợ bổ sung các chức năng mới trong tương lai. |

# Bước 6: Yêu cầu chức năng

# Bước 6. Yêu cầu chức năng

## 1. Khách hàng

- Đăng ký tài khoản
- Đăng nhập
- Đăng xuất
- Quên mật khẩu
- Quản lý thông tin cá nhân
- Đặt xe
- Theo dõi chuyến đi
- Hủy chuyến
- Thanh toán
- Xem lịch sử chuyến đi
- Xem chi tiết chuyến đi
- Đánh giá tài xế

## 2. Tài xế

- Đăng nhập
- Đăng xuất
- Quên mật khẩu
- Quản lý thông tin cá nhân
- Quản lý phương tiện
- Quản lý trạng thái hoạt động
- Xem chuyến được phân công
- Cập nhật trạng thái chuyến
- Xem lịch sử chuyến
- Xem chi tiết chuyến đi

## 3. Nhân viên vận hành

- Đăng nhập
- Đăng xuất
- Quên mật khẩu
- Quản lý thông tin cá nhân
- Quản lý khách hàng
- Xem thông tin khách hàng
- Quản lý tài xế
- Xem thông tin tài xế
- Quản lý phương tiện
- Quản lý chuyến đi
- Xem chi tiết chuyến đi
- Theo dõi hoạt động tài xế
- Quản lý giao dịch
- Xem chi tiết giao dịch
- Xử lý chuyến có vấn đề
- Quản lý quyền truy cập

## 4. Ban giám đốc

- Đăng nhập
- Đăng xuất
- Quên mật khẩu
- Quản lý thông tin cá nhân
- Theo dõi hoạt động kinh doanh
- Xem báo cáo hoạt động
- Theo dõi doanh thu
- Theo dõi số lượng chuyến
- Theo dõi tỷ lệ hoàn thành chuyến
- Theo dõi tỷ lệ hủy chuyến
- Theo dõi hiệu quả hoạt động của tài xế

## Bước 7. Use Case Diagram


# Bước 8: Đặc tả Use Case
## 1. Khách hàng

### UC01 - Đăng ký tài khoản

| Thành phần | Nội dung |
|---|---|
| **Use Case** | Đăng ký tài khoản |
| **Actor** | Khách hàng |
| **Mục đích** | Cho phép khách hàng tạo tài khoản để sử dụng các chức năng của CAB System |
| **Điều kiện trước** | Khách hàng chưa có tài khoản |
| **Điều kiện sau** | Tài khoản khách hàng được tạo thành công |
| **Luồng chính** | 1. Khách hàng chọn **Đăng ký tài khoản**.<br>2. Hệ thống hiển thị biểu mẫu đăng ký.<br>3. Khách hàng nhập các thông tin cần thiết.<br>4. Hệ thống kiểm tra tính hợp lệ của thông tin.<br>5. Hệ thống kiểm tra tài khoản đã tồn tại hay chưa.<br>6. Hệ thống tạo tài khoản khách hàng.<br>7. Hệ thống thông báo đăng ký thành công. |
| **Luồng thay thế / Ngoại lệ** | - Thông tin không hợp lệ → Hệ thống thông báo lỗi và yêu cầu nhập lại.<br>- Tài khoản đã tồn tại → Hệ thống thông báo và yêu cầu sử dụng thông tin khác. |

### UC02 - Đăng nhập

| Thành phần | Nội dung |
|---|---|
| **Use Case** | Đăng nhập |
| **Actor** | Khách hàng |
| **Mục đích** | Xác thực tài khoản để khách hàng sử dụng hệ thống |
| **Điều kiện trước** | Khách hàng đã có tài khoản và tài khoản đang hoạt động |
| **Điều kiện sau** | Khách hàng đăng nhập thành công |
| **Luồng chính** | 1. Khách hàng chọn **Đăng nhập**.<br>2. Hệ thống hiển thị biểu mẫu đăng nhập.<br>3. Khách hàng nhập thông tin đăng nhập.<br>4. Hệ thống kiểm tra thông tin.<br>5. Hệ thống xác thực tài khoản.<br>6. Hệ thống tạo phiên đăng nhập.<br>7. Hệ thống chuyển khách hàng đến giao diện chính. |
| **Luồng thay thế / Ngoại lệ** | - Thông tin đăng nhập không chính xác → Hệ thống thông báo lỗi.<br>- Tài khoản bị khóa hoặc không hoạt động → Hệ thống từ chối đăng nhập. |

### UC03 - Đăng xuất

| Thành phần | Nội dung |
|---|---|
| **Use Case** | Đăng xuất |
| **Actor** | Khách hàng |
| **Mục đích** | Kết thúc phiên sử dụng hệ thống |
| **Điều kiện trước** | Khách hàng đang đăng nhập |
| **Điều kiện sau** | Phiên đăng nhập được kết thúc |
| **Luồng chính** | 1. Khách hàng chọn **Đăng xuất**.<br>2. Hệ thống kết thúc phiên đăng nhập.<br>3. Hệ thống chuyển khách hàng về màn hình đăng nhập. |
| **Luồng thay thế / Ngoại lệ** | Không có. |

### UC04 - Quên mật khẩu

| Thành phần | Nội dung |
|---|---|
| **Use Case** | Quên mật khẩu |
| **Actor** | Khách hàng |
| **Mục đích** | Cho phép khách hàng khôi phục quyền truy cập khi quên mật khẩu |
| **Điều kiện trước** | Khách hàng đã có tài khoản |
| **Điều kiện sau** | Mật khẩu mới được cập nhật thành công |
| **Luồng chính** | 1. Khách hàng chọn **Quên mật khẩu**.<br>2. Hệ thống yêu cầu thông tin xác thực.<br>3. Khách hàng cung cấp thông tin tài khoản.<br>4. Hệ thống kiểm tra thông tin.<br>5. Hệ thống thực hiện xác thực.<br>6. Khách hàng nhập mật khẩu mới.<br>7. Hệ thống kiểm tra mật khẩu mới.<br>8. Hệ thống cập nhật mật khẩu.<br>9. Hệ thống thông báo khôi phục mật khẩu thành công. |
| **Luồng thay thế / Ngoại lệ** | - Không tìm thấy tài khoản → Hệ thống thông báo lỗi.<br>- Thông tin xác thực không hợp lệ → Hệ thống từ chối yêu cầu.<br>- Mật khẩu mới không hợp lệ → Hệ thống yêu cầu nhập lại. |

### UC05 - Quản lý thông tin cá nhân

| Thành phần | Nội dung |
|---|---|
| **Use Case** | Quản lý thông tin cá nhân |
| **Actor** | Khách hàng |
| **Mục đích** | Cho phép khách hàng xem và cập nhật thông tin cá nhân |
| **Điều kiện trước** | Khách hàng đã đăng nhập |
| **Điều kiện sau** | Thông tin cá nhân được cập nhật thành công |
| **Luồng chính** | 1. Khách hàng chọn **Thông tin cá nhân**.<br>2. Hệ thống hiển thị thông tin hiện tại.<br>3. Khách hàng chỉnh sửa thông tin cần thay đổi.<br>4. Hệ thống kiểm tra dữ liệu.<br>5. Khách hàng xác nhận cập nhật.<br>6. Hệ thống lưu thông tin mới.<br>7. Hệ thống thông báo cập nhật thành công. |
| **Luồng thay thế / Ngoại lệ** | - Thông tin không hợp lệ → Hệ thống thông báo lỗi và yêu cầu nhập lại.<br>- Khách hàng hủy cập nhật → Thông tin cũ được giữ nguyên. |

### UC06 - Đặt xe

| Thành phần | Nội dung |
|---|---|
| **Use Case** | Đặt xe |
| **Actor** | Khách hàng |
| **Mục đích** | Cho phép khách hàng tạo yêu cầu đặt xe |
| **Điều kiện trước** | Khách hàng đã đăng nhập |
| **Điều kiện sau** | Yêu cầu đặt xe được tạo và chuyển sang quá trình tìm tài xế |
| **Luồng chính** | 1. Khách hàng chọn **Đặt xe**.<br>2. Hệ thống yêu cầu nhập điểm đón và điểm đến.<br>3. Khách hàng nhập thông tin chuyến đi.<br>4. Khách hàng chọn loại phương tiện.<br>5. Hệ thống kiểm tra thông tin đặt xe.<br>6. Hệ thống tiếp nhận yêu cầu đặt xe.<br>7. Hệ thống tìm tài xế phù hợp.<br>8. Hệ thống phân công tài xế.<br>9. Hệ thống thông báo kết quả cho khách hàng. |
| **Luồng thay thế / Ngoại lệ** | - Thông tin đặt xe không hợp lệ → Hệ thống yêu cầu nhập lại.<br>- Không tìm được tài xế phù hợp → Hệ thống thông báo chưa tìm được tài xế.<br>- Khách hàng hủy thao tác → Yêu cầu đặt xe không được tạo. |

### UC07 - Theo dõi chuyến đi

| Thành phần | Nội dung |
|---|---|
| **Use Case** | Theo dõi chuyến đi |
| **Actor** | Khách hàng |
| **Mục đích** | Cho phép khách hàng theo dõi trạng thái và tiến trình của chuyến đi |
| **Điều kiện trước** | Khách hàng có chuyến đang được thực hiện |
| **Điều kiện sau** | Khách hàng xem được trạng thái hiện tại của chuyến |
| **Luồng chính** | 1. Khách hàng chọn chuyến đang thực hiện.<br>2. Hệ thống hiển thị thông tin chuyến.<br>3. Hệ thống cập nhật trạng thái chuyến.<br>4. Khách hàng theo dõi trạng thái hiện tại.<br>5. Hệ thống tiếp tục cập nhật cho đến khi chuyến kết thúc. |
| **Luồng thay thế / Ngoại lệ** | - Chuyến đã kết thúc → Hệ thống hiển thị trạng thái cuối cùng.<br>- Không thể cập nhật trạng thái → Hệ thống hiển thị trạng thái gần nhất đã ghi nhận. |

### UC08 - Hủy chuyến

| Thành phần | Nội dung |
|---|---|
| **Use Case** | Hủy chuyến |
| **Actor** | Khách hàng |
| **Mục đích** | Cho phép khách hàng hủy chuyến khi chuyến đang ở trạng thái cho phép hủy |
| **Điều kiện trước** | Khách hàng có chuyến đang được xử lý hoặc thực hiện và chuyến cho phép hủy |
| **Điều kiện sau** | Chuyến được chuyển sang trạng thái đã hủy |
| **Luồng chính** | 1. Khách hàng chọn chuyến cần hủy.<br>2. Hệ thống kiểm tra trạng thái chuyến.<br>3. Hệ thống hiển thị thông tin và điều kiện hủy chuyến.<br>4. Khách hàng xác nhận hủy chuyến.<br>5. Hệ thống cập nhật trạng thái chuyến.<br>6. Hệ thống ghi nhận thông tin hủy chuyến.<br>7. Hệ thống thông báo kết quả cho khách hàng và các bên liên quan. |
| **Luồng thay thế / Ngoại lệ** | - Chuyến không được phép hủy → Hệ thống thông báo và từ chối thao tác.<br>- Khách hàng không xác nhận → Chuyến được giữ nguyên trạng thái. |

### UC09 - Thanh toán

| Thành phần | Nội dung |
|---|---|
| **Use Case** | Thanh toán |
| **Actor** | Khách hàng |
| **Mục đích** | Cho phép khách hàng thanh toán chi phí của chuyến đi |
| **Điều kiện trước** | Chuyến đi đã phát sinh cước cần thanh toán |
| **Điều kiện sau** | Giao dịch thanh toán được ghi nhận với trạng thái tương ứng |
| **Luồng chính** | 1. Khách hàng chọn **Thanh toán**.<br>2. Hệ thống tính cước chuyến đi.<br>3. Hệ thống hiển thị số tiền cần thanh toán.<br>4. Khách hàng chọn phương thức thanh toán.<br>5. Khách hàng xác nhận thanh toán.<br>6. Hệ thống gửi yêu cầu xử lý giao dịch.<br>7. Hệ thống nhận kết quả giao dịch.<br>8. Hệ thống cập nhật trạng thái thanh toán.<br>9. Hệ thống thông báo kết quả cho khách hàng. |
| **Luồng thay thế / Ngoại lệ** | - Giao dịch thất bại → Hệ thống thông báo thanh toán không thành công.<br>- Giao dịch đang chờ xử lý → Hệ thống ghi nhận trạng thái chờ.<br>- Khách hàng hủy thanh toán → Giao dịch không được hoàn tất. |

### UC10 - Xem lịch sử chuyến đi

| Thành phần | Nội dung |
|---|---|
| **Use Case** | Xem lịch sử chuyến đi |
| **Actor** | Khách hàng |
| **Mục đích** | Cho phép khách hàng xem lại các chuyến đi đã thực hiện |
| **Điều kiện trước** | Khách hàng đã đăng nhập |
| **Điều kiện sau** | Danh sách lịch sử chuyến được hiển thị |
| **Luồng chính** | 1. Khách hàng chọn **Lịch sử chuyến đi**.<br>2. Hệ thống truy xuất lịch sử chuyến của khách hàng.<br>3. Hệ thống hiển thị danh sách chuyến.<br>4. Khách hàng lựa chọn chuyến cần xem. |
| **Luồng thay thế / Ngoại lệ** | - Không có lịch sử chuyến → Hệ thống thông báo chưa có dữ liệu. |

### UC11 - Xem chi tiết chuyến đi

| Thành phần | Nội dung |
|---|---|
| **Use Case** | Xem chi tiết chuyến đi |
| **Actor** | Khách hàng |
| **Mục đích** | Cho phép khách hàng xem đầy đủ thông tin của một chuyến đi |
| **Điều kiện trước** | Khách hàng đã đăng nhập và chuyến thuộc tài khoản khách hàng |
| **Điều kiện sau** | Thông tin chi tiết chuyến được hiển thị |
| **Luồng chính** | 1. Khách hàng chọn một chuyến.<br>2. Hệ thống kiểm tra quyền truy cập.<br>3. Hệ thống truy xuất thông tin chuyến.<br>4. Hệ thống hiển thị thông tin chi tiết chuyến, tài xế, phương tiện, cước và trạng thái. |
| **Luồng thay thế / Ngoại lệ** | - Không tìm thấy chuyến → Hệ thống thông báo lỗi.<br>- Chuyến không thuộc khách hàng → Hệ thống từ chối truy cập. |

### UC12 - Đánh giá tài xế

| Thành phần | Nội dung |
|---|---|
| **Use Case** | Đánh giá tài xế |
| **Actor** | Khách hàng |
| **Mục đích** | Cho phép khách hàng đánh giá chất lượng phục vụ của tài xế sau chuyến đi |
| **Điều kiện trước** | Chuyến đã hoàn thành và khách hàng chưa đánh giá chuyến |
| **Điều kiện sau** | Đánh giá được lưu thành công |
| **Luồng chính** | 1. Khách hàng chọn chuyến đã hoàn thành.<br>2. Khách hàng chọn **Đánh giá tài xế**.<br>3. Hệ thống hiển thị biểu mẫu đánh giá.<br>4. Khách hàng nhập mức đánh giá và nhận xét nếu có.<br>5. Khách hàng xác nhận gửi đánh giá.<br>6. Hệ thống kiểm tra thông tin đánh giá.<br>7. Hệ thống lưu đánh giá.<br>8. Hệ thống thông báo gửi đánh giá thành công. |
| **Luồng thay thế / Ngoại lệ** | - Chuyến đã được đánh giá → Hệ thống không cho phép đánh giá lại.<br>- Thông tin đánh giá không hợp lệ → Hệ thống yêu cầu nhập lại. |

## 2. Tài xế

> Các chức năng **Đăng nhập, Đăng xuất, Quên mật khẩu và Quản lý thông tin cá nhân** đã được đặc tả ở phần Khách hàng và được dùng chung, nên không đặc tả lại.

### UC13 - Quản lý phương tiện

| Thành phần | Nội dung |
|---|---|
| **Use Case** | Quản lý phương tiện |
| **Actor** | Tài xế |
| **Mục đích** | Cho phép tài xế xem và cập nhật thông tin phương tiện được sử dụng |
| **Điều kiện trước** | Tài xế đã đăng nhập |
| **Điều kiện sau** | Thông tin phương tiện được cập nhật thành công |
| **Luồng chính** | 1. Tài xế chọn **Quản lý phương tiện**.<br>2. Hệ thống hiển thị thông tin phương tiện hiện tại.<br>3. Tài xế xem hoặc chỉnh sửa thông tin phương tiện.<br>4. Hệ thống kiểm tra dữ liệu.<br>5. Tài xế xác nhận cập nhật.<br>6. Hệ thống lưu thông tin mới.<br>7. Hệ thống thông báo cập nhật thành công. |
| **Luồng thay thế / Ngoại lệ** | - Thông tin không hợp lệ → Hệ thống thông báo lỗi và yêu cầu nhập lại.<br>- Tài xế hủy thao tác → Thông tin cũ được giữ nguyên. |

### UC14 - Quản lý trạng thái hoạt động

| Thành phần | Nội dung |
|---|---|
| **Use Case** | Quản lý trạng thái hoạt động |
| **Actor** | Tài xế |
| **Mục đích** | Cho phép tài xế cập nhật trạng thái sẵn sàng nhận chuyến |
| **Điều kiện trước** | Tài xế đã đăng nhập và tài khoản đang hoạt động |
| **Điều kiện sau** | Trạng thái hoạt động của tài xế được cập nhật |
| **Luồng chính** | 1. Tài xế truy cập chức năng **Trạng thái hoạt động**.<br>2. Hệ thống hiển thị trạng thái hiện tại.<br>3. Tài xế lựa chọn trạng thái phù hợp.<br>4. Hệ thống kiểm tra điều kiện thay đổi trạng thái.<br>5. Hệ thống cập nhật trạng thái mới.<br>6. Hệ thống thông báo trạng thái đã được cập nhật. |
| **Luồng thay thế / Ngoại lệ** | - Tài xế đang thực hiện chuyến → Hệ thống không cho phép chuyển sang trạng thái không hoạt động.<br>- Trạng thái không hợp lệ → Hệ thống từ chối cập nhật. |

### UC15 - Xem chuyến được phân công

| Thành phần | Nội dung |
|---|---|
| **Use Case** | Xem chuyến được phân công |
| **Actor** | Tài xế |
| **Mục đích** | Cho phép tài xế xem các chuyến được hệ thống phân công |
| **Điều kiện trước** | Tài xế đã đăng nhập |
| **Điều kiện sau** | Danh sách chuyến được phân công được hiển thị |
| **Luồng chính** | 1. Tài xế truy cập **Chuyến được phân công**.<br>2. Hệ thống truy xuất các chuyến được phân công cho tài xế.<br>3. Hệ thống hiển thị danh sách chuyến.<br>4. Tài xế lựa chọn chuyến cần xem. |
| **Luồng thay thế / Ngoại lệ** | - Không có chuyến được phân công → Hệ thống thông báo chưa có chuyến. |

### UC16 - Cập nhật trạng thái chuyến

| Thành phần | Nội dung |
|---|---|
| **Use Case** | Cập nhật trạng thái chuyến |
| **Actor** | Tài xế |
| **Mục đích** | Cho phép tài xế cập nhật tiến trình thực hiện chuyến |
| **Điều kiện trước** | Tài xế đã đăng nhập và có chuyến được phân công |
| **Điều kiện sau** | Trạng thái chuyến được cập nhật |
| **Luồng chính** | 1. Tài xế chọn chuyến được phân công.<br>2. Hệ thống hiển thị trạng thái hiện tại.<br>3. Tài xế chọn trạng thái mới.<br>4. Hệ thống kiểm tra trạng thái có hợp lệ hay không.<br>5. Hệ thống cập nhật trạng thái chuyến.<br>6. Hệ thống thông báo cập nhật thành công.<br>7. Hệ thống cung cấp trạng thái mới cho các bên liên quan. |
| **Luồng thay thế / Ngoại lệ** | - Trạng thái không hợp lệ theo tiến trình chuyến → Hệ thống từ chối cập nhật.<br>- Chuyến đã kết thúc hoặc bị hủy → Tài xế không thể tiếp tục cập nhật trạng thái. |

### UC17 - Xem lịch sử chuyến

| Thành phần | Nội dung |
|---|---|
| **Use Case** | Xem lịch sử chuyến |
| **Actor** | Tài xế |
| **Mục đích** | Cho phép tài xế xem các chuyến đã thực hiện |
| **Điều kiện trước** | Tài xế đã đăng nhập |
| **Điều kiện sau** | Danh sách lịch sử chuyến của tài xế được hiển thị |
| **Luồng chính** | 1. Tài xế chọn **Lịch sử chuyến**.<br>2. Hệ thống truy xuất các chuyến đã thực hiện của tài xế.<br>3. Hệ thống hiển thị danh sách chuyến.<br>4. Tài xế lựa chọn chuyến cần xem. |
| **Luồng thay thế / Ngoại lệ** | - Không có lịch sử chuyến → Hệ thống thông báo chưa có dữ liệu. |

### UC18 - Xem chi tiết chuyến đi

| Thành phần | Nội dung |
|---|---|
| **Use Case** | Xem chi tiết chuyến đi |
| **Actor** | Tài xế |
| **Mục đích** | Cho phép tài xế xem đầy đủ thông tin của chuyến được phân công hoặc đã thực hiện |
| **Điều kiện trước** | Tài xế đã đăng nhập và chuyến thuộc phạm vi được phép truy cập |
| **Điều kiện sau** | Thông tin chi tiết chuyến được hiển thị |
| **Luồng chính** | 1. Tài xế chọn một chuyến.<br>2. Hệ thống kiểm tra quyền truy cập của tài xế.<br>3. Hệ thống truy xuất thông tin chuyến.<br>4. Hệ thống hiển thị thông tin khách hàng, điểm đón, điểm đến, phương tiện, trạng thái và thông tin liên quan. |
| **Luồng thay thế / Ngoại lệ** | - Không tìm thấy chuyến → Hệ thống thông báo lỗi.<br>- Tài xế không được phép truy cập chuyến → Hệ thống từ chối truy cập. |

## 3. Nhân viên vận hành

> Các chức năng **Đăng nhập, Đăng xuất, Quên mật khẩu và Quản lý thông tin cá nhân** đã được đặc tả trước đó và được dùng chung, nên không đặc tả lại.

### UC19 - Quản lý khách hàng

| Thành phần | Nội dung |
|---|---|
| **Use Case** | Quản lý khách hàng |
| **Actor** | Nhân viên vận hành |
| **Mục đích** | Cho phép nhân viên vận hành quản lý thông tin và trạng thái tài khoản khách hàng |
| **Điều kiện trước** | Nhân viên vận hành đã đăng nhập và có quyền quản lý khách hàng |
| **Điều kiện sau** | Thông tin hoặc trạng thái khách hàng được cập nhật thành công |
| **Luồng chính** | 1. Nhân viên chọn **Quản lý khách hàng**.<br>2. Hệ thống hiển thị danh sách khách hàng.<br>3. Nhân viên tìm kiếm hoặc chọn khách hàng cần quản lý.<br>4. Hệ thống hiển thị thông tin khách hàng.<br>5. Nhân viên thực hiện thao tác quản lý phù hợp.<br>6. Hệ thống kiểm tra dữ liệu và quyền thực hiện.<br>7. Hệ thống lưu thay đổi.<br>8. Hệ thống thông báo kết quả. |
| **Luồng thay thế / Ngoại lệ** | - Không tìm thấy khách hàng → Hệ thống thông báo không có dữ liệu phù hợp.<br>- Dữ liệu không hợp lệ → Hệ thống yêu cầu kiểm tra lại.<br>- Nhân viên không đủ quyền → Hệ thống từ chối thao tác. |

### UC20 - Xem thông tin khách hàng

| Thành phần | Nội dung |
|---|---|
| **Use Case** | Xem thông tin khách hàng |
| **Actor** | Nhân viên vận hành |
| **Mục đích** | Cho phép nhân viên xem thông tin chi tiết của khách hàng |
| **Điều kiện trước** | Nhân viên đã đăng nhập và có quyền truy cập |
| **Điều kiện sau** | Thông tin khách hàng được hiển thị |
| **Luồng chính** | 1. Nhân viên tìm kiếm khách hàng.<br>2. Hệ thống hiển thị danh sách kết quả.<br>3. Nhân viên chọn khách hàng.<br>4. Hệ thống kiểm tra quyền truy cập.<br>5. Hệ thống hiển thị thông tin chi tiết khách hàng. |
| **Luồng thay thế / Ngoại lệ** | - Không tìm thấy khách hàng → Hệ thống thông báo không có dữ liệu.<br>- Nhân viên không có quyền → Hệ thống từ chối truy cập. |

### UC21 - Quản lý tài xế

| Thành phần | Nội dung |
|---|---|
| **Use Case** | Quản lý tài xế |
| **Actor** | Nhân viên vận hành |
| **Mục đích** | Cho phép nhân viên quản lý thông tin và trạng thái tài xế |
| **Điều kiện trước** | Nhân viên đã đăng nhập và có quyền quản lý tài xế |
| **Điều kiện sau** | Thông tin hoặc trạng thái tài xế được cập nhật thành công |
| **Luồng chính** | 1. Nhân viên chọn **Quản lý tài xế**.<br>2. Hệ thống hiển thị danh sách tài xế.<br>3. Nhân viên tìm kiếm hoặc chọn tài xế.<br>4. Hệ thống hiển thị thông tin tài xế.<br>5. Nhân viên thực hiện thao tác quản lý.<br>6. Hệ thống kiểm tra dữ liệu và quyền.<br>7. Hệ thống lưu thay đổi.<br>8. Hệ thống thông báo kết quả. |
| **Luồng thay thế / Ngoại lệ** | - Không tìm thấy tài xế → Hệ thống thông báo không có dữ liệu.<br>- Dữ liệu không hợp lệ → Hệ thống yêu cầu nhập lại.<br>- Không đủ quyền → Hệ thống từ chối thao tác. |

### UC22 - Xem thông tin tài xế

| Thành phần | Nội dung |
|---|---|
| **Use Case** | Xem thông tin tài xế |
| **Actor** | Nhân viên vận hành |
| **Mục đích** | Cho phép nhân viên xem thông tin chi tiết của tài xế |
| **Điều kiện trước** | Nhân viên đã đăng nhập và có quyền truy cập |
| **Điều kiện sau** | Thông tin tài xế được hiển thị |
| **Luồng chính** | 1. Nhân viên tìm kiếm tài xế.<br>2. Hệ thống hiển thị danh sách kết quả.<br>3. Nhân viên chọn tài xế.<br>4. Hệ thống kiểm tra quyền truy cập.<br>5. Hệ thống hiển thị thông tin tài xế và thông tin phương tiện liên quan. |
| **Luồng thay thế / Ngoại lệ** | - Không tìm thấy tài xế → Hệ thống thông báo không có dữ liệu.<br>- Không có quyền truy cập → Hệ thống từ chối truy cập. |

### UC23 - Quản lý phương tiện

| Thành phần | Nội dung |
|---|---|
| **Use Case** | Quản lý phương tiện |
| **Actor** | Nhân viên vận hành |
| **Mục đích** | Cho phép nhân viên quản lý thông tin và trạng thái phương tiện |
| **Điều kiện trước** | Nhân viên đã đăng nhập và có quyền quản lý phương tiện |
| **Điều kiện sau** | Thông tin hoặc trạng thái phương tiện được cập nhật |
| **Luồng chính** | 1. Nhân viên chọn **Quản lý phương tiện**.<br>2. Hệ thống hiển thị danh sách phương tiện.<br>3. Nhân viên tìm kiếm hoặc chọn phương tiện.<br>4. Hệ thống hiển thị thông tin phương tiện.<br>5. Nhân viên thêm, cập nhật hoặc thay đổi trạng thái phương tiện.<br>6. Hệ thống kiểm tra dữ liệu.<br>7. Hệ thống lưu thay đổi.<br>8. Hệ thống thông báo kết quả. |
| **Luồng thay thế / Ngoại lệ** | - Thông tin phương tiện không hợp lệ → Hệ thống thông báo lỗi.<br>- Phương tiện không tồn tại → Hệ thống thông báo lỗi.<br>- Nhân viên không đủ quyền → Hệ thống từ chối thao tác. |

### UC24 - Quản lý chuyến đi

| Thành phần | Nội dung |
|---|---|
| **Use Case** | Quản lý chuyến đi |
| **Actor** | Nhân viên vận hành |
| **Mục đích** | Cho phép nhân viên theo dõi và quản lý các chuyến đi trong hệ thống |
| **Điều kiện trước** | Nhân viên đã đăng nhập và có quyền quản lý chuyến |
| **Điều kiện sau** | Thông tin hoặc trạng thái chuyến được cập nhật theo thao tác |
| **Luồng chính** | 1. Nhân viên chọn **Quản lý chuyến đi**.<br>2. Hệ thống hiển thị danh sách chuyến.<br>3. Nhân viên tìm kiếm hoặc lọc chuyến.<br>4. Nhân viên chọn chuyến cần xử lý.<br>5. Hệ thống hiển thị thông tin chuyến.<br>6. Nhân viên thực hiện thao tác quản lý phù hợp.<br>7. Hệ thống kiểm tra quyền và dữ liệu.<br>8. Hệ thống cập nhật thông tin chuyến.<br>9. Hệ thống thông báo kết quả. |
| **Luồng thay thế / Ngoại lệ** | - Không tìm thấy chuyến → Hệ thống thông báo không có dữ liệu.<br>- Thao tác không hợp lệ với trạng thái hiện tại → Hệ thống từ chối thao tác.<br>- Không đủ quyền → Hệ thống từ chối thao tác. |

### UC25 - Xem chi tiết chuyến đi

| Thành phần | Nội dung |
|---|---|
| **Use Case** | Xem chi tiết chuyến đi |
| **Actor** | Nhân viên vận hành |
| **Mục đích** | Cho phép nhân viên xem đầy đủ thông tin của một chuyến đi |
| **Điều kiện trước** | Nhân viên đã đăng nhập và có quyền truy cập |
| **Điều kiện sau** | Thông tin chi tiết chuyến được hiển thị |
| **Luồng chính** | 1. Nhân viên chọn một chuyến.<br>2. Hệ thống kiểm tra quyền truy cập.<br>3. Hệ thống truy xuất dữ liệu chuyến.<br>4. Hệ thống hiển thị thông tin khách hàng, tài xế, phương tiện, điểm đón, điểm đến, trạng thái và giao dịch liên quan. |
| **Luồng thay thế / Ngoại lệ** | - Không tìm thấy chuyến → Hệ thống thông báo lỗi.<br>- Không có quyền truy cập → Hệ thống từ chối truy cập. |

### UC26 - Theo dõi hoạt động tài xế

| Thành phần | Nội dung |
|---|---|
| **Use Case** | Theo dõi hoạt động tài xế |
| **Actor** | Nhân viên vận hành |
| **Mục đích** | Cho phép nhân viên theo dõi trạng thái và hoạt động của tài xế |
| **Điều kiện trước** | Nhân viên đã đăng nhập và có quyền theo dõi tài xế |
| **Điều kiện sau** | Thông tin hoạt động của tài xế được hiển thị |
| **Luồng chính** | 1. Nhân viên truy cập **Theo dõi hoạt động tài xế**.<br>2. Hệ thống lấy dữ liệu hoạt động của tài xế.<br>3. Hệ thống hiển thị danh sách tài xế và trạng thái hiện tại.<br>4. Nhân viên tìm kiếm hoặc lọc tài xế.<br>5. Nhân viên chọn tài xế cần theo dõi.<br>6. Hệ thống hiển thị thông tin hoạt động chi tiết. |
| **Luồng thay thế / Ngoại lệ** | - Không có dữ liệu hoạt động → Hệ thống thông báo chưa có dữ liệu.<br>- Dữ liệu chưa được cập nhật → Hệ thống hiển thị thời điểm cập nhật gần nhất. |

### UC27 - Quản lý giao dịch

| Thành phần | Nội dung |
|---|---|
| **Use Case** | Quản lý giao dịch |
| **Actor** | Nhân viên vận hành |
| **Mục đích** | Cho phép nhân viên theo dõi và quản lý các giao dịch thanh toán |
| **Điều kiện trước** | Nhân viên đã đăng nhập và có quyền quản lý giao dịch |
| **Điều kiện sau** | Thông tin giao dịch được cập nhật hoặc xử lý theo yêu cầu |
| **Luồng chính** | 1. Nhân viên chọn **Quản lý giao dịch**.<br>2. Hệ thống hiển thị danh sách giao dịch.<br>3. Nhân viên tìm kiếm hoặc lọc giao dịch.<br>4. Nhân viên chọn giao dịch cần xử lý.<br>5. Hệ thống hiển thị thông tin giao dịch.<br>6. Nhân viên thực hiện thao tác phù hợp.<br>7. Hệ thống kiểm tra quyền và dữ liệu.<br>8. Hệ thống cập nhật giao dịch.<br>9. Hệ thống thông báo kết quả. |
| **Luồng thay thế / Ngoại lệ** | - Không tìm thấy giao dịch → Hệ thống thông báo không có dữ liệu.<br>- Giao dịch không thể xử lý → Hệ thống thông báo lý do.<br>- Không đủ quyền → Hệ thống từ chối thao tác. |

### UC28 - Xem chi tiết giao dịch

| Thành phần | Nội dung |
|---|---|
| **Use Case** | Xem chi tiết giao dịch |
| **Actor** | Nhân viên vận hành |
| **Mục đích** | Cho phép nhân viên xem đầy đủ thông tin của một giao dịch |
| **Điều kiện trước** | Nhân viên đã đăng nhập và có quyền truy cập |
| **Điều kiện sau** | Thông tin chi tiết giao dịch được hiển thị |
| **Luồng chính** | 1. Nhân viên chọn một giao dịch.<br>2. Hệ thống kiểm tra quyền truy cập.<br>3. Hệ thống truy xuất thông tin giao dịch.<br>4. Hệ thống hiển thị mã giao dịch, chuyến đi liên quan, khách hàng, số tiền, phương thức và trạng thái giao dịch. |
| **Luồng thay thế / Ngoại lệ** | - Không tìm thấy giao dịch → Hệ thống thông báo lỗi.<br>- Không có quyền truy cập → Hệ thống từ chối truy cập. |

### UC29 - Xử lý chuyến có vấn đề

| Thành phần | Nội dung |
|---|---|
| **Use Case** | Xử lý chuyến có vấn đề |
| **Actor** | Nhân viên vận hành |
| **Mục đích** | Cho phép nhân viên xử lý các chuyến phát sinh sự cố hoặc bất thường |
| **Điều kiện trước** | Nhân viên đã đăng nhập và có quyền xử lý sự cố |
| **Điều kiện sau** | Vấn đề của chuyến được ghi nhận và xử lý hoặc chuyển sang trạng thái cần tiếp tục xử lý |
| **Luồng chính** | 1. Hệ thống ghi nhận hoặc nhân viên tiếp nhận chuyến có vấn đề.<br>2. Nhân viên xem thông tin chi tiết chuyến.<br>3. Nhân viên xác định vấn đề phát sinh.<br>4. Nhân viên thực hiện phương án xử lý phù hợp.<br>5. Hệ thống ghi nhận nội dung xử lý.<br>6. Hệ thống cập nhật trạng thái xử lý.<br>7. Hệ thống thông báo kết quả cho các bên liên quan nếu cần. |
| **Luồng thay thế / Ngoại lệ** | - Không đủ thông tin để xử lý → Hệ thống yêu cầu bổ sung thông tin.<br>- Vấn đề vượt quá quyền xử lý → Nhân viên chuyển vấn đề đến cấp có thẩm quyền.<br>- Không thể xử lý ngay → Hệ thống ghi nhận trạng thái đang xử lý. |

### UC30 - Quản lý quyền truy cập

| Thành phần | Nội dung |
|---|---|
| **Use Case** | Quản lý quyền truy cập |
| **Actor** | Nhân viên vận hành |
| **Mục đích** | Cho phép nhân viên có thẩm quyền quản lý quyền truy cập của người dùng trong hệ thống |
| **Điều kiện trước** | Nhân viên đã đăng nhập và được cấp quyền quản lý quyền truy cập |
| **Điều kiện sau** | Quyền truy cập của người dùng được cập nhật |
| **Luồng chính** | 1. Nhân viên truy cập **Quản lý quyền truy cập**.<br>2. Hệ thống hiển thị danh sách tài khoản và quyền hiện tại.<br>3. Nhân viên chọn tài khoản cần quản lý.<br>4. Hệ thống hiển thị các quyền hiện tại.<br>5. Nhân viên thêm, thay đổi hoặc thu hồi quyền.<br>6. Hệ thống kiểm tra quyền của nhân viên thực hiện thao tác.<br>7. Hệ thống lưu thay đổi.<br>8. Hệ thống ghi nhận lịch sử thay đổi quyền.<br>9. Hệ thống thông báo kết quả. |
| **Luồng thay thế / Ngoại lệ** | - Nhân viên không có quyền quản lý quyền truy cập → Hệ thống từ chối thao tác.<br>- Quyền được cấp không hợp lệ → Hệ thống thông báo lỗi.<br>- Tài khoản không tồn tại → Hệ thống thông báo lỗi. |

## 4. Ban giám đốc

> Các chức năng **Đăng nhập, Đăng xuất, Quên mật khẩu và Quản lý thông tin cá nhân** đã được đặc tả trước đó và được dùng chung, nên không đặc tả lại.

### UC31 - Theo dõi hoạt động kinh doanh

| Thành phần | Nội dung |
|---|---|
| **Use Case** | Theo dõi hoạt động kinh doanh |
| **Actor** | Ban giám đốc |
| **Mục đích** | Cho phép Ban giám đốc theo dõi tổng quan tình hình hoạt động kinh doanh của hệ thống |
| **Điều kiện trước** | Ban giám đốc đã đăng nhập và có quyền xem thông tin kinh doanh |
| **Điều kiện sau** | Các thông tin tổng quan về hoạt động kinh doanh được hiển thị |
| **Luồng chính** | 1. Ban giám đốc truy cập **Theo dõi hoạt động kinh doanh**.<br>2. Hệ thống tổng hợp dữ liệu hoạt động.<br>3. Hệ thống hiển thị các chỉ số kinh doanh tổng quan.<br>4. Ban giám đốc lựa chọn khoảng thời gian hoặc phạm vi cần theo dõi.<br>5. Hệ thống cập nhật dữ liệu theo điều kiện được chọn.<br>6. Ban giám đốc xem và phân tích tình hình hoạt động. |
| **Luồng thay thế / Ngoại lệ** | - Không có dữ liệu trong khoảng thời gian được chọn → Hệ thống thông báo chưa có dữ liệu.<br>- Dữ liệu chưa được cập nhật → Hệ thống hiển thị thời điểm cập nhật gần nhất. |

### UC32 - Xem báo cáo hoạt động

| Thành phần | Nội dung |
|---|---|
| **Use Case** | Xem báo cáo hoạt động |
| **Actor** | Ban giám đốc |
| **Mục đích** | Cho phép Ban giám đốc xem các báo cáo tổng hợp về hoạt động của hệ thống |
| **Điều kiện trước** | Ban giám đốc đã đăng nhập và có quyền xem báo cáo |
| **Điều kiện sau** | Báo cáo hoạt động được hiển thị |
| **Luồng chính** | 1. Ban giám đốc chọn **Xem báo cáo hoạt động**.<br>2. Hệ thống hiển thị các loại báo cáo.<br>3. Ban giám đốc lựa chọn loại báo cáo và khoảng thời gian.<br>4. Hệ thống tổng hợp dữ liệu.<br>5. Hệ thống tạo và hiển thị báo cáo.<br>6. Ban giám đốc xem thông tin báo cáo. |
| **Luồng thay thế / Ngoại lệ** | - Không có dữ liệu → Hệ thống thông báo không đủ dữ liệu để tạo báo cáo.<br>- Khoảng thời gian không hợp lệ → Hệ thống yêu cầu lựa chọn lại. |

### UC33 - Theo dõi doanh thu

| Thành phần | Nội dung |
|---|---|
| **Use Case** | Theo dõi doanh thu |
| **Actor** | Ban giám đốc |
| **Mục đích** | Cho phép Ban giám đốc theo dõi tình hình doanh thu từ hoạt động kinh doanh |
| **Điều kiện trước** | Ban giám đốc đã đăng nhập và có quyền xem dữ liệu doanh thu |
| **Điều kiện sau** | Thông tin doanh thu được hiển thị theo phạm vi lựa chọn |
| **Luồng chính** | 1. Ban giám đốc chọn **Theo dõi doanh thu**.<br>2. Hệ thống truy xuất dữ liệu giao dịch.<br>3. Hệ thống tổng hợp doanh thu.<br>4. Hệ thống hiển thị doanh thu theo khoảng thời gian được chọn.<br>5. Ban giám đốc xem và phân tích dữ liệu doanh thu. |
| **Luồng thay thế / Ngoại lệ** | - Không có dữ liệu doanh thu → Hệ thống thông báo chưa có dữ liệu.<br>- Dữ liệu giao dịch chưa hoàn tất → Hệ thống chỉ tính các giao dịch theo trạng thái được quy định. |

### UC34 - Theo dõi số lượng chuyến

| Thành phần | Nội dung |
|---|---|
| **Use Case** | Theo dõi số lượng chuyến |
| **Actor** | Ban giám đốc |
| **Mục đích** | Cho phép Ban giám đốc theo dõi số lượng chuyến phát sinh và tình trạng chuyến |
| **Điều kiện trước** | Ban giám đốc đã đăng nhập và có quyền xem dữ liệu chuyến |
| **Điều kiện sau** | Số lượng chuyến được tổng hợp và hiển thị |
| **Luồng chính** | 1. Ban giám đốc chọn **Theo dõi số lượng chuyến**.<br>2. Hệ thống truy xuất dữ liệu chuyến.<br>3. Hệ thống tổng hợp số lượng chuyến.<br>4. Hệ thống phân loại chuyến theo trạng thái.<br>5. Hệ thống hiển thị kết quả theo khoảng thời gian được chọn.<br>6. Ban giám đốc xem số liệu. |
| **Luồng thay thế / Ngoại lệ** | - Không có chuyến trong khoảng thời gian → Hệ thống thông báo chưa có dữ liệu.<br>- Dữ liệu chưa được cập nhật → Hệ thống hiển thị thời điểm cập nhật gần nhất. |

### UC35 - Theo dõi tỷ lệ hoàn thành chuyến

| Thành phần | Nội dung |
|---|---|
| **Use Case** | Theo dõi tỷ lệ hoàn thành chuyến |
| **Actor** | Ban giám đốc |
| **Mục đích** | Cho phép Ban giám đốc theo dõi tỷ lệ chuyến được hoàn thành |
| **Điều kiện trước** | Ban giám đốc đã đăng nhập và có quyền xem dữ liệu hoạt động |
| **Điều kiện sau** | Tỷ lệ hoàn thành chuyến được tính toán và hiển thị |
| **Luồng chính** | 1. Ban giám đốc chọn **Theo dõi tỷ lệ hoàn thành chuyến**.<br>2. Hệ thống truy xuất dữ liệu chuyến.<br>3. Hệ thống xác định số chuyến hoàn thành và tổng số chuyến theo phạm vi được chọn.<br>4. Hệ thống tính tỷ lệ hoàn thành.<br>5. Hệ thống hiển thị kết quả.<br>6. Ban giám đốc xem và phân tích tỷ lệ. |
| **Luồng thay thế / Ngoại lệ** | - Không có dữ liệu chuyến → Hệ thống thông báo không đủ dữ liệu để tính toán.<br>- Không có chuyến trong khoảng thời gian → Tỷ lệ không được tính và hệ thống thông báo tương ứng. |

### UC36 - Theo dõi tỷ lệ hủy chuyến

| Thành phần | Nội dung |
|---|---|
| **Use Case** | Theo dõi tỷ lệ hủy chuyến |
| **Actor** | Ban giám đốc |
| **Mục đích** | Cho phép Ban giám đốc theo dõi tình hình hủy chuyến |
| **Điều kiện trước** | Ban giám đốc đã đăng nhập và có quyền xem dữ liệu hoạt động |
| **Điều kiện sau** | Tỷ lệ hủy chuyến được tính toán và hiển thị |
| **Luồng chính** | 1. Ban giám đốc chọn **Theo dõi tỷ lệ hủy chuyến**.<br>2. Hệ thống truy xuất dữ liệu chuyến.<br>3. Hệ thống xác định số chuyến bị hủy và tổng số chuyến theo phạm vi được chọn.<br>4. Hệ thống tính tỷ lệ hủy chuyến.<br>5. Hệ thống hiển thị kết quả.<br>6. Ban giám đốc xem và phân tích tỷ lệ hủy. |
| **Luồng thay thế / Ngoại lệ** | - Không có dữ liệu chuyến → Hệ thống thông báo không đủ dữ liệu để tính toán.<br>- Không có chuyến trong khoảng thời gian → Tỷ lệ không được tính. |

### UC37 - Theo dõi hiệu quả hoạt động của tài xế

| Thành phần | Nội dung |
|---|---|
| **Use Case** | Theo dõi hiệu quả hoạt động của tài xế |
| **Actor** | Ban giám đốc |
| **Mục đích** | Cho phép Ban giám đốc đánh giá hiệu quả hoạt động của đội ngũ tài xế |
| **Điều kiện trước** | Ban giám đốc đã đăng nhập và có quyền xem dữ liệu tài xế |
| **Điều kiện sau** | Các chỉ số hiệu quả hoạt động của tài xế được hiển thị |
| **Luồng chính** | 1. Ban giám đốc chọn **Theo dõi hiệu quả hoạt động của tài xế**.<br>2. Hệ thống truy xuất dữ liệu hoạt động của tài xế.<br>3. Hệ thống tổng hợp các chỉ số liên quan đến hoạt động tài xế.<br>4. Hệ thống hiển thị kết quả theo từng tài xế hoặc toàn bộ đội ngũ.<br>5. Ban giám đốc lựa chọn khoảng thời gian hoặc tài xế cần theo dõi.<br>6. Hệ thống cập nhật dữ liệu theo điều kiện được chọn.<br>7. Ban giám đốc xem và đánh giá hiệu quả hoạt động. |
| **Luồng thay thế / Ngoại lệ** | - Không có dữ liệu tài xế → Hệ thống thông báo chưa có dữ liệu.<br>- Tài xế chưa có hoạt động trong khoảng thời gian → Hệ thống hiển thị trạng thái không có dữ liệu hoạt động. |
