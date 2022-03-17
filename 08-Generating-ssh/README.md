# Tạo SSH key dưới local

## Tạo SSH key

1. Mở Git bash
2. Chạy lệnh

```
ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
```

Nhớ thay đổi your_email@example.com thành email của các bạn.

-   Khi được hỏi lưu ở file nào? Nhấn enter để sử dụng vị trí mặc định.
-   Khi được hỏi nhập passphrase cho SSH thì nhấn enter, tức không dùng passphrase.
-   Khi được hỏi nhập lại passphrase, tiếp tục nhấn enter

> Passphrase được dùng để encrypt cái private key trên máy tính của mình. Mà encrypt thì khi sử dụng phải decrypt đó, nên để tránh rườm rà, coi như máy tính mình an toàn, khỏi encrypt.

3. Kiểm tra đã tạo SSH key thành công

```
cat ~/.ssh/id_rsa.pub
```

Ý nghĩa là log ra nội dung của file `id_rsa.pub` nằm ở folder `~/.ssh.` Dấu `~` là folder home của user trên máy tính.  
Nếu chạy lệnh trên có log ra nội dung, tức là đã thành công 🎉
