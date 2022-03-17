# Push code lên Github repo

## 1. Tạo một Github repository

Vào github cá nhân, tạo một repository mới. Nhớ tạo ra một empty repo, không có README, không có LICENSE.  
Điều này tránh được việc conflict khi push lần đầu từ local lên git remote.

## 2. Thêm git remote vào local project

```
git remote add origin git@github.com:paulnguyen-mn/temp.git
```

## 3. Đẩy code lên git remote lần đầu

Stage code changes

```
git add .
```

Commit code

```
git commit -m "Describe your changes briefly"
```

Tham khảo về cách viết commit message: https://chris.beams.io/posts/git-commit/  
Push code

```
git branch -M main
git push -u origin main
```

🌐 Link tham khảo
https://docs.github.com/en/github/using-git/pushing-commits-to-a-remote-repository
