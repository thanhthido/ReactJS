# JSX syntax

> JSX syntax

-   Một ví dụ của JSX:

```js
const title = 'What is JSX?'
const jsx = (
    <section className="hero">
        <h1 className="hero__title">{title}</h1>
        <p className="hero__description">JSX stands for Javascript XML.</p>
        <ul style={{ fontSize: '14px' }}>
            <li>Simple to learn</li>
            <li>Ease to use</li>
            <li>Familiar with JS developer</li>
        </ul>
        <div className="form-group">
            <label htmlFor="fullName">Full name</label>
            <input type="text" id="fullName" />
        </div>
    </section>
)
```

-   Đoạn code JSX này, nếu viết bằng JS thì sẽ như thế này:

```js
"use strict";
const title = 'What is JSX?';
const jsx = React.createElement("section", { className: "hero" },
React.createElement("h1", { className: "hero__title" }, "What is JSX?"),
React.createElement("p", { className: "hero__description" }, "JSX stands
for Javascript XML."),
React.createElement("ul", { style: { fontSize: '14px' }},
React.createElement("li", null, "Simple to learn"),
React.createElement("li", null, "Ease to use"),
React.createElement("li", null, "Familiar with JS developer")
),
React.createElement("div", { className: "form-group" },
React.createElement("label", { htmlFor: "fullName" }, "Full name"),
React.createElement("input", { type: "text", id: "fullName" })
)
);
```

> NOTES:

-   Trình duyệt không hiểu cú pháp của JSX, nên cần biên dịch JSX sang JS trước khi sử dụng trên trình duyệt.
-   `class` và `for` là từ khóa trong Javascript, nên bạn không sử dụng trong JSX được.
-   Dùng `className` thay cho `class`
-   Dùng `htmlFor` thay cho `for`
-   Phải `import` React khi sử dụng JSX.

🌐 Link tham khảo:

-   Giới thiệu về JSX: https://reactjs.org/docs/introducing-jsx.html
-   Tìm hiểu sâu về JSX: https://reactjs.org/docs/jsx-in-depth.html
-   Babel JSX to JS: [click here to open it online](https://babeljs.io/en/repl#?browsers=defaults%2C%20not%20ie%2011%2C%20not%20ie_mob%2011&build=&builtIns=false&corejs=3.21&spec=false&loose=false&code_lz=Q&debug=false&forceAllTransforms=false&shippedProposals=false&circleciRepo=&evaluate=false&fileSize=false&timeTravel=false&sourceType=module&lineWrap=true&presets=env%2Creact%2Cstage-2&prettier=false&targets=&version=7.11.4&externalPlugins=&assumptions=%7B%7D)
