# useState() lab - TodoList List and Remove

## Bài tập 2: TodoList - list and remove

Cho danh sách todos như bên dưới.

```js
const todoList = [
	{ id: 1, title: 'I love Easy Frontend! 😍 ' },
	{ id: 2, title: 'We love Easy Frontend! 🥰 ' },
	{ id: 3, title: 'They love Easy Frontend! 🚀 ' },
]
```

1. Render danh sách todos với dữ liệu được truyền từ component cha
2. Khi click lên một item thì remove item đó khỏi danh sách

---

## Phân tích

App

- Props: N/A
- State: `todoList`
- Handler: `handleTodoClick` - Remove todo ra khỏi state `todoList`
- Render: `<TodoList todos={todoList} onTodoClick={handleTodoClick} />`

TodoList

- Props:
  - `todos`: danh sách todos
  - `onTodoClick`: hàm sẽ được gọi khi một todo được click
- State: N/A
- Render: ul > li > todo.title
- Handle todo onClick: gọi hàm `props.onTodoClick()`

```
Cây component

App
|__ TodoList
```
