# React 最佳实践

## 事件处理

使用 `handleClick = () => { ... }` 语法定义事件处理函数
```JavaScript
// bad
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
    return <button onClick={this.handleClick} />;
  }
}

// bad
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
    return <button onClick={this.handleClick} />;
  }
}

// good
class App extends Component {

  handleClick() {
    console.log('this is', this);
  }

  render() {
    return <button onClick={e => this.handleClick(e)} />;
  }
}

// best
class App extends Component {

  handleClick = () => {
    console.log('this is', this);
  }

  render() {
    return <button onClick={this.handleClick} />;
  }
}
```