<<<<<<< HEAD
# 翻译 React 面试问题和答案
## [原文请点击这里](https://github.com/sudheerj/reactjs-interview-questions)
=======
# 翻译 React 面试问题和答案 原文)
## [原文请见](https://github.com/sudheerj/reactjs-interview-questions)
>>>>>>> 0f94bfdc75d7cfc3919cf8f9b6ee631ff078cea8

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

<<<<<<< HEAD
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
=======
## Core React

1. ### What is React?

    React is an **open-source frontend JavaScript library** which is used for building user interfaces especially for single page applications. It is used for handling view layer for web and mobile apps. React was created by Jordan Walke, a software engineer working for Facebook. React was first deployed on Facebook's News Feed in 2011 and on Instagram in 2012.

2. ### What are the major features of React?

    The major features of React are:

    * It uses **VirtualDOM** instead RealDOM considering that RealDOM manipulations are expensive.
    * Supports **server-side rendering**.
    * Follows *Unidirectional** data flow or data binding.
    * Uses **reusable/composable** UI components to develop the view.

3. ### What is JSX?

    *JSX* is a XML-like syntax extension to ECMAScript (the acronym stands for *JavaScript XML*). Basically it just provides syntactic sugar for the `React.createElement()` function, giving us expressiveness of JavaScript along with HTML like template syntax.

    In the example below text inside `<h1>` tag return as JavaScript function to the render function.
>>>>>>> 0f94bfdc75d7cfc3919cf8f9b6ee631ff078cea8

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

<<<<<<< HEAD
4. ### 元素和组件有什么区别?

    一个 *Element* 描述 DOM 节点和其他组件如何按你想要的出现在屏幕上的纯对象。 *Elements* 可以包含其他的 *Elements* 在它们的props 中. 创建一个React 元素很方便. 一旦创建了一个元素，它不再会发生改变。

    React Element的对象表示如下：:
=======
4. ### What is the difference between Element and Component?

    An *Element* is a plain object describing what you want to appear on the screen in terms of the DOM nodes or other components. *Elements* can contain other *Elements* in their props. Creating a React element is cheap. Once an element is created, it is never mutated.

    The object representation of React Element would be as follows:
>>>>>>> 0f94bfdc75d7cfc3919cf8f9b6ee631ff078cea8

    ```javascript
    const element = React.createElement(
      'div',
      {id: 'login-btn'},
      'Login'
    )
    ```

<<<<<<< HEAD
    上面 `React.createElement()` 函数返回一个对象:
=======
    The above `React.createElement()` function returns an object:
>>>>>>> 0f94bfdc75d7cfc3919cf8f9b6ee631ff078cea8

    ```
    {
      type: 'div',
      props: {
        children: 'Login',
        id: 'login-btn'
      }
    }
    ```

<<<<<<< HEAD
    最后它使用 `ReactDOM.render()` 函数去渲染DOM:
=======
    And finally it renders to the DOM using `ReactDOM.render()`:
>>>>>>> 0f94bfdc75d7cfc3919cf8f9b6ee631ff078cea8

    ```html
    <div id='login-btn'>Login</div>
    ```

<<<<<<< HEAD
    而 **组件** 可以用不同的方式声明，它可以使一个用 `render()` 方法的类。 或者简单的定义为一个函数. 无论怎样他都会接受传入的props, 并返回一个 JSX 树:
=======
    Whereas a **component** can be declared in several different ways. It can be a class with a `render()` method. Alternatively, in simple cases, it can be defined as a function. In either case, it takes props as an input, and returns an JSX tree as the output:
>>>>>>> 0f94bfdc75d7cfc3919cf8f9b6ee631ff078cea8

    ```javascript
    const Button = ({ onLogin }) =>
      <div id={'login-btn'} onClick={onLogin} />
    ```

<<<<<<< HEAD
    然后JSX转化为 `React.createElement()` 函数树:
=======
    Then JSX gets transpiled to `React.createElement()` function tree:
>>>>>>> 0f94bfdc75d7cfc3919cf8f9b6ee631ff078cea8

    ```javascript
    const Button = ({ onLogin }) => React.createElement(
      'div',
      { id: 'login-btn', onClick: onLogin },
      'Login'
    )
    ```

<<<<<<< HEAD
5. ### 如何在React中创建组件?

    有两种可能的方法来创建组件.

    1. **Function Components:** 这是创建组件的最简单方法. 这些是纯JavaScript函数，它们接受props对象作为第一个参数并返回React元素：

        ```jsx harmony
        function Greeting({ message }) {
          return <h1>{`Hello, ${message}`}</h1>
        }
        ```

    2. **Class Components:** 您还可以使用ES6类来定义组件。上面的函数组件可以写成：
=======
5. ### How to create components in React?

    There are two possible ways to create a component.

    1. **Function Components:** This is the simplest way to create a component. Those are pure JavaScript functions that accept props object as first parameter and return React elements:

        ```jsx harmony
        function Greeting({ message }) {
          return <h1>{`Hello, ${message}`}</h1> 
        }
        ```

    2. **Class Components:** You can also use ES6 class to define a component. The above function component can be written as:
>>>>>>> 0f94bfdc75d7cfc3919cf8f9b6ee631ff078cea8

        ```jsx harmony
        class Greeting extends React.Component {
          render() {
            return <h1>{`Hello, ${this.props.message}`}</h1>
          }
        }
        ```

<<<<<<< HEAD
6. ### 何时使用Class Component 替函 Function Component?

    如果组件需要 *内部状态（state）或生命周期方法 * 则使用类组件，否则使用函数组件。

7. ### 什么是 Pure Components?

    *`React.PureComponent`* 与 *`React.Component`* 极为相似， 除了处理了 `shouldComponentUpdate()` 方法，当 props 或state 改变, *PureComponent* 将会浅层比较 state 和 props。另一方面， *Component*  在输出的时候不会比较porps 和 state, 因此，无论何时 `shouldComponentUpdate` 被调用组件总会重新渲染。

8. ### What is state in React?

    组件的 *State（状态）* 是一个对象，在组件的整个生命周期中保存一些可能改变的信息。 组件状态应该尽可能的简单，尽可能使有状态组件数量最小。 让我们创建一个具有消息状态的用户组件，
=======
6. ### When to use a Class Component over a Function Component?

    If the component needs *state or lifecycle methods* then use class component otherwise use function component.

7. ### What are Pure Components?

    *`React.PureComponent`* is exactly the same as *`React.Component`* except that it handles the `shouldComponentUpdate()` method for you. When props or state changes, *PureComponent* will do a shallow comparison on both props and state. *Component* on the other hand won't compare current props and state to next out of the box. Thus, the component will re-render by default whenever `shouldComponentUpdate` is called.

8. ### What is state in React?

    *State* of a component is an object that holds some information that may change over the lifetime of the component. We should always try to make our state as simple as possible and minimize the number of stateful components. Let's create an user component with message state,
>>>>>>> 0f94bfdc75d7cfc3919cf8f9b6ee631ff078cea8


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

<<<<<<< HEAD
9. ### React 中 porps 是什么?

    *Props* 是组件传入的属性. 它们是单个值或包含一组值的对象，创建时使用类似于HTML标记属性的命名约定传入到组件中.它们是从父组件传递到子组件的数据。

    React中props的主要目的是提供以下组件功能：

    1. 将自定义数据传递给您的组件。
    2. 触发状态更改。
    3. 通过 `this.props.reactProp` 在组件 `render()` 方法中使用.

    例如，让我们创建一个具有reactProp属性的元素：
=======
9. ### What are props in React?

    *Props* are inputs to components. They are single values or objects containing a set of values that are passed to components on creation using a naming convention similar to HTML-tag attributes. They are data passed down from a parent component to a child component.

    The primary purpose of props in React is to provide following component functionality:

    1. Pass custom data to your component.
    2. Trigger state changes.
    3. Use via `this.props.reactProp` inside component's `render()` method.

    For example, let us create an element with `reactProp` property:
>>>>>>> 0f94bfdc75d7cfc3919cf8f9b6ee631ff078cea8

    ```jsx harmony
    <Element reactProp={'1'} />
    ```

<<<<<<< HEAD
    `reactProp` (无论起任何名字) 会被附加到 React 组件 props 属性中，所有由 React 库创建出来的组件都会有porps 属性。
=======
    This `reactProp` (or whatever you came up with) name then becomes a property attached to React's native props object which originally already exists on all components created using React library.
>>>>>>> 0f94bfdc75d7cfc3919cf8f9b6ee631ff078cea8

    ```
    props.reactProp
    ```

<<<<<<< HEAD
10. ### state 和 porps 的区别??

    *props* 和 *state* 都是 javascript 纯对象. 他们都保存影响渲染的数据, 但它们在组件方面的功能却不同。 Props 类似于函数参数传递给组件， 而 state 类似于函数中声明的变量在组件内部中管理。
=======
10. ### What is the difference between state and props?

    Both *props* and *state* are plain JavaScript objects. While both of them hold information that influences the output of render, they are different in their functionality with respect to component. Props get passed to the component similar to function parameters whereas state is managed within the component similar to variables declared within a function.
>>>>>>> 0f94bfdc75d7cfc3919cf8f9b6ee631ff078cea8
