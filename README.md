# Automatic Number Plate Detection

## Mô tả
Đây là ứng dụng **Nhận diện biển báo xe theo thời gian thực**.

## Video demo
Video demo sử dụng cho dự án này có thể tải ở [đây](https://www.pexels.com/video/traffic-flow-in-the-highway-2103099/).

## Mô hình
Dự án sử dụng mô hình pre-trained của Yolov8 để phát hiện ra các phương tiện và biển số của chúng. Trong đó mô hình phát hiện biển số được huấn luyện với bộ dataset [này](https://universe.roboflow.com/carplates2/licenseplate_v2).

![alt text](https://github.com/Raggza/hinh/blob/main/ANPR/yolo.png)

Đọc thêm về Yolov8 tại [đây](https://github.com/ultralytics/ultralytics).

## Cách sử dụng:
1. [train.ipynb](https://github.com/Raggza/ANPR/blob/main/train.ipynb): Sử dụng để huấn luyện mô hình phát hiện biển số
2. [data.yaml](https://github.com/Raggza/ANPR/blob/main/data.yaml): File chứa các đường dẫn đến các thư mục ảnh khác nhau
3. [main.py](https://github.com/Raggza/ANPR/blob/main/main.py): Phát hiện các phương tiện và biển số, lưu lại các giá trị vào 1 file csv.
4. [util.py](https://github.com/Raggza/ANPR/blob/main/util.py): Chứa các hàm hỗ trợ cho file main.py
5. [add_mising_data.py](https://github.com/Raggza/ANPR/blob/main/add_missing_data.py): Bổ sung thêm các dữ liệu còn thiếu của video.
6. [visualize.py](https://github.com/Raggza/ANPR/blob/main/visualize.py): Đưa ra kết quả cuối cùng.
7. [best.pt](https://github.com/Raggza/ANPR/blob/main/best.pt): Pre-trained của dữ liệu với 100 epochs.

**Lưu ý:**
1. Thay đổi các đường dẫn phù hợp với setup của người dùng.
2. Module sort dùng trong **main.py** có thể tìm thấy ở [repository này](https://github.com/abewley/sort).

## Kết quả:

Xem kết quả tại [đây](https://drive.google.com/file/d/1Ean7OXgxaNQCvAUuOBKDYxFTfrPt4mZW/view?usp=drive_link).
