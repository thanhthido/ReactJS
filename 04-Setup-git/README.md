# Setup Git

## Tải và cài đặt Git

Mỗi hệ điều hành có cách cài đặt khác nhau https://git-scm.com/
![git](./git.png)

## Kiểm tra để xác nhận cài đặt thành công

1. Mở Git Bash
2. Chạy lệnh kiểm tra version của git

```
git --version
```

## Cấu hình chung cho git

Khi mới cài git, mình cần cấu hình để git biết:

-   Người dùng git tên gì?
-   Người dùng git có email là gì?
    Chạy 2 lệnh sau:

```
git config --global user.name "Your Name"
```

```
git config --global user.email "your-email@gmail.com"
```

> Lưu ý: Điền tên và email của bạn vào 2 câu lệnh trên nhé.

Sau khi chạy xong, dùng lệnh này để kiểm tra để cấu hình thành công chưa?

```
git config --list | grep user
```

Ý nghĩa câu lệnh này là xem danh sách git config mà có chứa chữ user 😉
