# CAB System – Phân tích yêu cầu
# Bước 1: Hiểu rõ hệ thống
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
    subgraph KH["Khách hàng"] 
        KH_S["Khách hàng"] 
        KH_P1["Quản lý tài khoản"] 
        KH_P2["Đặt xe"] 
        KH_P3["Theo dõi chuyến đi"] 
        KH_P4["Xem lịch sử chuyến đi"] 
        KH_P5["Tính cước"] 
        KH_P6["Thanh toán"] 
        KH_P7["Nhận thông báo"] 
        KH_P8["Đánh giá tài xế"] 
        KH_M["Chưa xác định metric trong case study"] 

        KH_S --> KH_P1 
        KH_S --> KH_P2 
        KH_S --> KH_P3 
        KH_S --> KH_P4 
        KH_S --> KH_P5 
        KH_S --> KH_P6 
        KH_S --> KH_P7 
        KH_S --> KH_P8 
        KH_P1 --> KH_M 
        KH_P2 --> KH_M 
        KH_P3 --> KH_M 
        KH_P4 --> KH_M 
        KH_P5 --> KH_M 
        KH_P6 --> KH_M 
        KH_P7 --> KH_M 
        KH_P8 --> KH_M 
    end 

    subgraph TX["Tài xế"] 
        TX_S["Tài xế"] 
        TX_P1["Quản lý tài khoản"] 
        TX_P2["Tìm kiếm và phân công tài xế"] 
        TX_P3["Thực hiện chuyến đi"] 
        TX_P4["Gửi thông báo"] 
        TX_M["Chưa xác định metric trong case study"] 

        TX_S --> TX_P1 
        TX_S --> TX_P2 
        TX_S --> TX_P3 
        TX_S --> TX_P4 
        TX_P1 --> TX_M 
        TX_P2 --> TX_M 
        TX_P3 --> TX_M 
        TX_P4 --> TX_M 
    end 

    subgraph VH["Nhân viên vận hành"] 
        VH_S["Nhân viên vận hành"] 
        VH_P1["Quản lý khách hàng"] 
        VH_P2["Quản lý tài xế"] 
        VH_P3["Quản lý phương tiện"] 
        VH_P4["Quản lý chuyến đi"] 
        VH_P5["Xử lý chuyến bị lỗi"] 
        VH_P6["Tra cứu lịch sử giao dịch"] 
        VH_P7["Quản lý phân quyền"] 
        VH_M["Chưa xác định metric trong case study"] 

        VH_S --> VH_P1 
        VH_S --> VH_P2 
        VH_S --> VH_P3 
        VH_S --> VH_P4 
        VH_S --> VH_P5 
        VH_S --> VH_P6 
        VH_S --> VH_P7 
        VH_P1 --> VH_M 
        VH_P2 --> VH_M 
        VH_P3 --> VH_M 
        VH_P4 --> VH_M 
        VH_P5 --> VH_M 
        VH_P6 --> VH_M 
        VH_P7 --> VH_M 
    end 

    subgraph LD["Ban lãnh đạo / Ban giám đốc"] 
        LD_S["Ban lãnh đạo / Ban giám đốc"] 
        LD_P["Báo cáo hoạt động"] 
        LD_M1["Số lượng chuyến"] 
        LD_M2["Doanh thu"] 
        LD_M3["Tỷ lệ chuyến hoàn thành"] 
        LD_M4["Tỷ lệ hủy"] 
        LD_M5["Hiệu quả hoạt động của tài xế"] 

        LD_S --> LD_P 
        LD_P --> LD_M1 
        LD_P --> LD_M2 
        LD_P --> LD_M3 
        LD_P --> LD_M4 
        LD_P --> LD_M5 
    end 

    subgraph NTTT["Nhà cung cấp thanh toán bên ngoài"] 
        NTTT_S["Nhà cung cấp thanh toán bên ngoài"] 
        NTTT_P["Thanh toán"] 
        NTTT_M["Chưa xác định metric trong case study"] 

        NTTT_S --> NTTT_P 
        NTTT_P --> NTTT_M 
    end 

    subgraph BA["Business Analyst"] 
        BA_S["Business Analyst"] 
        BA_P["Phân tích và làm rõ yêu cầu"] 
        BA_M["Chưa xác định metric trong case study"] 

        BA_S --> BA_P 
        BA_P --> BA_M 
    end 

    classDef stakeholder stroke:#818cf8,fill:#eef2ff 
    classDef process stroke:#2dd4bf,fill:#f0fdfa 
    classDef metric stroke:#fb923c,fill:#fff7ed 
    classDef noMetric stroke:#f87171,fill:#fef2f2 

    class KH_S,TX_S,VH_S,LD_S,NTTT_S,BA_S stakeholder 
    class KH_P1,KH_P2,KH_P3,KH_P4,KH_P5,KH_P6,KH_P7,KH_P8,TX_P1,TX_P2,TX_P3,TX_P4,VH_P1,VH_P2,VH_P3,VH_P4,VH_P5,VH_P6,VH_P7,LD_P,NTTT_P,BA_P process 
    class LD_M1,LD_M2,LD_M3,LD_M4,LD_M5 metric 
    class KH_M,TX_M,VH_M,NTTT_M,BA_M noMetric
```
