# Component Life Cycles

Bảng life cycle rút gọn (nên dùng cái này)

![Component-Life-Cycles](./Component-Life-Cycles.png)

**componentWilUnMount()**

> Khi component bị huỷ bỏ: Khi chúng ta không render lên trên màn hình, khi chuyển trang.  
> Run đúng 1 lần trong 1 vòng đời của 1 component

- Được phép dùng.
- Clear timeout hoặc interval nếu có dùng.
- Reset dữ liệu trên redux nếu cần thiết.

```js
class Countdown extends PureComponent {
	constructor(props) {
		super(props)
		this.state = {
			currentSecond: 0,
		}
	}
	componentDidMount() {
		this.timer = setInterval(() => {
			this.setState((prevState) => ({
				currentSecond: prevState.currentSecond - 1,
			}))
		}, 1000)
	}
	componentWillUnmount() {
		if (this.timer) {
			clearInterval(this.timer)
		}
	}
	render() {
		const { currentSecond } = this.state
		return <p>{currentSecond}</p>
	}
}
```
