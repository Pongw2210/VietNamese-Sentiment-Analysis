# Phân tích cảm xúc tiếng Việt (Vietnamese Sentiment Analysis)

Dự án phân loại cảm xúc văn bản tiếng Việt sử dụng các mô hình học máy và học sâu.

## Mục tiêu:
- Phân loại câu tiếng Việt thành 3 cảm xúc: **Tích cực**, **Tiêu cực**, **Trung lập**
- Huấn luyện và so sánh hiệu quả giữa mô hình truyền thống (ML) và mô hình học sâu (DL)
  
## Mô tả dự án:
### 1. Bộ dữ liệu
- Phát hành trên nền tảng Hugging Face bởi nhóm nghiên cứu UIT NLP tại Trường Đại học Công nghệ Thông tin – Đại học Quốc gia TP. Hồ Chí Minh.
- Bao gồm các bình luận tiếng Việt thực tế từ sinh viên, đã được gán nhãn cảm xúc theo ba nhóm chính: Tích cực, Trung lập, Tiêu cực.
### 2. Các mô hình được sử dụng huấn luyện
  - Naive Bayes Model
  - Logistic Regression Model
  - CNN +Bi-LSTM Model
  - MLP + FastText Model
  - PhoBert + FastText Model
### 3. Quy trình thực hiện
  - **Tiền xử lý dữ liệu**: Làm sạch văn bản, chuẩn hóa Unicode, loại bỏ ký tự đặc biệt, oversampling, v. v.
  - **Tách từ tiếng Việt**: Sử dụng thư viện `underthesea`.
  - **Vector hóa**:
    - TF-IDF cho các mô hình truyền thống (Naive Bayes, Logistic Regression)
    - FastText vector cho mô hình MLP
    - Embedding layer cho mô hình học sâu (CNN + Bi-LSTM)
  - **Huấn luyện mô hình**: Sử dụng tập train/test chia theo tỷ lệ tùy mỗi mô hình.
  - **Đánh giá mô hình**: Accuracy, Precision,Recall, F1-Score, Confusion Matrix.
### 4. Kết quả các mô hình

| Mô hình                 | Accuracy (ước lượng) | Ghi chú                                      |
|------------------------|----------------------|----------------------------------------------|
| Naive Bayes            | ~0.92                | Cơ bản, nhanh, sử dụng TF-IDF                |
| Logistic Regression    | ~0.87                | Hiệu quả, baseline tốt                       |
| CNN + Bi-LSTM          | ~0.93                | Học sâu, xử lý ngữ cảnh tốt                 |
| MLP + FastText         | ~0.89                | Kết hợp embedding hiệu quả                   |
| PhoBERT + FastText     | ~0.96                | Mô hình tốt nhất (nếu cấu hình đúng)         |


### 5. Thư viện sử dụng
  - Xử lý dữ liệu: pandas, re, underthesea
  - Học máy: scikit-learn
  - Học sâu: Keras, TensorFlow
  - Embedding: FastText, PhoBERT
  - Trực quan hóa: matplotlib, seaborn

## Thành viên thực hiện
Dự án được thực hiện bởi nhóm có 3 thành viên khóa học SIC và 1 thành viên khác.

## Tài liệu báo cáo
[![Google Drive](https://img.icons8.com/color/48/000000/google-drive--v2.png)](https://drive.google.com/drive/folders/1UTcIBk9B8qAUlJl3a69vgJ_iNVr1YOWh?usp=drive_link)

