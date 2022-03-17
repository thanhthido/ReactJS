# Thêm SSH vào Github account

## Copy SSH public key vào clipboard

1. Mở Git bash
2. Chạy lệnh

```
clip < ~/.ssh/id_rsa.pub
```

Ý nghĩa là copy nội dung file ~/.ssh/id_rsa.pub vào clipboard.

## Vào Github, thêm mới một SSH key

1. Vào tài khoản Github --> Settings.
2. Vào mục SSH và GPG keys.
3. Thêm mới một SSH và paste cái SSH key vừa mới copy xong. Đặt title cho SSH để biết SSH key này là của máy tính nào.
4. Xác nhận thêm SSH key thành công bằng cách chạy lệnh

```
ssh -T git@github.com
```

Gõ `yes` khi được hỏi, và cuôi cùng nó ra dạng thế này là thành công.

```
Hi username! You've successfully authenticated, but GitHub does not
provide shell access.
```

🌐 Link tham khảo

-   https://docs.github.com/en/github/authenticating-to-github/adding-a-new-ssh-key-to-your-githubaccount
-   https://docs.github.com/en/github/authenticating-to-github/testing-your-ssh-connection
