# 翻译 React 面试问题和答案
## [原文请点击这里](https://github.com/sudheerj/reactjs-interview-questions)

> 如果你喜欢这个项目 请给一个Star,表示非常的感谢.

### 内容表格

| 序号. | 问题 |
| --- | --------- |
|   | **React 核心** |
|1  | [什么是React?](#what-is-react) |
|2  | [React 主要特点是什么?](#what-are-the-major-features-of-react) |
|3  | [什么是JSX？](#what-is-jsx) |
|4  | [元素和组件有什么区别？](#what-is-the-difference-between-element-and-component) |
|5  | [如何在React中创建组件？](#how-to-create-components-in-react) |
|6  | [何时使用Class Component 替函 Function Component?](#when-to-use-a-class-component-over-a-function-component) |
|7  | [什么是 Pure Components?](#what-are-pure-components) |
|8  | [React 中 state 是什么?](#what-is-state-in-react) |
|9  | [React 中 porps 是什么?](#what-are-props-in-react) |
|10 | [state 和 porps 的区别?](#what-is-the-difference-between-state-and-props) |

## React 核心

1. ### 什么是React?

    React 是一个 **开源前端JavaScript库** 用于构建用户界面， 尤其是单页面应用程序。他被用于处理 web 和 移动 app 的视图层。 React 是由Facebook 的软件工程师 Jordan Walke 所创立的. React于2011年首次部署在Facebook的News Feed上，2012年首次部署在Instagram上。

2. ### React 主要特点是什么？

    React 主要特点是:

    * 考虑到RealDOM操作很昂贵，它使用 **VirtualDOM** 而不是 RealDOM 。
    * 支持 **服务器端渲染**。
    * 遵循 *单向** 数据流或数据绑定。
    * 使用 **可重用/可组合的** UI UI组件来开发视图。

3. ### 什么是JSX?

    *JSX* 是 ECMAScript 的类似XML的语法扩展 (是 *JavaScript XML* 首字母缩略词). 基本上它只是为 `React.createElement()` 函数提供语法糖, 给我们提供一种 JavaScript 和 HTML 在一起使用的类模板.

    In the example below text inside `<h1>` tag return as JavaScript function to the render function.
    在下面的示例中，`<h1>`标签和其中的文本，作为 JavaScript 函数 在render 函数中被返回。

    ```jsx harmony
    class App extends React.Component {
      render() {
        return(
          <div>
            <h1>{'Welcome to React world!'}</h1>
          </div>
        )
      }
    }
    ```

4. ### 元素和组件有什么区别?

    一个 *Element* 描述 DOM 节点和其他组件如何按你想要的出现在屏幕上的纯对象。 *Elements* 可以包含其他的 *Elements* 在它们的props 中. 创建一个React 元素很方便. 一旦创建了一个元素，它不再会发生改变。

    React Element的对象表示如下：:

    ```javascript
    const element = React.createElement(
      'div',
      {id: 'login-btn'},
      'Login'
    )
    ```

    上面 `React.createElement()` 函数返回一个对象:

    ```
    {
      type: 'div',
      props: {
        children: 'Login',
        id: 'login-btn'
      }
    }
    ```

    最后它使用 `ReactDOM.render()` 函数去渲染DOM:

    ```html
    <div id='login-btn'>Login</div>
    ```

    而 **组件** 可以用不同的方式声明，它可以使一个用 `render()` 方法的类。 或者简单的定义为一个函数. 无论怎样他都会接受传入的props, 并返回一个 JSX 树:

    ```javascript
    const Button = ({ onLogin }) =>
      <div id={'login-btn'} onClick={onLogin} />
    ```

    然后JSX转化为 `React.createElement()` 函数树:

    ```javascript
    const Button = ({ onLogin }) => React.createElement(
      'div',
      { id: 'login-btn', onClick: onLogin },
      'Login'
    )
    ```

5. ### 如何在React中创建组件?

    有两种可能的方法来创建组件.

    1. **Function Components:** 这是创建组件的最简单方法. 这些是纯JavaScript函数，它们接受props对象作为第一个参数并返回React元素：

        ```jsx harmony
        function Greeting({ message }) {
          return <h1>{`Hello, ${message}`}</h1>
        }
        ```

    2. **Class Components:** 您还可以使用ES6类来定义组件。上面的函数组件可以写成：

        ```jsx harmony
        class Greeting extends React.Component {
          render() {
            return <h1>{`Hello, ${this.props.message}`}</h1>
          }
        }
        ```

6. ### 何时使用Class Component 替函 Function Component?

    如果组件需要 *内部状态（state）或生命周期方法 * 则使用类组件，否则使用函数组件。

7. ### 什么是 Pure Components?

    *`React.PureComponent`* 与 *`React.Component`* 极为相似， 除了处理了 `shouldComponentUpdate()` 方法，当 props 或state 改变, *PureComponent* 将会浅层比较 state 和 props。另一方面， *Component*  在输出的时候不会比较porps 和 state, 因此，无论何时 `shouldComponentUpdate` 被调用组件总会重新渲染。

8. ### What is state in React?

    组件的 *State（状态）* 是一个对象，在组件的整个生命周期中保存一些可能改变的信息。 组件状态应该尽可能的简单，尽可能使有状态组件数量最小。 让我们创建一个具有消息状态的用户组件，


    ```jsx harmony
    class User extends React.Component {
      constructor(props) {
        super(props)

        this.state = {
          message: 'Welcome to React world'
        }
      }

      render() {
        return (
          <div>
            <h1>{this.state.message}</h1>
          </div>
        )
      }
    }
    ```

    ![state](images/state.jpg)

9. ### React 中 porps 是什么?

    *Props* 是组件传入的属性. 它们是单个值或包含一组值的对象，创建时使用类似于HTML标记属性的命名约定传入到组件中.它们是从父组件传递到子组件的数据。

    React中props的主要目的是提供以下组件功能：

    1. 将自定义数据传递给您的组件。
    2. 触发状态更改。
    3. 通过 `this.props.reactProp` 在组件 `render()` 方法中使用.

    例如，让我们创建一个具有reactProp属性的元素：

    ```jsx harmony
    <Element reactProp={'1'} />
    ```

    `reactProp` (无论起任何名字) 会被附加到 React 组件 props 属性中，所有由 React 库创建出来的组件都会有porps 属性。

    ```
    props.reactProp
    ```

10. ### state 和 porps 的区别??

    *props* 和 *state* 都是 javascript 纯对象. 他们都保存影响渲染的数据, 但它们在组件方面的功能却不同。 Props 类似于函数参数传递给组件， 而 state 类似于函数中声明的变量在组件内部中管理。