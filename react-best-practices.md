# React 最佳实践

## 事件处理
```JavaScript
// 正确，但不推荐
class App extends Component {

  constructor(props) {
    super(props);

    // 必须调用 bind() 绑定 this，否则 handleClick 中的 this 为 undefined
    this.handleClick = this.handleClick.bind(this);
  }

  handleClick() {
    console.log('this is', this);
  }

  render() {
    return <div onClick={this.handleClick} />;
  }
}

// 正确，但不推荐
class App extends Component {

  constructor(props) {
    super(props);

    // 必须调用 bind() 绑定 this，否则 handleClick 中的 this 为 undefined
    this.handleClick = this.handleClick.bind(this);
  }

  handleClick = function() {
    console.log('this is', this);
  }

  render() {
    return <div onClick={this.handleClick} />;
  }
}

// 推荐
class App extends Component {

  handleClick = () => {
    console.log('this is', this);
  }

  render() {
    return <div onClick={this.handleClick} />;
  }
}
```