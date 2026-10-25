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
| `firestore.rules` | Quy tắc bảo mật Firestore cho đăng nhập Google (dán vào Firebase → Firestore → Rules) |

Nội dung (câu hỏi, nhịp, hoạt động) nằm trong `index.html`, khối **DỮ LIỆU NỘI DUNG** ở đầu thẻ `<script>`.

## Dữ liệu
Mặc định mọi dữ liệu chỉ lưu trên trình duyệt của người dùng (localStorage).

## Đăng nhập Google (giai đoạn 1, tùy chọn)
- Bật bằng cách dán `firebaseConfig` vào hằng `FIREBASE_CONFIG` trong `index.html`; để `null` thì chức năng đăng nhập ẩn.
- Khi đăng nhập, trạng thái được lưu vào Firestore tại `users/{uid}` (một chuỗi JSON). Ảnh khoảnh khắc không bao giờ được gửi lên; nhật ký chỉ gửi khi người dùng bật.
- `ALLOWED_EMAIL_DOMAIN` giới hạn email được đăng nhập (ví dụ `fpt.edu.vn`).

## Cập nhật
Sửa `index.html` trên GitHub → Commit → Vercel tự triển khai lại sau khoảng 1 phút.
