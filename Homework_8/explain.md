# Giải thích bài 2.3
## Phần 2.3.1
### 1.Import các thư viện cần thiết:

- train_test_split: Chia dữ liệu thành tập huấn luyện và tập kiểm tra.
- StandardScaler: Chuẩn hóa dữ liệu để các giá trị của các features có giá trị trung bình là 0 và độ lệch chuẩn là 1.
- LinearRegression: Mô hình hồi quy tuyến tính.
- Pipeline: Kết hợp các bước tiền xử lý và huấn luyện mô hình thành một chuỗi các bước.

### 2.Tách dữ liệu:

- X là các feature (đặc trưng) được chọn (trong trường hợp này là các đặc trưng như MedInc, HouseAge,...).
- y là biến mục tiêu (MedHouseVal), mà chúng ta muốn dự đoán.

### 3.Chia dữ liệu:

- Dùng train_test_split để chia dữ liệu thành 80% cho tập huấn luyện và 20% cho tập kiểm tra.

### 4.Pipeline:

- Pipeline giúp tạo một chuỗi các bước, trong đó dữ liệu sẽ được chuẩn hóa qua StandardScaler và sau đó mô hình hồi quy tuyến tính LinearRegression sẽ được huấn luyện trên dữ liệu đã chuẩn hóa.

### 5.Huấn luyện và dự đoán:

- pipeline.fit(X_train, y_train) huấn luyện mô hình.
- pipeline.predict(X_test) thực hiện dự đoán cho dữ liệu kiểm tra.

## Phần 2.3.2
### 1.Tính kích thước tập huấn luyện:

- train_size = int(0.8 * len(data)): Tính toán 80% của tổng số mẫu trong dữ liệu, đó là kích thước của tập huấn luyện.
### 2.Chia dữ liệu:

- train_data = data[:train_size]: Lấy 80% đầu của dữ liệu làm tập huấn luyện.
- test_data = data[train_size:]: Lấy 20% còn lại làm tập kiểm tra.
### 3.Tạo các biến đặc trưng và mục tiêu:

- X_train: Các đặc trưng trong tập huấn luyện.
- y_train: Mục tiêu trong tập huấn luyện.
- X_test: Các đặc trưng trong tập kiểm tra.
- y_test: Mục tiêu trong tập kiểm tra.
