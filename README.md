# IPv6 Quy hoạch IPv6 cho doanh nghiệp nhỏ

## Giới thiệu

Dự án xây dựng và mô phỏng mô hình mạng IPv6 cho một doanh nghiệp nhỏ bằng Cisco Packet Tracer. Mục tiêu là thiết kế hệ thống mạng có cấu trúc rõ ràng, phân chia mạng theo phòng ban và kiểm tra khả năng kết nối, định tuyến cũng như kiểm soát truy cập giữa các mạng con.
<img width="668" height="550" alt="image" src="https://github.com/user-attachments/assets/dbf7d485-919a-474a-9457-6d7a3c5d8df9" />


## Công nghệ sử dụng

* **Cisco Packet Tracer:** Thiết kế topology và mô phỏng hệ thống mạng.
* **IPv6:** Quy hoạch địa chỉ và định tuyến giữa các mạng con.
* **VLAN:** Phân chia mạng theo từng phòng ban.
* **Trunk:** Truyền lưu lượng của nhiều VLAN trên liên kết giữa các thiết bị mạng.
* **Static Routing:** Định tuyến IPv6 giữa hai router.
* **DNS:** Phân giải tên máy chủ nội bộ thành địa chỉ IPv6.
* **IPv6 ACL:** Kiểm soát lưu lượng truy cập giữa các mạng theo chính sách đã cấu hình.

## Nội dung triển khai

* Thiết kế topology gồm router, switch, máy trạm và máy chủ.
* Quy hoạch địa chỉ IPv6 sử dụng dải tài liệu `2001:DB8:16::/48`.
* Phân chia các VLAN cho Hành chính, Kế toán, Kỹ thuật, Quản lý và Máy chủ.
* Cấu hình địa chỉ IPv6, gateway và định tuyến giữa các mạng.
* Cấu hình DNS nội bộ với tên `server.congty.local`.
* Thiết lập ACL để chặn lưu lượng từ VLAN 10 đến VLAN 30, đồng thời cho phép các lưu lượng IPv6 khác theo quy tắc đã cấu hình.

## Kết quả kiểm thử

* Các máy trạm có thể giao tiếp với gateway IPv6 tương ứng.
* Kiểm thử ping giữa các mạng con và giữa hai router cho kết quả thành công trước khi áp dụng ACL.
* Máy trạm phân giải được tên `server.congty.local` thành địa chỉ IPv6 của máy chủ.
* Sau khi áp dụng ACL, lưu lượng từ VLAN 10 đến VLAN 30 bị chặn, trong khi kết nối từ VLAN 10 đến máy chủ ở VLAN 50 vẫn hoạt động.
* Kết quả được kiểm tra bằng các lệnh CLI và công cụ Command Prompt trong Cisco Packet Tracer.

## Cấu trúc sản phẩm

* `IPv6_DoanhNghiep_BanGoc.pkt`: Mô hình cơ sở dùng để kiểm tra kết nối trước khi áp dụng ACL.
* `IPv6_DoanhNghiep_ACL.pkt`: Mô hình thử nghiệm với chính sách ACL IPv6.
* `IPv6_DoanhNghiep_HoanThien.pkt`: Phiên bản hoàn thiện, nếu đã lưu riêng.

## Mục tiêu đạt được

Dự án giúp củng cố kiến thức về thiết kế mạng IPv6, phân chia VLAN, định tuyến tĩnh, cấu hình DNS và kiểm soát truy cập. Đồng thời, quá trình mô phỏng và kiểm thử giúp làm rõ mối liên hệ giữa thiết kế mạng, cấu hình thiết bị và kết quả vận hành thực tế.

## Phạm vi và giới hạn

Đây là mô hình mô phỏng phục vụ học tập, không phải hệ thống đã triển khai trong môi trường doanh nghiệp thực tế. Dải địa chỉ `2001:DB8::/32` được sử dụng cho tài liệu và ví dụ, không dùng làm địa chỉ IPv6 định tuyến công khai trên Internet.

## Tác giả và mục đích

Dự án được thực hiện trong khuôn khổ học phần **Mạng máy tính**, nhằm thực hành quy hoạch và cấu hình mạng IPv6 trên Cisco Packet Tracer.
