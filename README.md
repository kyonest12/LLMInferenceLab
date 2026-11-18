# LLM Inference Practice

Kho lưu trữ tài liệu và bài thực hành về LLM inference.

## Cấu trúc

- `Slide/`: slide và worksheet/lab gốc.
- `notebooks/`: notebook chạy bài thực hành trên Google Colab GPU.
- Các thư mục bài tập sẽ được thêm ở thư mục gốc theo từng chủ đề.

## Chạy bằng GPU Google Colab

1. Tạo một repository trống trên GitHub (không tạo sẵn README).
2. Từ máy local, thêm remote và đẩy nhánh hiện tại:

   ```powershell
   git remote add origin https://github.com/<USERNAME>/<REPOSITORY>.git
   git push -u origin main
   ```

3. Mở `notebooks/00_colab_setup.ipynb` trên GitHub, bấm **Open in Colab**.
4. Trong Colab, chọn **Runtime > Change runtime type > T4 GPU** (hoặc GPU khác).
5. Điền `REPO_URL`, rồi chạy lần lượt các cell. Cell kiểm tra sẽ in thông tin GPU bằng `nvidia-smi`.

Với repository private, không ghi token trực tiếp vào notebook. Hãy thêm secret tên `GITHUB_TOKEN` trong biểu tượng chìa khóa của Colab và cấp quyền notebook truy cập secret đó.

## Đồng bộ thay đổi

Trong Colab, commit và push như Git thông thường. Không commit model weights, dataset lớn, output, token hay khóa bí mật; các loại tệp phổ biến đã được loại trừ trong `.gitignore`.

