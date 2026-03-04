# PROJECT INSTRUCTIONS — Hợp Đồng Dịch Vụ CNTT

## Mục đích
Dự án này quản lý việc soạn thảo và chỉnh sửa Hợp đồng Cung cấp Dịch vụ Công nghệ Thông tin theo pháp luật Việt Nam.

## Quy tắc làm việc

### 1. Khi edit file .docx
- **Luôn dùng Tracked Changes** (ghi `<w:ins>` / `<w:del>` trong XML) để user có thể review trong Word
- **Tạo diff report** sau mỗi lần edit — dạng artifact hoặc markdown, so sánh nội dung trước/sau
- **Cập nhật CHANGELOG.md** với entry mới, ghi rõ: ngày, nội dung sửa, trường bị ảnh hưởng, file output
- **Cập nhật checklist trạng thái** ở cuối CHANGELOG.md

### 2. Workflow mỗi lần sửa
```
1. User cung cấp nội dung cần sửa
2. Unpack file .docx mới nhất
3. Edit XML với Tracked Changes (w:ins/w:del, author="Claude")
4. Pack lại → validate → đây là file _tracked.docx
5. Accept all changes → tạo bản sạch _v{N}.docx
6. Tạo diff report cho user review
7. Cập nhật CHANGELOG.md
8. Output: file _tracked.docx + file _v{N}.docx (sạch) + diff report
```

### 2b. Quy tắc output 2 file
- `hop_dong_dich_vu_cntt_v{N}_tracked.docx` — bản có Tracked Changes để review trong Word
- `hop_dong_dich_vu_cntt_v{N}.docx` — bản sạch (đã accept), dùng làm base cho edit tiếp theo
- Trong cùng session: tiếp tục edit trên bản sạch, KHÔNG cần user update Project
- Khi kết thúc session: nhắc user upload bản sạch mới nhất + CHANGELOG.md vào Project Knowledge

### 3. Khi bắt đầu session mới
- Đọc CHANGELOG.md để nắm trạng thái hiện tại
- File .docx mới nhất là file có version number cao nhất (vd: v5 > v4)
- Tiếp tục đánh số edit từ số tiếp theo trong CHANGELOG
- Hỏi user muốn sửa gì tiếp

### 4. Quy ước đặt tên file
- File hợp đồng: `hop_dong_dich_vu_cntt_v{N}.docx`
- N tăng dần theo mỗi lần edit
- CHANGELOG.md: luôn giữ tên này, cập nhật nội dung

### 5. Căn cứ pháp lý chính
- Bộ luật Dân sự 2015 (91/2015/QH13)
- Luật Thương mại 2005 (36/2005/QH11)
- Luật CNTT — hợp nhất 65/VBHN-VPQH 2025
- Luật Giao dịch điện tử 2023 (20/2023/QH15)
- Luật ATTT mạng 2015, Luật An ninh mạng 2018
- NĐ 13/2023/NĐ-CP (bảo vệ dữ liệu cá nhân)
- NĐ 73/2019 sửa đổi bởi NĐ 82/2024/NĐ-CP
- TT 16/2024/TT-BTTTT (hiệu lực 14/02/2025)
