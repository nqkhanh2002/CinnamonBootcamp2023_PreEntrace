<a name="readme-top"></a>
<div align="center">
  <p align="center">
    <a href="https://www.youtube.com/channel/UCKaMI0RBxF26f6j0Q8RRyTw">View Demo</a>
    ·
    <a href="https://github.com/nqkhanh2002/CinnamonBootcamp2023_PreEntrace/issues">Report Bug</a>
    ·
    <a href="https://github.com/nqkhanh2002/CinnamonBootcamp2023_PreEntrace/pulls">Request Feature</a>
  </p>
</div>

<h1 align="center">LANE DETECTION APPLICATION IN SELF-DRIVING CAR</h1>

<div align="center">
  <img src="intro.gif" alt="Result Example" width="800px">
</div>


Phát hiện làn đường là một nhiệm vụ thị giác máy tính liên quan đến việc xác định ranh giới của các làn đường lái xe trong video hoặc hình ảnh về cảnh đường. Mục tiêu là định vị và theo dõi chính xác vạch kẻ đường trong thời gian thực, ngay cả trong những điều kiện khó khăn như ánh sáng kém, ánh sáng chói hoặc bố cục đường phức tạp.

Kho lưu trữ này phát triển một giải pháp phát hiện và theo dõi làn đường cho xe tự lái. Đây là một phần quan trọng của hệ thống lái tự động, nhằm đảm bảo an toàn và hiệu quả cho người lái và hành khách trên đường.
# Thành viên nhóm 
| STT | Họ và tên | MSSV |
|-------|-------|-------|
| 1 | Nguyễn Quốc Khánh | 20521452 |
| 2 | Đinh Phương Nam | 20520641 |
# Cấu trúc dự án
# Phương pháp
Bài toán triển khai gồm 3 phần: 
1. Phương pháp xử lý ảnh truyền thống
2. Phương pháp mạng nơ-ron học sâu
3. Xây dựng giao diện người dùng (GUI) để sử dụng và so sánh 2 phương pháp 
------- 
## Phương pháp xử lý ảnh truyền thống
1. Tính toán ma trận hiệu chỉnh camera (camera calibration matrix) và hệ số méo hình ảnh (distortion coefficients).
2. Áp dụng sự hiệu chỉnh méo cho ảnh gốc.
3. Sử dụng các chuyển đổi màu sắc, độ dốc, vv, để tạo ra một hình ảnh nhị phân được ngưỡng.
4. Áp dụng phép chuyển đổi góc nhìn để tạo ra một "góc nhìn chim" của hình ảnh.
5. Phát hiện các pixel của làn đường và phù hợp để tìm ranh giới của làn đường.
6. Xác định độ cong của làn đường và vị trí xe so với trung tâm.
7. Chuyển đổi lại ranh giới của làn đường được phát hiện trở lại hình ảnh ban đầu và hiển thị ước tính số liệu của độ cong của làn đường và vị trí xe.
## Phương pháp học sâu 
1. Mô hình SCNN-Tensorflow
## Xây dựng giao diện người dùng (GUI)
## Cách chạy chương trình
1. Cài đặt các thư viện cần thiết bằng lệnh sau:
```
pip install -r requirements.txt
```
2. Chạy chương trình bằng lệnh trong file command_pipline.txt
- main.py [--video] INPUT_PATH OUTPUT_PATH 

Trong đó tham số INPUT_PATH là đường dẫn đến video hoặc ảnh đầu vào, OUTPUT_PATH là đường dẫn đến video hoặc ảnh đầu ra, [--video] là tham số để chương trình biết INPUT_PATH là video hay ảnh.
- Ví dụ:
```
python Image_Processing/main.py --video Test_Video/video_test_01.mp4 Results/output_test_01.mp4
```
3. Báo cáo kỹ thuật trong file Report.pdf
4. [Link colab cho triển khai nhanh source code](https://colab.research.google.com/drive/1ymFbIRuQhlgN0u20zoaH9lyR3gm5emF0?usp=sharing)
