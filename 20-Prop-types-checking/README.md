# Khai báo props và kiểm tra loại dữ liệu của props

## Props có thể dùng mà không cần định nghĩa

```js
import React from 'react'
function ColorBox(props) {
    const { color } = props
    return <div className="box" style={{ backgroundColor: color }}></div>
}
export default ColorBox
```

```js
import React from 'react'
import ColorBox from './components/ColorBox'
export default function App() {
    return (
        <section>
            <ColorBox color="red"></ColorBox>
            <ColorBox color="green"></ColorBox>
            <ColorBox color="blue"></ColorBox>
        </section>
    )
}
```

![result](./result.png)

## Nên dùng propTypes để kiểm tra đúng loại dữ liệu cho props

```js
import React from 'react'
import PropTypes from 'prop-types' // add package prop-types
function ColorBox(props) {
    const { color } = props
    return <div className="box" style={{ backgroundColor: color }}></div>
}
// declare all props used in this component
ColorBox.propTypes = {
    color: PropTypes.string.isRequired,
    rounded: PropTypes.bool,
}
// don't forget to set default value for non-required props
ColorBox.defaultProps = {
    rounded: true,
}
export default ColorBox
```
