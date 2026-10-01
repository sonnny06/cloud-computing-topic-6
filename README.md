# Xây dựng đám mây IaaS quy mô phòng thí nghiệm bằng nền tảng ảo hóa mã nguồn mở 
Câu hỏi nghiên cứu. Các cơ chế template, snapshot, phân bổ tài nguyên và di chuyển máy ảo  tạo ra năng lực IaaS như thế nào trên hạ tầng phần cứng giới hạn?

Mục tiêu của đề tài :
- Cài đặt và cấu hình nền tảng ảo hóa có khả năng cấp phát máy ảo theo mẫu. 
- Đánh giá ảnh hưởng của overcommit CPU và bộ nhớ đến hiệu năng và mức cô lập. 
- Xây dựng quy trình cấp phát, sao lưu, khôi phục và thu hồi máy ảo có ghi nhận bằng chứng.

Nội dung lý thuyết cần báo cáo :
- Hypervisor loại 1 và loại 2; vCPU, vRAM, virtual disk, bridge và virtual NIC. 
- Template, cloud-init, snapshot, clone, migration, thin provisioning và overcommit. 
- Đa thuê, cô lập tài nguyên, noisy neighbor và giới hạn của snapshot so với backup. 
- Ánh xạ các chức năng của phòng thí nghiệm vào lớp resource abstraction and control của kiến trúc NIST.

Yêu cầu thực nghiệm 
- Cài nền tảng trên máy vật lý hoặc nested virtualization; tạo template Linux tích hợp cloud
init. 
- Tự động cấp phát ít nhất ba máy ảo thuộc hai mạng logic, áp dụng quota hoặc giới hạn tài 
nguyên. 
- Đo CPU, I/O và độ trễ mạng khi tải đơn và khi xuất hiện noisy neighbor. 
- Thực hiện snapshot, backup, restore và nếu hạ tầng cho phép, migration; ghi thời gian và 
mức gián đoạn. 

Kết quả và minh chứng cần đạt 
- Cụm IaaS hoặc nút ảo hóa hoạt động, kèm sơ đồ vật lý - logic và danh mục tài nguyên. 
- Template chuẩn, kịch bản cấp phát tự động và chính sách đặt tên, quota, vòng đời. 
- Bảng benchmark thể hiện mức suy giảm do tranh chấp tài nguyên và giải pháp hạn chế. 
- Biên bản kiểm thử khôi phục chứng minh dữ liệu và dịch vụ trở lại đúng trạng thái mong 
đợi. 

Tài liệu nghiên cứu gợi ý. [2], [9], [33] và Bài giảng Chương 2 : https://courses.ut.edu.vn/pluginfile.php/1408118/mod_resource/content/0/Chapter2.pdf

Công nghệ gợi ý. Proxmox VE/KVM hoặc OpenStack DevStack; cloud-init; Ansible; fio, 
iperf3, stress-ng; Prometheus Node Exporter. 
