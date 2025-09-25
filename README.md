# Analyzing-data-from-the-Quotes-website
Phân tích dữ liệu từ trang web http://quotes.toscrape.com
# Khai Phá Dữ Liệu Từ Câu Nói Của Người Nổi Tiếng

## Giới thiệu

Thu thập, xử lý và khai phá dữ liệu từ các câu nói của người nổi tiếng được đăng tải trên trang web [http://quotes.toscrape.com](http://quotes.toscrape.com). Mục tiêu là xây dựng một pipeline từ việc thu thập dữ liệu đến phân tích, trích xuất đặc trưng và phân loại phong cách nói của từng tác giả.

---

## 1. Thu thập dữ liệu

- **Nguồn dữ liệu**: 10 trang đầu tiên tại http://quotes.toscrape.com
- **Công cụ sử dụng**: `requests`, `BeautifulSoup`
- **Dữ liệu thu thập được**: HTML các thẻ `div` có class `quote`
- **Thông tin trích xuất**:
  - Câu nói
  - Tên tác giả
  - Link thông tin tác giả
  - Ngày sinh tác giả

---

## 2. Xử lý và làm sạch dữ liệu

- Chuyển đổi định dạng ngày sinh về kiểu `datetime`
- Tự động điền số thứ tự, tính tuổi tác giả
- Lưu trữ dữ liệu sạch vào file `Quote.csv`

---

## 3. Khai phá và phân tích dữ liệu

- Thống kê:
  - Số lượng câu nói theo từng tác giả
  - Câu nói ngắn nhất / dài nhất
  - Từ xuất hiện phổ biến
- Trích xuất đặc trưng sử dụng **Bag of Words (BoW)** với `CountVectorizer`

---

## Mô hình hóa & Suy luận

- **Phân loại câu nói theo tác giả**:
  - Sử dụng các mô hình như: Logistic Regression, SVM, RandomForest
  - Đánh giá bằng các chỉ số: Accuracy, Precision, Recall, F1-score

- **Tính độ tương đồng phong cách nói giữa các tác giả**:
  - Áp dụng cosine similarity hoặc khoảng cách Euclidean

---

## Công nghệ sử dụng

- Python
- BeautifulSoup, Requests
- Pandas, NumPy
- Scikit-learn, Matplotlib, Seaborn
- Selenium (hỗ trợ thu thập dữ liệu động)

---

## 📁 Cấu trúc thư mục

