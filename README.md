# Trợ Lý Kỹ Thuật — bản trải nghiệm công khai

Public release candidate: `3.0.1-pilot-rc.4` — `CANDIDATE`, chưa xuất bản.

Người dùng cuối chỉ cần trình duyệt. Không cần Python, Node, tài khoản GitHub hoặc phần mềm bổ sung.

## Ranh giới công khai

Repository phát hành dự kiến là **public toàn bộ**. GitHub Pages chỉ phục vụ branch `main`, folder `/docs`; các file ngoài `docs/` trong repository vẫn công khai.

Payload này cố ý chỉ có bảy file:

- `docs/index.html`
- `docs/bac-si.html`
- `docs/ban-hang.html`
- `docs/404.html`
- `README.md`
- `PUBLICATION_MANIFEST.sha256`
- `PUBLICATION_PROVENANCE.json`

Không có GitHub Actions, workflow, AI instruction, test, verifier, raw evidence, backend, analytics hoặc network request trong payload. Test/verifier chỉ nằm trong release packet local.

## Phản hồi pilot

Hai trang theo vai trò có nút **Sổ tạm (n)** luôn nhìn thấy. Người dùng có thể mở sổ, xem phản hồi, chép toàn bộ, tải file `.txt` hoặc bôi đen nội dung thủ công bất cứ lúc nào, kể cả khi chưa hoàn thành bài hoặc đã chọn dừng.

Mặc định phiếu `FEEDBACK_PACKET/1.0` xuất không kèm môi trường: `environment_consent=false` và `environment_raw=null`. Người dùng có lựa chọn ngang hàng để tự nguyện kèm phần môi trường thô đang được hiển thị. Việc từ chối không làm mất quyền chép hoặc tải.

Trang **không tự gửi và không tự lưu bền**, không có backend hay kết nối mạng. Mỗi phiếu ghi rõ `sent=false` và `received=false`. Người dùng phải quay lại cuộc trò chuyện nơi nhận được link và tự dán phiếu phản hồi. Mốc xử lý 48 giờ chỉ bắt đầu sau khi nơi nhận thật sự nhận phiếu và xác nhận việc nhận.

## An toàn

Không đưa dữ liệu bệnh nhân/khách hàng, thông tin định danh, raw chat, log, evidence nội bộ, policy, secret, token hoặc credential vào repository này.

Namespace đã được người quyết định chọn ở mức ứng viên là `tro-ly-ky-thuat`; repository dự kiến là `tro-ly-trai-nghiem`. Availability, ownership và trạng thái GitHub vẫn là `CURRENT_RUNTIME_UNVERIFIED`. Payload này không tạo hay xác nhận Organization/repository.
