# 翻译 React 面试问题和答案 原文)
## [原文请见](https://github.com/sudheerj/reactjs-interview-questions)

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

4. ### What is the difference between Element and Component?

    An *Element* is a plain object describing what you want to appear on the screen in terms of the DOM nodes or other components. *Elements* can contain other *Elements* in their props. Creating a React element is cheap. Once an element is created, it is never mutated.

    The object representation of React Element would be as follows:

    ```javascript
    const element = React.createElement(
      'div',
      {id: 'login-btn'},
      'Login'
    )
    ```

    The above `React.createElement()` function returns an object:

    ```
    {
      type: 'div',
      props: {
        children: 'Login',
        id: 'login-btn'
      }
    }
    ```

    And finally it renders to the DOM using `ReactDOM.render()`:

    ```html
    <div id='login-btn'>Login</div>
    ```

    Whereas a **component** can be declared in several different ways. It can be a class with a `render()` method. Alternatively, in simple cases, it can be defined as a function. In either case, it takes props as an input, and returns an JSX tree as the output:

    ```javascript
    const Button = ({ onLogin }) =>
      <div id={'login-btn'} onClick={onLogin} />
    ```

    Then JSX gets transpiled to `React.createElement()` function tree:

    ```javascript
    const Button = ({ onLogin }) => React.createElement(
      'div',
      { id: 'login-btn', onClick: onLogin },
      'Login'
    )
    ```

5. ### How to create components in React?

    There are two possible ways to create a component.

    1. **Function Components:** This is the simplest way to create a component. Those are pure JavaScript functions that accept props object as first parameter and return React elements:

        ```jsx harmony
        function Greeting({ message }) {
          return <h1>{`Hello, ${message}`}</h1> 
        }
        ```

    2. **Class Components:** You can also use ES6 class to define a component. The above function component can be written as:

        ```jsx harmony
        class Greeting extends React.Component {
          render() {
            return <h1>{`Hello, ${this.props.message}`}</h1>
          }
        }
        ```

6. ### When to use a Class Component over a Function Component?

    If the component needs *state or lifecycle methods* then use class component otherwise use function component.

7. ### What are Pure Components?

    *`React.PureComponent`* is exactly the same as *`React.Component`* except that it handles the `shouldComponentUpdate()` method for you. When props or state changes, *PureComponent* will do a shallow comparison on both props and state. *Component* on the other hand won't compare current props and state to next out of the box. Thus, the component will re-render by default whenever `shouldComponentUpdate` is called.

8. ### What is state in React?

    *State* of a component is an object that holds some information that may change over the lifetime of the component. We should always try to make our state as simple as possible and minimize the number of stateful components. Let's create an user component with message state,


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

9. ### What are props in React?

    *Props* are inputs to components. They are single values or objects containing a set of values that are passed to components on creation using a naming convention similar to HTML-tag attributes. They are data passed down from a parent component to a child component.

    The primary purpose of props in React is to provide following component functionality:

    1. Pass custom data to your component.
    2. Trigger state changes.
    3. Use via `this.props.reactProp` inside component's `render()` method.

    For example, let us create an element with `reactProp` property:

    ```jsx harmony
    <Element reactProp={'1'} />
    ```

    This `reactProp` (or whatever you came up with) name then becomes a property attached to React's native props object which originally already exists on all components created using React library.

    ```
    props.reactProp
    ```

10. ### What is the difference between state and props?

    Both *props* and *state* are plain JavaScript objects. While both of them hold information that influences the output of render, they are different in their functionality with respect to component. Props get passed to the component similar to function parameters whereas state is managed within the component similar to variables declared within a function.