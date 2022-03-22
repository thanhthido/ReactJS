# Render elements in reactjs

-   Render được chuỗi, số
-   Không render trực tiếp được các giá trị boolean trên màn hình
    > Có thể dùng render theo điều kiện. Trường hợp này chỉ có một thẻ cha, có thể dùng thẻ cha hoặc `Fragment`, hoặc thẻ trống
-   Không render được object trực tiếp lên màn hình, có thể render ra key

-   Mảng: dùng map duyệt qua

```js
import React from 'react'
import logo from './logo.svg'
import './App.css'

function App() {
    const name = 'Thi'
    const age = 22
    const isFemale = true
    const student = {
        name: 'Easy Frontend',
    }
    const colorList = ['red', 'green', 'blue']

    return (
        <div className="App">
            <header className="App-header">
                <img src={logo} className="App-logo" alt="logo" />
                <p>Thanh Thi</p>

                <p>
                    Xin chao {name} - {age} - {isFemale ? 'Female' : 'Male'}
                </p>

                {isFemale ? <p>Female</p> : <p>Male</p>}

                {isFemale && <p>Female</p>}
                {!isFemale && <p>Male</p>}

                {isFemale && (
                    <div>
                        <p>Female 1</p>
                        <p>Female 2</p>
                        <p>Female 3</p>
                    </div> // render ra cả thẻ div
                )}

                {isFemale && (
                    <React.Fragment>
                        <p>Female 4</p>
                        <p>Female 5</p>
                        <p>Female 6</p>
                    </React.Fragment> // render 3 thẻ p
                )}

                {isFemale && (
                    <>
                        <p>Female 7</p>
                        <p>Female 8</p>
                        <p>Female 9</p>
                    </> // render 3 thẻ p
                )}

                <p>{student.name}</p>

                <ul>
                    {colorList.map((color) => (
                        <li key={color} style={{ color }}>
                            {color}
                        </li>
                    ))}
                </ul>
            </header>
        </div>
    )
}

export default App
```
