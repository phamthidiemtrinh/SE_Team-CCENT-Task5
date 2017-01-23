# Định tuyến tĩnh

## 1. Định tuyến
- Định tuyến là tìm ra đường đi tối tưu từ điểm này tới điểm khác của mạng
- có 2 loại định tuyến :
  - định tuyến tĩnh : người quản trị trực tiếp  nhập thông tin hướng dẫn đường đi (static route) trong việc định tuyến
  - định tuyến động : các router tự học thông tin và tìm ra đường đi (Dynamic route) bằng giao thức định tuyến.
- router là thiết bị thuộc lớp layer 3, có khả năng định tuyến, để định tuyến được:
  - router cần biết địa chỉ đích đến của gói tin
  - xác định được nguồn gốc mà từ đó router có khả năng học theo 
  - biết được các đường đi khác có thể tới đích để tránh trường hợ đường đi tối ưu xảy ra lỗi
  - Duy trì thông tín định tuyến ( bảng định tuyến)
## 2. Cấu hình định tuyến tĩnh
- câu lệnh : Router (config) # ip route destination_subnet subnetmask{IP_next_hop|output_interface} [AD]
-trong đó :
  - destination_subnet: mạng đích đến.
  - subnetmask: subnet – mask của mạng đích.
  - IP_next_hop: địa chỉ IP của trạm kế tiếp trên đường đi.
  - output_interface: cổng ra trên router.
  - AD: chỉ số AD của route khai báo, sử dụng trong trường hợp có cấu hình dự phòng.
 
## 3.Default route
- cho phép router tối giản hoá bảng định tuyến ( chỉ nên áp dụng với mạng cụt stub network)
