# Có gì bên trong folder ReactJS project

```
learn-reactjs/
README.md
node_modules/
package.json
public/
index.html # html template
favicon.ico
src/ # all resources should be inside this folder
App.css
App.js
App.test.js
index.css
index.js # entry point
logo.svg
```

LƯU Ý:

-   Không thay đổi tên file của `public/index.html` và `src/index.js`
-   ` index.js`: Đây là file đầu vào của project.
-   `index.html`: Đây là file template của project.App sẽ được mount vào node `root` trong template này.
-   `package.json`: Chứa thông tin các packages mà project sử dụng cũng như một vài config khác.
-   `node_modules`: Đây là folder rất nặng, rất lớn. Nó chứa tất cả các packages mình sử dụng, folder này chỉ có dưới local, không push lên `Github`, không có trên môi trường `production`.

🌐 Link tham khảo

-   Folder structure: https://create-react-app.dev/docs/folder-structure
-   Các scripts được setup sẵn: https://create-react-app.dev/docs/available-scripts
-   Các trình duyệt hỗ trợ: https://create-react-app.dev/docs/available-scripts
