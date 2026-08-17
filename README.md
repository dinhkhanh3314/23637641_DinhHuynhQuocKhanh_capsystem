# CAB System – Phân tích yêu cầu
## Bước 1: Hiểu rõ hệ thống
## 1. Tại sao cần hệ thống?

Công ty ABC cần xây dựng hệ thống CAB mới để khắc phục những hạn chế của hệ thống hiện tại, đặc biệt là việc phân công tài xế còn thủ công, khách hàng khó theo dõi trạng thái chuyến đi, thông tin thanh toán chưa được quản lý tập trung và bộ phận vận hành gặp khó khăn khi mở rộng hệ thống. Hệ thống mới sẽ giúp tự động hóa quy trình đặt xe và tìm kiếm tài xế, quản lý tập trung dữ liệu, nâng cao trải nghiệm khách hàng và hiệu quả vận hành. Đồng thời, hệ thống được định hướng xây dựng như một nền tảng có khả năng phục vụ số lượng lớn khách hàng và tài xế, cũng như hỗ trợ mở rộng thêm các dịch vụ và tính năng trong tương lai.

## 2. Các vấn đề hiện hữu

- Việc phân công tài xế chủ yếu được thực hiện thủ công.
- Khách hàng khó theo dõi trạng thái chuyến đi.
- Thông tin thanh toán chưa được quản lý tập trung.
- Bộ phận vận hành gặp khó khăn khi muốn mở rộng hệ thống.
- Hệ thống cần có khả năng phục vụ số lượng lớn khách hàng và tài xế.
- Hệ thống hiện tại còn hạn chế trong việc phát triển thêm các tính năng trong tương lai.

## 3. Ai sẽ tham gia vào hệ thống?

- **Khách hàng**
  - Đặt xe và theo dõi chuyến đi.
  - Xem lịch sử chuyến đi.
  - Thanh toán và đánh giá tài xế.

- **Tài xế**
  - Nhận và thực hiện chuyến đi.
  - Cập nhật trạng thái chuyến đi.
  - Cập nhật vị trí.

- **Nhân viên vận hành**
  - Quản lý khách hàng, tài xế, phương tiện và chuyến đi.
  - Theo dõi chuyến đi và trạng thái tài xế.
  - Hỗ trợ xử lý các trường hợp chuyến bị lỗi.

- **Ban lãnh đạo**
  - Theo dõi các báo cáo về hoạt động kinh doanh.

- **Nhà cung cấp thanh toán bên ngoài**
  - Xử lý các giao dịch thanh toán điện tử.

## 4. Giá trị kinh doanh của hệ thống mới

- Tự động hóa việc tìm kiếm và phân công tài xế.
- Nâng cao trải nghiệm khách hàng thông qua khả năng theo dõi chuyến đi.
- Quản lý tập trung thông tin khách hàng, tài xế, phương tiện, chuyến đi và giao dịch.
- Nâng cao hiệu quả hoạt động của bộ phận vận hành.
- Hỗ trợ quản lý hoạt động kinh doanh thông qua các báo cáo.
- Đáp ứng số lượng lớn khách hàng và tài xế khi nhu cầu tăng cao.
- Tạo nền tảng có khả năng mở rộng và phát triển thêm các tính năng trong tương lai.

## Bước 2. Stakeholder

## 1. Các stakeholder của hệ thống
| Stakeholder | Vai trò | Tương tác với hệ thống |
|---|---|---|
| **Khách hàng** | Sử dụng dịch vụ đặt xe | Đăng ký, đăng nhập, quản lý thông tin cá nhân, đặt xe, theo dõi chuyến đi, xem lịch sử, thanh toán, nhận thông báo và đánh giá tài xế |
| **Tài xế** | Thực hiện chuyến đi | Quản lý hồ sơ và phương tiện, cập nhật trạng thái, nhận thông báo, chấp nhận/từ chối chuyến, cập nhật trạng thái chuyến và vị trí |
| **Nhân viên vận hành** | Quản lý hoạt động vận hành | Quản lý khách hàng, tài xế, phương tiện, chuyến đi; theo dõi chuyến, kiểm tra trạng thái tài xế, xử lý chuyến bị lỗi và tra cứu giao dịch |
| **Ban lãnh đạo** | Quản lý hoạt động kinh doanh | Theo dõi số lượng chuyến, doanh thu, tỷ lệ hoàn thành, tỷ lệ hủy và hiệu quả hoạt động của tài xế |
| **Nhà cung cấp thanh toán bên ngoài** | Cung cấp dịch vụ thanh toán điện tử | Tích hợp với CAB để xử lý giao dịch thanh toán điện tử và trả kết quả giao dịch về hệ thống |

## 2. Stakeholder metrics
```mermaid
flowchart LR

    KH["Khách hàng"]
    TX["Tài xế"]
    VH["Nhân viên vận hành"]
    LD["Ban lãnh đạo / Ban giám đốc"]
    NTTT["Nhà cung cấp thanh toán bên ngoài"]
    BA["Business Analyst"]

    KH --> KH_P1["Quản lý tài khoản"]
    KH --> KH_P2["Đặt xe"]
    KH --> KH_P3["Theo dõi chuyến đi"]
    KH --> KH_P4["Xem lịch sử chuyến đi"]
    KH --> KH_P5["Tính cước"]
    KH --> KH_P6["Thanh toán"]
    KH --> KH_P7["Nhận thông báo"]
    KH --> KH_P8["Đánh giá tài xế"]

    TX --> TX_P1["Quản lý tài khoản"]
    TX --> TX_P2["Nhận và xử lý yêu cầu chuyến"]
    TX --> TX_P3["Thực hiện chuyến đi"]
    TX --> TX_P4["Cập nhật trạng thái và vị trí"]

    VH --> VH_P1["Quản lý khách hàng"]
    VH --> VH_P2["Quản lý tài xế"]
    VH --> VH_P3["Quản lý phương tiện"]
    VH --> VH_P4["Quản lý chuyến đi"]
    VH --> VH_P5["Xử lý chuyến bị lỗi"]
    VH --> VH_P6["Tra cứu lịch sử giao dịch"]
    VH --> VH_P7["Quản lý phân quyền"]

    LD --> LD_P["Báo cáo hoạt động"]
    LD_P --> LD_M1["Số lượng chuyến"]
    LD_P --> LD_M2["Doanh thu"]
    LD_P --> LD_M3["Tỷ lệ chuyến hoàn thành"]
    LD_P --> LD_M4["Tỷ lệ hủy"]
    LD_P --> LD_M5["Hiệu quả hoạt động của tài xế"]

    NTTT --> NTTT_P["Thanh toán"]
    BA --> BA_P["Phân tích và làm rõ yêu cầu"]

    classDef stakeholder fill:#eef2ff,stroke:#818cf8
    classDef process fill:#f0fdfa,stroke:#2dd4bf
    classDef metric fill:#fff7ed,stroke:#fb923c

    class KH,TX,VH,LD,NTTT,BA stakeholder
    class KH_P1,KH_P2,KH_P3,KH_P4,KH_P5,KH_P6,KH_P7,KH_P8 process
    class TX_P1,TX_P2,TX_P3,TX_P4 process
    class VH_P1,VH_P2,VH_P3,VH_P4,VH_P5,VH_P6,VH_P7 process
    class LD_P,NTTT_P,BA_P process
    class LD_M1,LD_M2,LD_M3,LD_M4,LD_M5 metric
```
