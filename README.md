# Nhịp Nhà

> Mỗi nhịp chạm, thêm một nhịp thương.

Web của đề tài nghiên cứu khoa học **"Bộ công cụ nhận diện sớm nguy cơ rạn nứt quan hệ cha mẹ – con tuổi vị thành niên trong môi trường nội trú và đề xuất giải pháp hỗ trợ"** – Trường THPT FPT Cần Thơ.

## Nội dung
- Phiếu 23 câu bản 3 (`cham-v2-ban3`), xưng hô theo người được chọn
- Chỉ số CRI, cờ an toàn, Bản đồ kết nối bốn thang
- Hành trình CHẠM 4 tuần theo bốn nhịp, thói quen mỗi ngày, mâm cơm, Bé Chạm

## Cấu trúc
| Tệp | Vai trò |
|---|---|
| `index.html` | Toàn bộ web (giao diện, nội dung, xử lý) |
| `favicon.svg` | Biểu tượng trên tab trình duyệt |
| `vercel.json` | Cấu hình bảo mật khi chạy trên Vercel |

Nội dung (câu hỏi, nhịp, hoạt động) nằm trong `index.html`, khối **DỮ LIỆU NỘI DUNG** ở đầu thẻ `<script>`.

## Dữ liệu
Mọi câu trả lời chỉ lưu trên trình duyệt của người dùng (localStorage), không gửi về máy chủ.

## Cập nhật
Sửa `index.html` trên GitHub → Commit → Vercel tự triển khai lại sau khoảng 1 phút.
