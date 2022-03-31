# React hooks 1 - Setup project

## Chuẩn bị phần mềm

- Cài đặt `NodeJS`
- Cài đặt `VSCode`

## Khởi tạo ReactJS project với create-react-app

- Điều kiện: phải cài đặt xong NodeJS vs VSCode trước.

1. Tạo một folder tên `react js` trống rỗng.
2. Mở VSCode. File --> Open folder --> Chọn folder `react js`
3. Mở terminal trong VSCode.
4. Chạy lệnh `npx create-react-app react-hooks-basic`

## Khắc phục lỗi Execution policy bên Windows

1. Mở Powershell với quyền admin.
2. Chạy lệnh này: `Set-ExecutionPolicy -ExecutionPolicy emoteSigned`
3. Chọn Yes to All
4. DONE
   --> Vào VSCode thử lại.

## Cài đặt extensions cho VSCode

- Bật Auto format on save.
- Cài `ReactJS Code Snippets`
- Cài `SCSS Formatter`

## Chạy thử project

1. Mở folder `react-hooks-basic`
2. Chạy lệnh `npm start`
3. Dừng server `Ctrl + C`
4. Cài thêm `node-sass` để sử dụng scss styles. Lệnh: `npm i --save-dev node-sass`
5. Giới thiệu về project:

- Folder `public`: chứa static files như sitemap.xml, robots.txt, images, ...
- Folder `src`: Tất cả code sẽ viết trong này.
- File `public/index.html`:
  - File `src/index.js`: Entry point của react app.
  - File s`rc/App.js`: Component chính của react.

6. Sửa styles và nội dung: "Welcome to React Hooks"
7. READY to ROCKS!!! 🚀
