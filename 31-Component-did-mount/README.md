# Component Life Cycles

Bảng life cycle rút gọn (nên dùng cái này)

![Component-Life-Cycles](./Component-Life-Cycles.png)

**componentDidMount()**

- Chạy đúng một lần lúc component khởi tạo
- Chạy sau render

- Được phép dùng.
- Khởi tạo dữ liệu cho component: `gọi API`, biến đổi dữ liệu, cập nhật state.
- Gửi tracking page view (GA, FacebookPixel, ...)

```js
class HomePage extends PureComponent {
  // 1: Chạy đầu tiên
  constructor(props) {
    super(props)

    this.state = {
      loading: true,
      productList: [],
  }
}

// 3: componentDidMount
async componentDidMount() {
  try {
    // Send GA page view tracking
    analytics.page('Home page')

    const productList = await productApi.getAll()
    this.setState({
      productList,
      loading: false,
    })
  } catch (error) {
    console.log('Failed to fetch product list: ', error)
    this.setState({loading: false})
  }
}

// 2: Render lần đầu
render() {
  const {loading, productList} = this.state
  if (loading) return <Loader />

  return <ProductList productList={productList}>
  }
}
```
