# ReactDOM.render()

> Render code ReactJS, những component ReactJS lên trên HTML DOM

```html
<!-- /public/index.html -->
<body>
    <noscript>You need to enable JavaScript to run this app.</noscript>
    <div id="root"></div>
</body>

```

```js
// /src/index.js
ReactDOM.render(
    <React.StrictMode>
        <App />
    </React.StrictMode>,
    document.getElementById('root'),
)
```

> NOTES:
> Theo kinh nghiệm thực tế thì hàm `ReactDOM.render()` chỉ sử dụng đúng một lần ở đây

🌐 Link tham khảo:

-   Render elements trong React: https://reactjs.org/docs/rendering-elements.html
