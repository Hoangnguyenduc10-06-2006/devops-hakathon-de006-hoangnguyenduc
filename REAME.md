
sudo ufw allow 80/tcp
sudo ufw enable

=== thay đổi ssh
# Mở cổng 2222 giao thức TCP trên tường lửa UFW (bắt buộc làm trước để không bị mất kết nối)
sudo ufw allow 2222/tcp

# Kiểm tra trạng thái UFW để đảm bảo cổng 2222 đã nằm trong danh sách cho phép (ALLOW)
sudo ufw status

# Mở tệp cấu hình chính của dịch vụ SSH daemon để đổi thông số Port
sudo nano /etc/ssh/sshd_config

# Kiểm tra tính đúng đắn về mặt cú pháp của cấu hình SSH trước khi áp dụng
sudo sshd -t
