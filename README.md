# 🤖 AI Enterprise Document Chatbot (RAG)

## 📌 Giới thiệu
AI Enterprise Document Chatbot là một chatbot trí tuệ nhân tạo được xây dựng để **trả lời câu hỏi dựa trên tài liệu nội bộ của doanh nghiệp** như PDF, DOCX, TXT.  
Dự án áp dụng kiến trúc **Retrieval-Augmented Generation (RAG)**, giúp chatbot trả lời **đúng nội dung tài liệu**, tránh việc trả lời sai hoặc lan man.

👉 Phù hợp cho:
- Website doanh nghiệp
- Trung tâm đào tạo / e-learning
- Bộ phận HR
- Hỗ trợ khách hàng nội bộ

---

## 🎯 Bài toán doanh nghiệp
Doanh nghiệp thường gặp các vấn đề:
- Nhân viên mất thời gian tìm kiếm tài liệu
- Thông tin phân tán, khó tra cứu
- Nhân sự mới khó tiếp cận kiến thức nội bộ

➡️ **Giải pháp**:  
Xây dựng chatbot AI cho phép:
- Upload tài liệu nội bộ
- Đặt câu hỏi bằng ngôn ngữ tự nhiên
- Nhận câu trả lời chính xác dựa trên tài liệu đã cung cấp

---

## 🧠 Giải pháp & Kiến trúc
Hệ thống sử dụng mô hình **RAG** với các bước chính:

1. Người dùng upload tài liệu (PDF/DOCX/TXT)
2. Hệ thống:
   - Trích xuất văn bản
   - Chia nhỏ nội dung (chunking)
   - Chuyển văn bản thành vector embedding
3. Lưu embedding vào **Vector Database**
4. Khi người dùng đặt câu hỏi:
   - Truy xuất các đoạn văn liên quan
   - Kết hợp với LLM để sinh câu trả lời chính xác

---

## 🧱 Tech Stack
- **Backend**: Python, FastAPI
- **AI / NLP**:
  - Large Language Model (LLM API)
  - Embedding Model
- **Vector Database**: FAISS / ChromaDB
- **Frontend**: HTML đơn giản / Streamlit
- **Deployment**: Local / Render / Railway

---

## 📂 Cấu trúc thư mục
```text
ai-enterprise-chatbot/
│
├── app/
│   ├── main.py              # FastAPI entry point
│   ├── api.py               # API routes
│   ├── rag_pipeline.py      # RAG logic
│   ├── vector_store.py      # Vector DB handling
│   └── utils.py             # Helper functions
│
├── data/
│   └── documents/           # Uploaded documents
│
├── frontend/
│   └── index.html           # Simple UI
│
├── requirements.txt
├── README.md
└── .env
