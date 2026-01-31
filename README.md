# Lending Club Loan Data Analysis

## Giới thiệu
Dự án phân tích dữ liệu khoản vay từ Lending Club (2007-2018 Q4) sử dụng PySpark và Machine Learning để dự đoán tình trạng khoản vay.

## Mục tiêu
- Phân tích dữ liệu khoản vay từ Lending Club
- Xây dựng mô hình dự đoán khả năng trả nợ của khách hàng
- Đánh giá hiệu suất mô hình sử dụng các metrics như AUC-ROC

## Dataset
- **Nguồn**: Lending Club Loan Data (accepted_2007_to_2018Q4.csv)
- **Kích thước**: 2,260,701 hồ sơ × 151 đặc trưng
- **Thời gian**: Từ 2007 đến Q4/2018

### Các đặc trưng chính:
- `loan_amnt`: Số tiền vay
- `int_rate`: Lãi suất
- `grade`: Xếp hạng khoản vay
- `annual_inc`: Thu nhập hàng năm
- `loan_status`: Tình trạng khoản vay (target variable)

## Yêu cầu hệ thống

### Phần mềm
- Python 3.7+
- Apache Spark 3.x
- Jupyter Notebook hoặc Google Colab

### Thư viện
Xem file `requirements.txt` để biết chi tiết các thư viện cần thiết.

## Cài đặt

1. Clone repository:
```bash
git clone https://github.com/[your-username]/lending-club-analysis.git
cd lending-club-analysis
```

2. Cài đặt các thư viện cần thiết:
```bash
pip install -r requirements.txt
```

3. Tải dataset:
- Tải file `accepted_2007_to_2018Q4.csv` từ [Lending Club](https://www.lendingclub.com/info/download-data.action)
- Đặt file vào thư mục gốc của project

## Sử dụng

### Chạy trên Jupyter Notebook:
```bash
jupyter notebook DataMiningFinalProject__1_.ipynb
```

### Chạy trên Google Colab:
1. Upload notebook lên Google Drive
2. Mở bằng Google Colab
3. Upload dataset hoặc mount Google Drive

## Quy trình phân tích

### 1. Thiết lập môi trường
- Cài đặt PySpark
- Khởi tạo SparkSession
- Import các thư viện cần thiết

### 2. Đọc và khám phá dữ liệu
- Load dataset vào Spark DataFrame
- Kiểm tra kích thước và cấu trúc dữ liệu
- Phân tích thống kê mô tả

### 3. Tiền xử lý dữ liệu
- Xử lý missing values
- Chuyển đổi categorical features (StringIndexer, OneHotEncoder)
- Feature engineering
- Chuẩn hóa dữ liệu

### 4. Xây dựng mô hình
- Chia tập train/test
- Huấn luyện mô hình classification
- Tối ưu hyperparameters

### 5. Đánh giá mô hình
- Confusion Matrix
- Precision, Recall, F1-Score
- **AUC-ROC Score**: 0.6845

## Kết quả

### Hiệu suất mô hình
- **Area under ROC Curve (AUC)**: 0.6845
- Mô hình cho thấy khả năng phân loại khá tốt giữa các khoản vay tốt và xấu

### Visualizations
- ROC Curve
- Feature importance
- Distribution plots
- Correlation heatmap

## Cấu trúc thư mục
```
lending-club-analysis/
│
├── DataMiningFinalProject__1_.ipynb   # Notebook chính
├── README.md                           # File này
├── requirements.txt                    # Dependencies
├── .gitignore                          # Git ignore rules
│
├── data/                               # Thư mục data (không commit)
│   └── accepted_2007_to_2018Q4.csv
│
└── images/                             # Các hình ảnh, biểu đồ
    └── roc_curve.png
```

## Công nghệ sử dụng
- **PySpark**: Xử lý big data
- **Pandas**: Data manipulation
- **Matplotlib**: Data visualization
- **Spark MLlib**: Machine learning algorithms

## Đóng góp
Mọi đóng góp đều được chào đón! Vui lòng:
1. Fork repository
2. Tạo branch mới (`git checkout -b feature/AmazingFeature`)
3. Commit changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to branch (`git push origin feature/AmazingFeature`)
5. Mở Pull Request

## Tác giả
- **Tên của bạn** - [GitHub Profile](https://github.com/your-username)

## License
Project này được phân phối dưới giấy phép MIT License - xem file [LICENSE](LICENSE) để biết thêm chi tiết.

## Tài liệu tham khảo
- [Lending Club Statistics](https://www.lendingclub.com/info/statistics.action)
- [PySpark Documentation](https://spark.apache.org/docs/latest/api/python/)
- [Spark MLlib Guide](https://spark.apache.org/docs/latest/ml-guide.html)

## Liên hệ
- Email: your.email@example.com
- GitHub: [@your-username](https://github.com/your-username)

---
**Note**: Dataset này chỉ dùng cho mục đích học tập và nghiên cứu.
