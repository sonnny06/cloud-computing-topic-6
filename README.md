# Xây dựng đám mây IaaS quy mô phòng thí nghiệm bằng nền tảng ảo hóa mã nguồn mở 
Câu hỏi nghiên cứu. Các cơ chế template, snapshot, phân bổ tài nguyên và di chuyển máy ảo  tạo ra năng lực IaaS như thế nào trên hạ tầng phần cứng giới hạn?
** Mục tiêu của đề tài ** 
- Cài đặt và cấu hình nền tảng ảo hóa có khả năng cấp phát máy ảo theo mẫu. 
- Đánh giá ảnh hưởng của overcommit CPU và bộ nhớ đến hiệu năng và mức cô lập. 
- Xây dựng quy trình cấp phát, sao lưu, khôi phục và thu hồi máy ảo có ghi nhận bằng chứng. 
**Nội dung lý thuyết cần báo cáo **
- Hypervisor loại 1 và loại 2; vCPU, vRAM, virtual disk, bridge và virtual NIC. 
- Template, cloud-init, snapshot, clone, migration, thin provisioning và overcommit. 
- Đa thuê, cô lập tài nguyên, noisy neighbor và giới hạn của snapshot so với backup. 
- Ánh xạ các chức năng của phòng thí nghiệm vào lớp resource abstraction and control của kiến trúc NIST.
