# useState() lab - TodoList - add new todo

## Bài tập 3: TodoList - add new todo

Tạo một `form` đơn giản như sau:

- Chứa một thẻ `input` để user có thể nhập dữ liệu
- Khi `form submit`:
  - Chặn browser reload.
  - Tạo thêm một todo mới vào danh sách.

---

## Phân tích

TodoForm

- Props:
  - `onSubmit`: hàm được gọi khi form được submit.
- State: `value` ( giữ giá trị thẻ i input)
- Render: `form > input`
- Handle submit: gọi hàm `props.onSubmit()`

```
1. TodoForm quản lý nhập liệu
2. Khi submit, TodoForm báo component cha App, đây là dữ liệu user submit
3. App: Lấy dữ liệu, cập nhật state todoList.
4. TodoList: thấy todoList mới, re-render lại.
```

```
Cây component

App
|__ TodoForm
|__ TodoList
```
