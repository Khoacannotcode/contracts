# Hợp Đồng Cung Cấp Dịch Vụ CNTT

## Cấu trúc repo

| File | Mô tả |
|---|---|
| `hop_dong_dich_vu_cntt.docx` | Bản sạch mới nhất (accepted all changes) |
| `hop_dong_dich_vu_cntt_tracked.docx` | Bản có tracked changes — mở trong Word để review |
| `hop_dong_dich_vu_cntt.md` | Text export — readable trên GitHub, dùng cho git diff |
| `STATUS.md` | Checklist trường còn trống |

## Workflow
- Mỗi lần Claude edit → commit + push tự động
- Xem diff nội dung: so sánh `hop_dong_dich_vu_cntt.md` giữa các commit
- Review chi tiết: mở `_tracked.docx` trong Word
- Revert: yêu cầu Claude revert commit
