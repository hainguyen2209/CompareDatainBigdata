-	Thuật toán này sử dụng một trong những thuật toán mã hóa băm (hashing algorithm), được sử dụng để tạo ra các giá trị băm (hash value) đại diện cho một chuỗi dữ liệu bất kỳ.
-	Thuật toán sử dụng một chuỗi các phép biến đổi trên một khối dữ liệu đầu vào để tạo ra một giá trị băm có độ dài cố định là 128 bit (16 byte – độ dài này có thể điều chỉnh để tăng tính bảo mật và nhận diện dữ liệu, tuy nhiên, mục tiêu ở đây là so sánh toàn bộ dữ liệu nên không cần kéo dài chuỗi số liệu đầu ra – trong một mục tiêu khác, khi phát hiện dữ liệu không khớp, thì mới cần thực thi lại thuật toán ở mức 512 bit để phát hiện điểm bất thường – anomaly detection). Các bước chính của thuật toán như sau:
1.	Khởi tạo bộ đệm: Ban đầu, một bộ đệm 128 bit được khởi tạo để lưu trữ các giá trị trung gian trong quá trình tính toán.
2.	Chia khối dữ liệu đầu vào: Khối dữ liệu đầu vào được chia thành nhiều khối con có độ dài bằng nhau (512 bit).
3.	Tiền xử lý dữ liệu: Mỗi khối con sẽ được tiền xử lý để chuẩn bị cho các bước tiếp theo của thuật toán.
4.	Điều chỉnh bộ đệm: Bộ đệm sẽ được điều chỉnh thông qua các phép XOR, xoay trái và phép trộn bit.
Tính toán giá trị băm: Cuối cùng, giá trị băm sẽ được tính toán dựa trên giá trị của bộ đệm.
