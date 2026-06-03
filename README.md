# Đồ án Môn học: Dữ liệu Lớn (Big Data)
**Mã môn học:** IS405.Q23  
**Đề tài:** Ứng dụng và Tinh chỉnh các Mô hình Ngôn ngữ Lớn (LLMs) mã nguồn mở nhằm lấp đầy khoảng trống nghiên cứu từ bài báo gốc.

---

## 📝 Giới thiệu dự án và Mục tiêu Nghiên cứu
Đồ án này được thực hiện với định hướng nghiên cứu chuyên sâu, lấy cảm hứng từ một bài báo khoa học gốc. Thay vì chỉ dừng lại ở việc tái hiện kết quả, nhóm nghiên cứu tập trung vào việc **khai thác và lấp đầy khoảng trống nghiên cứu (Research Gap)** mà tác giả bài báo chưa thực hiện: So sánh hiệu năng của các mô hình LLMs mã nguồn mở, liệu có khả năng thay thế mô hình đóng GPT-4o (tốn phí) trong việc phân tích cảm xúc tài chính hay không?

Cụ thể, dự án tiến hành tiền xử lý dữ liệu và **Fine-tuning (Tinh chỉnh)** trên 3 kiến trúc Mô hình Ngôn ngữ Lớn (Large Language Models - LLMs) để đánh giá và so sánh hiệu năng:
1. **Llama**
2. **Qwen**
3. **DeepSeek**

Quá trình huấn luyện và đánh giá được thực hiện hoàn toàn trên môi trường Kaggle kết hợp với Big Data (Dask). Ứng dụng kiến trúc Big Data (Dask) để xây dựng hệ thống đánh giá mở rộng.


---

## 👥 Thành viên thực hiện
*(Chi tiết xem tại file `IS405.Q23 - DSThanhVien.txt`)*

| STT | Họ và Tên | Mã số sinh viên |

| 1 | Phạm Nhật Khoa | 23520753 |

| 2 | Nguyễn Gia Bảo | 23520121 |

---

## 🚀 Quy trình thực hiện (Pipeline)
Mã nguồn của dự án được tổ chức thành 4 luồng (Notebooks) độc lập và rõ ràng:

* **Luồng 1 (BigData 1):** Tiền xử lý dữ liệu đặc thù và Fine-tuning mô hình **Llama 3 8B**.
* **Luồng 2 (BigData 2):** Tiền xử lý dữ liệu đặc thù và Fine-tuning mô hình **Qwen 2.5 7B**.
* **Luồng 3 (BigData 3):** Tiền xử lý dữ liệu đặc thù và Fine-tuning mô hình **DeepSeek-R1 Distill Qwen 7B Reasoning Model**.
* **Luồng 4 (BigData 4 - Evaluation):** Viết script đánh giá, trích xuất metrics và so sánh hiệu suất chéo giữa 3 mô hình trên tập Validation/Test để rút ra kết luận khoa học.

---

## 📁 Cấu trúc kho chứa (Repository Structure)

📦 **IS405.Q23 - NoteBook thực hiện ở Kaggle/**

 ┣ 📜 `BigData 1 - Llama - Preprocessing - Finetunning.ipynb`
 
 ┣ 📜 `BigData 2 - Qwen - Preprocessing - Finetunning.ipynb`
 
 ┣ 📜 `BigData 3 - DeepSeek - Preprocessing - Finetunning.ipynb`
 
 ┗ 📜 `BigData 4 - Evaluation.ipynb`

--

📦 **IS405.Q23 - Data lấy trực tiếp từ Github tác giả/**

 ┣ 📜 `train_set.csv`: Tập dữ liệu huấn luyện.
 
 ┣ 📜 `validation_set.csv`: Tập dữ liệu kiểm chứng trong quá trình Fine-tune.
 
 ┗ 📜 `test_set.csv`: Tập dữ liệu kiểm tra độc lập.

--

📦 **Tài liệu Bài báo gốc/**

 ┣ 📜 `Bài báo gốc.pdf`: Tài liệu nền tảng của dự án.
 
 ┣ 📜 `Dataset Kaggle.txt`: Link dẫn đến nguồn dữ liệu.
 
 ┗ 📜 `Github bài báo gốc.txt`: Nguồn tham khảo mã nguồn từ tác giả.

--

📄 **Báo cáo & Tài liệu đính kèm:**

 ┣ 📂 **IS405.Q23 - Report/**: Chứa file báo cáo đồ án chi tiết (Word & PDF).
 
 ┣ 📜 `IS405.Q23 - Slide.pptx`: Slide thuyết trình báo cáo.
 
 ┗ 📜 `IS405.Q23 - TomTatDeTai.pdf`: Bản tóm tắt nhanh mục tiêu và kết quả dự án.

---

## 🛠 Công cụ & Nền tảng sử dụng
- **Môi trường tính toán:** Kaggle (sử dụng GPU/TPU cho việc huấn luyện LLMs).
- **Ngôn ngữ:** Python.
- **Mô hình trọng tâm:** Llama, Qwen, DeepSeek.
- **Quản lý phiên bản:** Git & GitHub.
