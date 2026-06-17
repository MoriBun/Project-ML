# Project Final - Dự đoán giai đoạn xơ gan (Liver Cirrhosis)

Đồ án cuối kỳ môn Machine Learning: phân tích, tiền xử lý và xây dựng các mô hình học máy để dự đoán **giai đoạn bệnh xơ gan (Stage)** dựa trên bộ dữ liệu `liver_cirrhosis.csv` (25.000 dòng, 19 cột).

## Cấu trúc thư mục

```
Project-ML/
├── Code/
│   ├── Code_Final.ipynb     # Notebook chính chứa toàn bộ code
│   └── data/
│       └── data.zip         # Chứa liver_cirrhosis.csv
├── Báo cáo.pdf               # Báo cáo chi tiết của đồ án
├── Bản trình bày.pdf          # Slide trình bày
└── Tệp_thông_tin.pdf         # Thông tin nhóm & hướng dẫn chạy chương trình
```

## Nội dung thực hiện

Notebook `Code_Final.ipynb` được tổ chức theo các phần chính:

1. **Tiền xử lý dữ liệu**: đọc dữ liệu, mô tả & thống kê sơ bộ, kiểm tra giá trị thiếu/bất thường, chuyển đổi đơn vị, xử lý outliers, chuẩn hóa dữ liệu.
2. **Phân tích và trực quan hóa dữ liệu**: khảo sát phân bố các trường, mối liên hệ giữa các đặc trưng và giai đoạn bệnh.
3. **Phân cụm dữ liệu**: áp dụng K-Means, đánh giá bằng WCSS (Elbow) và Silhouette Score.
4. **Phân loại**: áp dụng và so sánh các mô hình KNN, MLP, SVM trên dữ liệu gốc và dữ liệu sau giảm chiều (PCA/LDA).
5. **Hồi quy**: chuyển bài toán phân loại giai đoạn về dạng hồi quy, áp dụng MLP và Linear Regression.

## Thành viên nhóm và phân công

| Thành viên | MSV | Công việc |
|---|---|---|
| Nguyễn Huy Hoàng (Trưởng nhóm) | 22000095 | Tiền xử lý dữ liệu, phân tích dữ liệu, mô hình KNN (phân loại), Random Forest (hồi quy) |
| Tạ Đăng Đức | 22000088 | Phân cụm dữ liệu, mô hình MLP (phân loại), Linear Regression (hồi quy) |
| Đào Mạnh Đức | 22000085 | Giảm chiều dữ liệu (PCA - LDA), mô hình SVM (phân loại) |

## Hướng dẫn chạy chương trình

Chương trình được xây dựng để chạy trên **Google Colab**.

1. Truy cập [Google Colab](https://colab.research.google.com/) và tải lên file `Code/Code_Final.ipynb`.
2. Tải thư mục `Code/data` (chứa `data.zip`) lên Colab, ghi nhớ đường dẫn (ví dụ `/content/data`).
3. Trong notebook, tìm và sửa biến đường dẫn file zip cho khớp với vị trí thực tế, ví dụ:
   ```python
   local_zip = '/content/data/data.zip'
   extract_to = '/content/'
   ```
4. Chạy lần lượt các cell:
   - Kết nối Google Drive (nếu sử dụng Drive để lưu trữ dữ liệu).
   - Import các thư viện cần thiết.
   - Giải nén `data.zip`.
   - Đọc dữ liệu từ `liver_cirrhosis.csv`.
   - Các cell tiếp theo: tiền xử lý, phân tích, huấn luyện và hiển thị kết quả mô hình.

> Nếu không chạy trên Colab, cần chỉnh lại đường dẫn dữ liệu phù hợp với môi trường cục bộ.

Thông tin chi tiết hơn về cách tổ chức và chạy chương trình xem tại [Tệp_thông_tin.pdf](Tệp_thông_tin.pdf).

## Tài liệu liên quan

- [Báo cáo.pdf](Báo%20cáo.pdf): báo cáo chi tiết toàn bộ đồ án.
- [Bản trình bày.pdf](Bản%20trình%20bày.pdf): slide trình bày.
