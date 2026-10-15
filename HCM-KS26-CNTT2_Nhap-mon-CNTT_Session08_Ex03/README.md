# Bài 3 : Onboarding lập trình viên mới

## Cài đặt VS Code
Phần giải thích là văn bản thường, còn *câu lệnh cần gõ* nằm trong khung code.

## Các bước

1. **Download** bản cài đặt từ `code.visualstudio.com`.
2. **Install** theo hướng dẫn của trình cài đặt.
3. **Open Terminal** bằng ``Ctrl + ` ``.
4. **(Tùy chọn) Add to PATH** để mở VS Code từ mọi thư mục.
5. **Verify** bằng lệnh:

```bash
 --version
```

>  Nếu lệnh `code` không nhận diện, hãy khởi động lại Terminal hoặc máy.

## Kiểm tra bằng Python

```python
import subprocess

try:
    result = subprocess.run(["code", "--version"], capture_output=True, text=True, check=True)
    version = result.stdout.splitlines()[0]
    print(f"VS Code phiên bản: {version}")
except (FileNotFoundError, subprocess.CalledProcessError):
    print("Chưa nhận diện được lệnh code.")
```

## So sánh công cụ

| Tiêu chí | StackEdit | VS Code |
| :--- | :---: | :---: |
| Cài đặt | Không cần, chạy trên trình duyệt | Cần cài đặt |
| Xem trước Markdown | Song song, ngay lập tức | Markdown Preview |
| Phạm vi | Soạn Markdown | Lập trình nhiều ngôn ngữ |

## Tiến độ

- [x] Download
- [x] Install
- [ ] Verify bằng `code --version`

Để hiển thị nguyên dấu \* hoặc \#, thêm dấu \\ phía trước.

---

## Báo cáo I/O

- **Input:** văn bản thô trong file `.md`, gồm chữ và ký hiệu như `#`, `**`, `-`.
- **Output:** giao diện render trên StackEdit, nơi Parser biến ký hiệu thành tiêu đề, bảng, checkbox và code có màu.
