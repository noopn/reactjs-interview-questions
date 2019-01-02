# 翻译 React 面试问题和答案
## [原文请点击这里](https://github.com/sudheerj/reactjs-interview-questions)

> 如果你喜欢这个项目 请给一个Star,表示非常的感谢.

### 内容表格

| 序号. | 问题 |
| --- | --------- |
|   | **React 核心** |
|1  | [什么是React？](#什么是React) |
|2  | [React主要特点是什么？](#React主要特点是什么) |
|3  | [什么是JSX？](#什么是JSX) |
|4  | [元素和组件有什么区别？](#元素和组件有什么区别) |
|5  | [如何在React中创建组件？](#如何在React中创建组件) |
|6  | [何时使用ClassComponent替函FunctionComponent？](#何时使用ClassComponent替函FunctionComponent) |
|7  | [什么是PureComponents？](#什么是PureComponents) |
|8  | [React中state是什么？](#React中state是什么) |
|9  | [React中porps是什么？](#React中porps是什么) |
|10 | [state和porps的区别？](#state和porps的区别) |
|11 | [为什么不应该直接更新state？](#为什么不应该直接更新state) |
|12 | [回调函数作为setState()参数的目的是什么？](#回调函数作为setState()参数的目的是什么)
|13 | [HTML和React事件绑定的区别是什么？](#HTML和React事件绑定的区别是什么) |
|14 | [如何在JSX回调中绑定方法或事件绑定？](#如何在JSX回调中绑定方法或事件绑定) |
|15 | [如何向事件绑定或回调中传递一个参数？](#如何向事件绑定或回调中传递一个参数) |
|16 | [React中合成事件是什么？](#React中合成事件是什么) |
|17 | [什么是内联条件表达式？](#什么是内联条件表达式) |
|18 | [什么是key属性，在数组中使用它们的好处是什么？](#什么是key属性在数组中使用它们的好处是什么) |
|19 | [refs有什么用？](#refs有什么用) |
|20 | [如何创建refs？](#如何创建refs) |  
|21 | [什么是 forward refs？](#什么是forward-refs) |
|22 | [在refs回调函数和findDOMNode()应该首选哪一个？](#在refs回调函数和findDOMNode()应该首选哪一个) |
|23 | [为什么曾经refs是String类型？](#为什么曾经refs是String类型) |
|24 | [什么是虚拟DOM？](#什么是虚拟DOM) |
|25 | [虚拟DOM是如何工作的？](#虚拟DOM是如何工作的) |
|26 | [Shadow DOM 和 Virtual DOM 的区别？](#Shadow-DOM和Virtual-DOM的区别) |
|27 | [React Fiber 是什么？](#React-Fiber是什么) |
|28 | [React Fiber 出现的主要目的是什么？](#ReactFiber出现的主要目的是什么) |
|29 | [什么是受控组件？](#什么是受控组件) |
|30 | [什么是非受控组件？](#什么是非受控组件) |
|31 | [createElement 和 cloneElement 的区别](#createElement和cloneElement的区别) |
|32 | [React 中 State 提升是什么？](#React中State提升是什么) |
|33 | [组件生命周期的不同阶段是什么？](#组件生命周期的不同阶段是什么) |
|34 | [React 生命周期方法是什么？](#React生命周期方法是什么) |
|35 | [什么是高阶组件？](#什么是高阶组件) |
|36 | [如何创建高阶组件的 props 代理？](#如何创建高阶组件的props代理) |
|37 | [什么是 context？](#什么是context) |
|38 | [什么是 children porp？](#什么是childrenporp) |
|39 | [在 react 中怎么写注释？](#在react中怎么写注释) |
|40 | [使用带 props 参数的 super 构造函数的目的是什么？](#使用带props参数的super构造函数的目的是什么) |
|41 | [什么是 reconciliation？](#什么是reconciliation) |
|42 | [如何使用动态 key 值设置state？](#如何使用动态key值设置state) |
|43 | [每次渲染时每次调用函数的常见错误是什么？](#每次渲染时每次调用函数的常见错误是什么) |
|44 | [为什么必须大写组件名称？](#为什么必须大写组件名称) |
|45 | [React 为什么使用 `className` 代替 `class` 属性？](#React为什么使用className代替class属性) |
|46 | [什么是 fragments？](#什么是fragments) |
|47 | [为什么 fragments 比 div 容器好？](#为什么fragments比div容器好) |
|48 | [React 中 portals 是什么？](#React中portals是什么) |
|49 | [什么是无状态组件？](#什么是无状态组件) |
|50 | [什么是有状态组件？](#什么是有状态组件) |
|51 | [React 中如何对 props 进行验证？](#React中如何对props进行验证) |
|52 | [React的优点是什么？](#React的优点是什么) |
|53 | [React 的局限是什么？](#React的局限是什么) |
|54 | [React V16 中错误边界是什么](#ReactV16中错误边界是什么) |
|55 | [React v15中如何处理错误边界？](#Reactv15中如何处理错误边界) |
|56 | [什么是 static 类型检查的推荐方法？](#什么是static类型检查的推荐方法) |
|57 | [react-dom 包的用途是什么？](#react-dom包的用途是什么) |
|58 | [react-dom render 方法的目的是什么？](#react-dom-render方法的目的是什么) |
|59 | [什么是 ReactDOMServer？](#什么是ReactDOMServer) |
|60 | [如何在 React 中使用 innerHTML？](#如何在React中使用innerHTML) |
|61 | [如何在 React 中使用 style？](#如何在React中使用style) |
|62 | [React 中事件有什么不同？](#React中事件有什么不同) |
|63 | [在 constructor 中使用 setState() 会发生什么？](#在constructor中使用setState()会发生什么) |
|64 | [数组索引作为keys的影响是什么？](#数组索引作为keys的影响是什么) |
|65 | [在 componentWillMount() 方法中使用 setState() 好么？](#在componentWillMount()方法中使用setState()好么) |
|66 | [如果在初始化 state 时使用 porps 会发生什么?](#如果在初始化state时使用porps会发生什么) |
|67 | [如何根据条件渲染组件?](#如何根据条件渲染组件)
|68 | [为什么在dom元素上展开props时要注意?](#为什么在dom元素上展开props时要注意) |
|69 | [React 怎么使用修饰器?](#React怎么使用修饰器) |
|70 | [你如何记忆一个组件?](#你如何记忆一个组件) |
|71 | [如何实现服务器端呈现或SSR?](#如何实现服务器端呈现或SSR) |
|72 | [React 怎么开启 production 模式?](#React怎么开启production模式) |
|73 | [什么是CRA及其好处?](#什么是CRA及其好处) |
|74 | [挂载阶段生命周期方法的顺序是什么?](#挂载阶段生命周期方法的顺序是什么) |
|75 | [React v16 什么生命周期方法不赞同使用?](#React-v16什么生命周期方法不赞同使用) |
|76 | [getDerivedStateFromProps() 生命周期的目的是什么?](#getDerivedStateFromProps()生命周期的目的是什么) |
|77 | [getSnapshotBeforeUpdate() 生命周期方法的目的是什么?](#getSnapshotBeforeUpdate()生命周期方法的目的是什么) |
|78 | [createElement() 和 cloneElement() 不同?](#createElement()和cloneElement()不同) |
|79 | [推荐的命名组件的方法是什么?](#推荐的命名组件的方法是什么) |
|80 | [组件类中方法的推荐顺序是什么？](#组件类中方法的推荐顺序是什么) |
## React 核心

1. ### 什么是React？

    React 是一个 **开源前端JavaScript库** 用于构建用户界面， 尤其是单页面应用程序。他被用于处理 web 和 移动 app 的视图层。 React 是由Facebook 的软件工程师 Jordan Walke 所创立的. React于2011年首次部署在Facebook的News Feed上，2012年首次部署在Instagram上。

2. ### React主要特点是什么？

    React 主要特点是:

    * 考虑到RealDOM操作很昂贵，它使用 **VirtualDOM** 而不是 RealDOM 。
    * 支持 **服务器端渲染**。
    * 遵循 **单向** 数据流或数据绑定。
    * 使用 **可重用/可组合的** UI 组件来开发视图。

3. ### 什么是JSX？

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

4. ### 元素和组件有什么区别？

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

5. ### 如何在React中创建组件？

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

6. ### 何时使用ClassComponent替函FunctionComponent？

    如果组件需要 *内部状态（state）或生命周期方法 * 则使用类组件，否则使用函数组件。

7. ### 什么是PureComponents？

    *`React.PureComponent`* 与 *`React.Component`* 极为相似， 除了处理了 `shouldComponentUpdate()` 方法，当 props 或state 改变, *PureComponent* 将会浅层比较 state 和 props。另一方面， *Component*  在输出的时候不会比较porps 和 state, 因此，无论何时 `shouldComponentUpdate` 被调用组件总会重新渲染。

8. ### React中state是什么？

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

    ![state](image/state.jpg)

9. ### React中porps是什么？

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

10. ### state和porps的区别？

    *props* 和 *state* 都是 javascript 纯对象. 他们都保存影响渲染的数据, 但它们在组件方面的功能却不同。 Props 类似于函数参数传递给组件， 而 state 类似于函数中声明的变量在组件内部中管理。

11. ### 为什么不应该直接更新state？

    为什么不应该直接更新state，那么它不会重新渲染组件.

    ```javascript
    //错误
    this.state.message = 'Hello world'
    ```

    使用 `setState()` 方法代替. 他会为组件的state对象计划（安排）更新. 当state改变, 组件会重新渲染。

    ```javascript
    //正确
    this.setState({ message: 'Hello World' })
    ```

    **提示:**你可以使用 *constructor* 或javascript最新class声明语法中的任意一个，直接指定state对象。

12. ### 回调函数作为setState()参数的目的是什么？

    当setState执行完成，回调函数会被执行，而且组件会被重新渲染。 因 `setState()` 是 **异步的** 所以回调函数被用来发起一些请求。

    **提示:** 推荐使用生命周期函数而不是使用回调函数

    ```javascript
    setState({ name: 'John' }, () => console.log('The name has updated and component re-rendered'))
    ```

13. ### HTML和React事件绑定的区别是什么？

    1. HTML中时间名字必须是 *小写*:

    ```html
    <button onclick='activateLasers()'>
    ```

    然而React中遵循 *驼峰命名* 约定:

    ```jsx harmony
    <button onClick={activateLasers}>
    ```

    2. HTML中可以返回 `false` 阻止默认行为:

    ```html
    <a href='#' onclick='console.log("The link was clicked."); return false;' />
    ```

    然而React中必须明确调用 `preventDefault()`:

    ```javascript
    function handleClick(event) {
      event.preventDefault()
      console.log('The link was clicked.')
    }
    ```

14. ### 如何在JSX回调中绑定方法或事件绑定？

    有3中可行的方法达到目的:

    1.	**Constructor中绑定:** 在javascript的class中, 方法默认不会绑定执行上下文. 在React的事件绑定中也是同样的. 通常在constructor中绑定.

    ```javascript
    class Component extends React.Componenet {
      constructor(props) {
        super(props)
        this.handleClick = this.handleClick.bind(this)
      }

      handleClick() {
        // ...
      }
    }
    ```

    2. **Public class fields syntax（类的字段语法）:** 如果你不喜欢bind方法，那么 *public class fields syntax（类的字段语法）* 可以正确的绑定回调。

    ```jsx harmony
    handleClick = () => {
      console.log('this is:', this)
    }
    ```

    ```jsx harmony
    <button onClick={this.handleClick}>
      {'Click me'}
    </button>
    ```

    3. **回调中的箭头函数:** 你可以在回调函数中直接使用 *箭头函数*.

    ```jsx harmony
    <button onClick={(event) => this.handleClick(event)}>
      {'Click me'}
    </button>
    ```

    **提示:** 如果回调函数作为属性传递到组件, 这些组件可能会不必要的重新渲染. 鉴于此,考虑到性能问题， 使用`.bind()` 或 *public class fields syntax（类的字段语法）* 是首选的.

15. ### 如何向事件绑定或回调中传递一个参数？

    可以使用 *箭头函数* 包裹一个 *事件绑定函数* 并传入参数:

    ```jsx harmony
    <button onClick={() => this.handleClick(id)} />
    ```

    这相当于调用 `.bind`:

    ```jsx harmony
    <button onClick={this.handleClick.bind(this, id)} />
    ```

16. ### React中合成事件是什么？

    ```合成事件` 是浏览器原生事件跨浏览器进行了封装的事件. 它的API与浏览器原生事件相似, 包括 `stopPropagation()` 和 `preventDefault()`, except the events work identically across all browsers.

17. ### 什么是内联条件表达式？

    JS中提供了条件表达式，你可以使用 *if 声明* 或 *三元表达式* . 除了这些方法, 你也可以JS逻辑运算符`&&`在JSX中嵌入一些表达式。

    ```jsx harmony
    <h1>Hello!</h1>
    {
      messages.length > 0 &&
      <h2>
        You have {messages.length} unread messages.
      </h2>
    }
    ```

    <!-- TODO: fix this section -->

18. ### 什么是key属性，在数组中使用它们的好处是什么？

    `key` 是一个特殊的string属性，在创建数组元素的时候你 **应该** 包含它们 . *Keys* 帮助React确认哪一项发生改变,加入,或移除。

    多数时候使用数据中的id作为 *keys*:

    ```jsx harmony
    const todoItems = todos.map((todo) =>
      <li key={todo.id}>
        {todo.text}
      </li>
    )
    ```

    当没有稳定的ID用作每一项渲染时, 也可以使用数组的 *索引* 当作 *key*，作为最后的选择:

    ```jsx harmony
    const todoItems = todos.map((todo, index) =>
      <li key={index}>
        {todo.text}
      </li>
    )
    ```

    **提示:**

    1. 使用 *索引* 作为 *key* 是 **不推荐** 的。如果每一项的先后顺序改变. 会对性能有副作用并可能导致组件状态的问题。
    2. 如果将列表中的一项提取为单独的组件， 那么在组件上使用 *keys* 来代替 `li` 标签.
    3. 如果`key`属性在列表项中不存在，在控制台会报出错误.

19. ### refs有什么用？

    *ref* 用来返回一个元素的引用. 大多用情况 *应该避免使用*,当需要直接的操作DOM元素或组件实例时它们会非常有用。

20. ### 如何创建refs？

    有两种方法。
    1. 这是不久前才加入的方法. *Refs* 使用 `React.createRef()` 方法创建， 通过 `ref` 属性被附加到React元素上. 为了在组件中随处使用 *refs*, 只要把 *ref* 赋给组件构造函数的实例属性。

    ```jsx harmony
    class MyComponent extends React.Component {
      constructor(props) {
        super(props)
        this.myRef = React.createRef()
      }
      render() {
        return <div ref={this.myRef} />
      }
    }
    ```
    2. 也可以使用ref回调函数方法，无论在什么React版本中. 例如, SearchBar 组件获取Input元素，如下,
    ```jsx harmony
    class SearchBar extends Component {
       constructor(props) {
          super(props);
          this.txtSearch = null;
          this.state = { term: '' };
          this.setInputSearchRef = e => {
             this.txtSearch = e;
          }
       }
       onInputChange(event) {
          this.setState({ term: this.txtSearch.value });
       }
       render() {
          return (
             <input
                value={this.state.term}
                onChange={this.onInputChange.bind(this)}
                ref={this.setInputSearchRef} />
          );
       }
    }
    ```

    函数式组件中也可以通过闭包使用 *refs*
    **提示**: 你也可是使用内联的ref回调函数，虽然他不是推荐的方法。

21. ### 什么是 forward refs？

    *Ref forwarding* 是一个新特性， 让一些组件获得到接受的 *ref*, 并把它进一步传递到下层的子组件中.

    ```jsx harmony
    const ButtonElement = React.forwardRef((props, ref) => (
      <button ref={ref} className="CustomButton">
        {props.children}
      </button>
    ));

    // Create ref to the DOM button:
    const ref = React.createRef();
    <ButtonElement ref={ref}>{'Forward Ref'}</ButtonElement>
    ```

22. ### 在refs回调函数和findDOMNode()应该首选哪一个？

    应该优先使用 *callback refs* 而不是 `findDOMNode()`. 为了预防 `findDOMNode()` 在将来的 React 版本中发生改变

    `findDOMNode` 一般的使用方法:

    ```javascript
    class MyComponent extends Component {
      componentDidMount() {
        findDOMNode(this).scrollIntoView()
      }

      render() {
        return <div />
      }
    }
    ```

    推荐的使用方法:

    ```javascript
    class MyComponent extends Component {
      componentDidMount() {
        this.node.scrollIntoView()
      }

      render() {
        return <div ref={node => this.node = node} />
      }
    }
    ```

23. ### 为什么曾经refs是String类型？

    如果曾经在工作中使用过React, 你可能轻车熟路的一个过时的API就是 String 类型的 `ref` 属性， 像 `ref={'textInput'}`, 和 通过像 `this.refs.textInput` 的方式引用. 我们强烈反对它因为 *String 类型的 refs 有以下问题*, 他们在过去被反复确认过. String 类型的refs  **已经在 React V16 版本中被移除**.

    1. 它们 *迫使 React 与当前正在执行的组件保持联系*. 这是有问题的， 因为它使得 React 模块有状态, 因此 React 模块在打包过程中被复制时，会产生意想不到的问题.
    2. 它们是 *不可合并的* — 如果一个库把 ref 放在被传入的子元素上,使用者不能把另一个 ref 再放在上面. refs 回调函数是完美的可合并的。
    3. 它们像 Flow 一样 *在静态分析时并不工作* .Flow 无法推测框架想让字符串类型 ref 出现在 `this.refs` 上。 因此，他的类型可能不同. refs 回调函数对静态分析是友好的.
    4. 大多数人使用类似 "回调函数" 时，并不会像期待中的那样工作。 (例如 <DataGrid renderRow={this.renderRow} />)
       ```jsx harmony
       class MyComponent extends Component {
         renderRow = (index) => {
           // This won't work. Ref will get attached to DataTable rather than MyComponent:
           return <input ref={'input-' + index} />;

           // This would work though! Callback refs are awesome.
           return <input ref={input => this['input-' + index] = input} />;
         }

         render() {
           return <DataTable data={this.props.data} renderRow={this.renderRow} />
         }
       }
       ```
24. ### 什么是虚拟DOM？

    *虚拟DOM* (VDOM) 是内存中 *真实DOM* 的映射. UI的表现保存在内存中，并与“真实”DOM同步。他是发生在渲染函数被调用和在屏幕中展现元素之间的一步。 这一完整的过程称为 *reconciliation*.

25. ### 虚拟DOM是如何工作的？

    *虚拟DOM* 工作的三个简单步骤.

    1. 无论何时一些底层的数据改变, 全部UI都会在虚拟DOM表示中重新呈现。。
        ![vdom](image/vdom1.png)

    2. 然后计算前一个DOM表现和新DOM表现之间的差异。
        ![vdom2](image/vdom2.png)

    3. 一旦计算完成，真实 DOM 只会更新确实被改变的部分。
        ![vdom3](image/vdom3.png)

26. ### Shadow DOM 和 Virtual DOM 的区别？

    *Shadow DOM* 浏览器技术为在 *web components* 中变量和css作用域主要设计的。 *Virtual DOM* 是JavaScript库在浏览器API 上贯彻的理念。

27. ### 什么事React Fiber？

    Fiber 是React 16 中新的协调引擎或核心算法的重新实现。React Fiber的目标是提高其在诸如动画、布局、手势、暂停和中止的能力等领域的性能，重用工作并为不同类型的更新分配优先级; and new concurrency primitives.

28. ### ReactFiber出现的主要目的是什么？

    React Fiber 的目标是提高其在动画，布局，手势，等领域的性能. 首要的特点是 **增量渲染**: 可以把渲染工作切割成多k块，在多个画面中进行渲染.

29. ### 什么是受控组件？

    在用户输入后控制（劫持）了表单中的输入元素的组件叫做 **受控组件**, 即, 每一个 state 的改变都会有相关的处理函数

    例如, 把名字全部写为大写字母, 使用像下面的处理,

    ```javascript
    handleChange(event) {
      this.setState({value: event.target.value.toUpperCase()})
    }
    ```

30. ### 什么是非受控组件？

    **非受控组件** 是那些在自己内部存储状态的组件, 当你需要时，通过使用 ref 访问元素找到当前的值。这有点像传统的HTML。

    UserProfile 组件中, `name` 输入使用 ref 接入.

    ```jsx harmony
    class UserProfile extends React.Component {
      constructor(props) {
        super(props)
        this.handleSubmit = this.handleSubmit.bind(this)
        this.input = React.createRef()
      }

      handleSubmit(event) {
        alert('A name was submitted: ' + this.input.current.value)
        event.preventDefault()
      }

      render() {
        return (
          <form onSubmit={this.handleSubmit}>
            <label>
              {'Name:'}
              <input type="text" ref={this.input} />
            </label>
            <input type="submit" value="Submit" />
          </form>
        );
      }
    }
    ```

    一般情况下, 推荐使用受控组件实现表单.
31. ### createElement 和 cloneElement 的区别？

    JSX 元素将会被编译成 `React.createElement()` 函数用来创建 react 元素，他们将用于UI的对象表示. 然而， `cloneElement` 用来克隆一个元素并传入新的props.

32. ### React 中 State 提升是什么？

    当几个组件需要共享相同的可变数据时，建议 *提升共享状态* 到它们最近的公共祖先元素. 意味着如果两个子组件共享相同的数据时来自他们的父元素。 把状态移动到父元素代替在每个子元素中都有自己的状态。

33. ### 组件生命周期的不同阶段是什么？

    组件生命周期有四个不同阶段.

    1. **Initialization（初始化）:** 组件准备设置初始化 state 和 默认的 props.

    2. **Mounting（挂载）:** 组件随时可以在浏览器元素中挂载. 这个阶段包括 `componentWillMount()` 和 `componentDidMount()` 生命周期方法.

    3. **Updating（更新）:**  组件通过两种方式更新, 发送新的props 和 更新state. 这个阶段包括 `shouldComponentUpdate()`, `componentWillUpdate()` 和 `componentDidUpdate()` 生命周期方法.

    4. **Unmounting（卸载）:** 组件不再需要，从浏览器DOM中被卸载. 这个阶段包括 `componentWillUnmount()` 生命周期方法.
        ![phases](image/phases.png)

    <!-- TODO: new lifecycle methods in React v16 -->

34. ### React 生命周期方法是什么？

    - **componentWillMount:** 在渲染前执行，在根组件中用作App级别的配置。
    - **componentDidMount:** 在第一次渲染后执行，这里应该发生，所有的请求，元素、state 更新,事件监听。
    - **componentWillReceiveProps:** 当某些props更新触发了state的改变时执行。
    - **shouldComponentUpdate:** 决定组件是否更新. 默认返回true.在 state 或 props 更新后如果确定组件不需要冲渲染可以返回false.这是一个提升性能非常好的地方，因为它可以让你在组件接收到新的props避免重新渲染。
    - **componentWillUpdate:** 在重渲染前执行，如果有通过 `shouldComponentUpdate()` 确认的state 或 props 的改变，返回true.
    - **componentDidUpdate:** 大多数使用它在prop 或 state 改变时响应更新DOM。
    - **componentWillUnmount:** 它将用于取消任何传出的网络请求，或移除所有组件应该绑定的事件监听函数。

    <!-- TODO: new lifecycle methods in React v16 -->

35. ### 什么是高阶组件？

    *高阶组件* (*HOC*) 是一个接受组件并返回新组件的函数. 基本上,它是从React 组合特定中派生的一种模式。

    可以叫它们 **pure components** 因为它们可以接受任何动态提供的子组件，它们不会修改或复制来自输入组件的任何行为。

    ```javascript
    const EnhancedComponent = higherOrderComponent(WrappedComponent)
    ```

    HOC 可以在很多场景中使用:

    1. 代码重用、逻辑 和 bootstrap abstraction。
    2. 渲染劫持。
    3. 状态抽象和控制。
    4. Props 控制。

36. ### 如何创建高阶组件的 props 代理？

    你可以通过组件中使用 *props 代理* 的形式添加或编辑 props:

    ```jsx harmony
    function HOC(WrappedComponent) {
      return class Test extends Component {
        render() {
          const newProps = {
            title: 'New Header',
            footer: false,
            showFeatureX: false,
            showFeatureY: true
          }

          return <WrappedComponent {...this.props} {...newProps} />
        }
      }
    }
    ```

37. ### 什么是 context？

    *Context* 规定一种方法，穿过组件数传递数据，不需要在每个层级手动的把 props 传递下去。例如, 有效用户, locale preference, UI 主题在程序的很多组件中都需要接入。

    ```javascript
    const {Provider, Consumer} = React.createContext(defaultValue)
    ```

38. ### 什么是 children porp？

    *Children* 是一个 prop (`this.prop.children`)，允许把组件作为数据传递给其他组件, 就像使用其他的 props 一样. 组件树将把起始标签，闭合标签中间的内容作为 `children` prop 传递给其他组件。
    这有许多 React API 中的方法，对这个 prop 适用. 包括 `React.Children.map`, `React.Children.forEach`, `React.Children.count`, `React.Children.only`, `React.Children.toArray`.

    ```jsx harmony
    const MyDiv = React.createClass({
      render: function() {
        return <div>{this.props.children}</div>
      }
    })

    ReactDOM.render(
      <MyDiv>
        <span>{'Hello'}</span>
        <span>{'World'}</span>
      </MyDiv>,
      node
    )
    ```

39. ### 在 react 中怎么写注释？

    React/JSX 的注释于 JavaScript 多行注释很相似但要放在花括号中。

    **单行注释:**

    ```jsx harmony
    <div>
      {/* 单行注释(在通常的Javascript中, 单行注释使用两个反斜线(//)) */}
      {`Welcome ${user}, let's play React`}
    </div>
    ```

    **多行注释:**

    ```jsx harmony
    <div>
      {/* 多行
       注释 */}
      {`Welcome ${user}, let's play React`}
    </div>
    ```

40. ### 使用带 props 参数的 super 构造函数的目的是什么？

     子类构造函数在调用 `super()` 方法之前不能使用 `this` 引用。同样适用于ES6子类.传递参数到 `super()` 执行的主要原因是在子构造函数中获得 `this.props`.

    **传递Porps:**

    ```javascript
    class MyComponent extends React.Component {
      constructor(props) {
        super(props)

        console.log(this.props) // prints { name: 'John', age: 42 }
      }
    }
    ```

    **没有传递Porps**

    ```javascript
    class MyComponent extends React.Component {
      constructor(props) {
        super()

        console.log(this.props) // prints undefined

        // but props parameter is still available
        console.log(props) // prints { name: 'John', age: 42 }
      }

      render() {
        // no difference outside constructor
        console.log(this.props) // prints { name: 'John', age: 42 }
      }
    }
    ```

    上面代码显示 `this.props` 只在构造函数中是不同的.在构造函数之外是一样的。

41. ### 什么是 reconciliation？

    当一个组件的 props 或 state 改变,React通过比较新返回的元素和先前呈现的元素来确定是否需要实际的DOM更新。当他们不相同, react 将会更新DOM. 这一过程被叫做 *reconciliation*.

42. ### 如何使用动态 key 值设置state？

    如果你使用 ES6 或 Babel 转换器转换你的 JSX, 那么你可以使用 *computed property names* 完成.

    ```javascript
    handleInputChange(event) {
      this.setState({ [event.target.id]: event.target.value })
    }
    ```

43. ### 每次渲染时每次调用函数的常见错误是什么？

    你需要清楚的是，函数作为参数传递时没有被调用。

    ```jsx harmony
    render() {
      // 错误: handleClick 已经执行，替换了作为引用传递!
      return <button onClick={this.handleClick()}>{'Click Me'}</button>
    }
    ```

    相反，不带括号传递函数本身:

    ```jsx harmony
    render() {
      // 正确: handleClick 作为引用传递!
      return <button onClick={this.handleClick}>{'Click Me'}</button>
    }
    ```

44. ### 为什么必须大写组件名称？

    这是必须的，因为组件不是DOM元素，他们是构造函数. 同样, 在 JSX  中小写标签名代表 HTML 元素，不是组件.

45. ### React 为什么使用 `className` 代替 `class` 属性？

    `class` 在Javascript中是一个关键字, JSX 是 JavaScript 的扩展. 这是 React 为什么使用 `className` 代替`class` 的主要原因. 传递一个 String 类型 `className` 属性.

    ```jsx harmony
    render() {
      return <span className={'menu navigation-menu'}>{'Menu'}</span>
    }
    ```
46. ### 什么是 fragments？

    这是React中的通用模式，用于组件返回多个元素。*Fragments* 允许在不向DOM添加额外节点的情况下对子节点列表进行分组。

    ```jsx harmony
    render() {
      return (
        <React.Fragment>
          <ChildA />
          <ChildB />
          <ChildC />
        </React.Fragment>
      )
    }
    ```

    还有*更短的语法*，但是许多工具不支持它：

    ```jsx harmony
    render() {
      return (
        <>
          <ChildA />
          <ChildB />
          <ChildC />
        </>
      )
    }
    ```

47. ### 为什么 fragments 比 div 容器好？

    1. Fragments 会更快一点，不需要创建额外的DOM节点使用更少的内存. 这只对大树和深树有真正的好处。
    2. 一些CSS机制 *Flexbox* 和 *CSS Grid* 有特殊的父子关系, 在中间添加div使得很难保持所需的布局。
    3. DOM检查器会更清晰。

48. ### React 中 portals 是什么？

    *Portal* 是将子节点呈现到存在于父组件的DOM层次结构之外的DOM节点的推荐方法。

    ```javascript
    ReactDOM.createPortal(child, container)
    ```

    第一个参数是任何可呈现的Reict子元素，例如元素、字符串或片段。第二个参数是DOM元素。

49. ### 什么是无状态组件？

    如果行为独立于其状态，那么它可以是一个无状态组件。 可以使用函数或类来创建无状态组件。 不在组件中使用生命周期函数, 您应该选择函数组件.如果您决定在这里使用函数组件，那么有很多好处；它们易于编写、理解和测试，稍微快一点，并且您可以完全避免使用 `this` 关键字。

50. ### 什么是有状态组件？

    如果组件的行为取决于组件的 `state`，那么可以将其称为有状态组件, 这些 *有状态组件* 总是 *class 组件* 并在 `constructor` 中获取初始化 state. 

    ```javascript
    class App extends Component {
      constructor(props) {
        super(props)
        this.state = { count: 0 }
      }

      render() {
        // ...
      }
    }
    ```
51. ### React 中如何对 props 进行验证？

    当程序运行在 *开发模式*, React 将会自动检查所有设置在组件上的 props 确保它们有 *正确类型*. 如果类型错误, React将在控制台中生成警告消息。 由于性能影响，它在*生产模式*中禁用。. The mandatory props are defined with `isRequired`.

    一组预定义的prop类型:

    1. `PropTypes.number`
    2. `PropTypes.string`
    3. `PropTypes.array`
    4. `PropTypes.object`
    5. `PropTypes.func`
    6. `PropTypes.node`
    7. `PropTypes.element`
    8. `PropTypes.bool`
    9. `PropTypes.symbol`
    10. `PropTypes.any`

    我们可以为 `User` 组件定义 `propTypes`:

    ```jsx harmony
    import React from 'react'
    import PropTypes from 'prop-types'

    class User extends React.Component {
      static propTypes = {
        name: PropTypes.string.isRequired,
        age: PropTypes.number.isRequired
      }

      render() {
        return (
          <>
            <h1>{`Welcome, ${this.props.name}`}</h1>
            <h2>{`Age, ${this.props.age}`}</h2>
          </>
        )
      }
    }
    ```

    **Note:** 在 React v15.5 *PropTypes* 被从 `React.PropTypes` 移动到 `prop-types` 库.

52. ### React的优点是什么？

    1. 使用 *Virtual DOM* 提高应用程序的性能。
    2. JSX 使代码易读易写.
    3. 同时支持客户端服务端渲染 (*SSR*).
    4. 易于与框架（Angular, Backbone）集成，因为它只是一个视图库。
    5. 易于使用诸如Jest之类的工具编写单元和集成测试。

53. ### React 的局限是什么？

    1. React 只是一个视图库，并不是完整的框架.
    2. 对于刚接触网络开发的初学者来说，有一个学习曲线。
    3. 将React集成到传统的MVC框架中需要一些额外的配置。
    4. 代码复杂性随着内联模板和JSX的增加而增加。
    5. 太多的小组件导致过度工作量或模版。

54. ### React V16 中错误边界是什么？

    *错误边界*是在其子组件树中的任何位置捕获JavaScript错误的组件，打印这些错误, 并显示一个回退UI，防止组件树崩溃。

    一个类组件如果定义一个 `componentDidCatch(error, info)` 新的生命周期方法就回变成错误边界。

    ```jsx harmony
    class ErrorBoundary extends React.Component {
      constructor(props) {
        super(props)
        this.state = { hasError: false }
      }

      componentDidCatch(error, info) {
        // 显示回退 UI
        this.setState({ hasError: true })
        // 你也可以向错误收集服务器发送错误
        logErrorToMyService(error, info)
      }

      render() {
        if (this.state.hasError) {
          // 你可以渲染任何自定义的回退UI
          return <h1>{'Something went wrong.'}</h1>
        }
        return this.props.children
      }
    }
    ```

    之后像常规组件一样使用:

    ```jsx harmony
    <ErrorBoundary>
      <MyWidget />
    </ErrorBoundary>
    ```

55. ### React v15中如何处理错误边界？

    React v15 为错误边界提供了非常基本的支持使用 `unstable_handleError` 方法. 

56. ### 什么是 static 类型检查的推荐方法？

    在 React 程序中，通常我们使用 *PropTypes库* (`React.PropTypes` 在 React v15.5 移动到 `prop-types` 包中) 用作 *类型检查*。 以大量代码作为基础, 推荐使用 *static 类型检查* 就像 Flow 或 TypeScript, 在编译时执行类型检查并提供自动完成功能的。

57. ### react-dom 包的用途是什么？

    `react-dom` 包提供了*DOM特定的方法*可以在应用程序的顶层使用. 大多数组件不需要使用此模块。这个包的一些方法是:

    1. `render()`
    2. `hydrate()`
    3. `unmountComponentAtNode()`
    4. `findDOMNode()`
    5. `createPortal()`

58. ### `react-dom` render 方法的目的是什么？

    此方法用于在所提供的容器中将React元素呈现到DOM中，并返回对组件的引用。如果React元素先前被呈现到容器中, 它将对它执行更新，并且仅根据需要修改DOM以反映最新的更改。

    ```
    ReactDOM.render(element, container[, callback])
    ```

   如果提供了可选的回调，则在呈现或更新组件之后将执行该回调。

59. ### 什么是ReactDOMServer？

    `ReactDOMServer` 对象使您能够渲染组件为静态标记（通常在节点服务器上使用）. 这个对象主要用于*服务器端呈现*(SSR)。以下方法可以在服务器和浏览器环境中使用

    1. `renderToString()`
    2. `renderToStaticMarkup()`

    例如，通常运行基于节点的Web服务器，如Express、Hapi或Koa，然后调用 `renderToString` 将根组件呈现给字符串，然后作为响应发送该字符串。

    ```javascript
    // using Express
    import { renderToString } from 'react-dom/server'
    import MyPage from './MyPage'

    app.get('/', (req, res) => {
      res.write('<!DOCTYPE html><html><head><title>My Page</title></head><body>')
      res.write('<div id="content">')
      res.write(renderToString(<MyPage/>))
      res.write('</div></body></html>')
      res.end()
    })
    ```

60. ### 如何在 React 中使用 innerHTML？

    `dangerouslySetInnerHTML` 是浏览器中 React 代替 `innerHTML` 的属性. 就像 `innerHTML` 一样, 考虑到跨站点脚本（XSS）攻击，使用这个属性是危险的。 你只需要传递一个对象key为 `__html` 值为文本 .

    在这个例子中，MyComponent使用 `dangerouslySetInnerHTML` 属性来设置HTML标记:

    ```jsx harmony
    function createMarkup() {
      return { __html: 'First &middot; Second' }
    }

    function MyComponent() {
      return <div dangerouslySetInnerHTML={createMarkup()} />
    }
    ```
61. ### 如何在React中使用style？

    `style` 属性接受驼峰命名的javascript对象而不是 CSS 字符串。 这与DOM样式的JavaScript属性是一致的，更加有效，并且防止了XSS安全漏洞。.

    ```jsx harmony
    const divStyle = {
      color: 'blue',
      backgroundImage: 'url(' + imgUrl + ')'
    };

    function HelloWorldComponent() {
      return <div style={divStyle}>Hello World!</div>
    }
    ```

   Style 键是驼峰命名，以便与JavaScript中访问DOM节点上的属性一致 (例如. `node.style.backgroundImage`).

62. ### React 中事件有什么不同？

    绑定事件在 React 中有一些语法上的不同:

    1. React 事件处理是驼峰命名而不是小写命名。
    2. JSX 中传递一个函数作为事件处理函数,而不是一个字符串.

63. ### 在 constructor 中使用 `setState()` 会发生什么？

    当使用 `setState()`, 除了给对象状态赋值之外，React还重新呈渲染件及其所有子组件。 你会得到像这样的错误: *Can only update a mounted or mounting component.* 所以需要使用 `this.state` 在 constructor 初始化 state 变量.

64. ### 数组索引作为keys的影响是什么？

    键应该是稳定的、可预测的、唯一的，以便React可以跟踪元素。

    在下面的代码片段中，每个元素的键将基于排序, 而不是和正在使用的数据绑定.这限制了React可以做的优化。

    ```jsx harmony
    {todos.map((todo, index) =>
      <Todo
        {...todo}
        key={index}
      />
    )}
    ```

    如果将元素数据用于唯一键，假设todo.id对这个列表是惟一的并且是稳定的，React将能够重新排序元素，而无需对它们重新赋值。

    ```jsx harmony
    {todos.map((todo) =>
      <Todo {...todo}
        key={todo.id} />
    )}
    ```

65. ### 在 `componentWillMount()` 方法中使用 `setState()` 好么？

    建议避免 `componentWillMount()` 生命周期方法中的异步初始化。`componentWillMount()` 在渲染前发生. 在 `render()` 前被调用, 因此，在该方法中设置状态将不会触发重新渲染. 避免在此方法中引入任何side-effects or subscriptions。确保对组件的异步赋值发生在 `componentDidMount()` 而不是 `componentWillMount()`.

    ```jsx harmony
    componentDidMount() {
      axios.get(`api/todos`)
        .then((result) => {
          this.setState({
            messages: [...result.data]
          })
        })
    }
    ```
66. ### 如果在初始化state时使用porps会发生什么?

    如果在不刷新组件的情况下更改组件上的属性，新的prop值将永远不会显示，因为构造函数函数永远不会更新组件的当前状态。 只有当组件首次创建时，才会从props中执行状态初始化。

    下面的组件不会显示更新的输入值： 

    ```jsx harmony
    class MyComponent extends React.Component {
      constructor(props) {
        super(props)

        this.state = {
          records: [],
          inputValue: this.props.inputValue
        };
      }
      //译者：如果想使用props的值渲染组件，那么在render中直接从props中获取，而不是在constructor中保存在state中。
      render() {
        return <div>{this.state.inputValue}</div>
      }
    }
    ```

    在render方法中使用props将更新值：

    ```jsx harmony
    class MyComponent extends React.Component {
      constructor(props) {
        super(props)

        this.state = {
          record: []
        }
      }

      render() {
        return <div>{this.props.inputValue}</div>
      }
    }
    ```

67. ### 如何根据条件渲染组件?

    您希望根据某种状态渲染不同的组件. JSX 不会渲染 `false` 或 `undefined`, 所以你可以使用条件 *短路*，仅当某个条件为真时才渲染组件的给定部分。

    ```jsx harmony
    const MyComponent = ({ name, address }) => (
      <div>
        <h2>{name}</h2>
        {address &&
          <p>{address}</p>
        }
      </div>
    )
    ```

    如果你需要 `if-else` 条件，那么使用 *三元运算*.

    ```jsx harmony
    const MyComponent = ({ name, address }) => (
      <div>
        <h2>{name}</h2>
        {address
          ? <p>{address}</p>
          : <p>{'Address is not available'}</p>
        }
      </div>
    )
    ```

68. ### 为什么在dom元素上展开props时要注意?

    当 *展开props* 我们遇到添加未知HTML属性的风险, 这是个坏习惯. 相反，我们可以使用 `...rest` 操作符，因此它只添加所需的 props。例如

    ```jsx harmony
    const ComponentA = () =>
      <ComponentB isDisplay={true} className={'componentStyle'} />

    const ComponentB = ({ isDisplay, ...domProps }) =>
      <div {...domProps}>{'ComponentB'}</div>
    ```

69. ### React 怎么使用修饰器?

    你可以 *修饰* 你的 *类* 组件, 就像给一个函数传递组件一样. **Decorators** 是灵活易读的修改组件功能的方法。

    ```jsx harmony
    @setTitle('Profile')
    class Profile extends React.Component {
        //....
    }

    /*
      title 是一个字符串将会被设置为 document title
      WrappedComponent 是上面个例子中，修饰器放在上面的类组件
    */
    const setTitle = (title) => (WrappedComponent) => {
      return class extends React.Component {
        componentDidMount() {
          document.title = title
        }

        render() {
          return <WrappedComponent {...this.props} />
        }
      }
    }
    ```

    **Note:** 装饰器是没有进入ES7的一个特性，但是目前是一个*阶段2建议*。

70. ### 你如何记忆一个组件?

    有可用的memoize库，可用于函数组件。例如，`moize` 库可以将另一个组件中的组件记忆起来。

    ```jsx harmony
    import moize from 'moize'
    import Component from './components/Component' // this module exports a non-memoized component

    const MemoizedFoo = moize.react(Component)

    const Consumer = () => {
      <div>
        {'I will memoize the following entry:'}
        <MemoizedFoo/>
      </div>
    }
    ```
71. ### 如何实现服务器端呈现或SSR?

    React 以及具备在服务器端的渲染。有一个特殊版本的DOM渲染器可用, 它遵循与客户端相同的模式。

    ```jsx harmony
    import ReactDOMServer from 'react-dom/server'
    import App from './App'

    ReactDOMServer.renderToString(<App />)
    ```

    此方法将以字符串形式输出常规HTML, 然后将其作为服务器响应的一部分放在页面正文中。在客户端, React 检测预渲染的内容， 然后 seamlessly（无缝的） picks up（获取） where it left off（停止）.

72. ### React 怎么开启 production 模式?

    你应该使用 Webpack 的 `DefinePlugin` 方法设置 `NODE_ENV` 成 `production`,它删除了PropType验证和额外警告等内容。 除此之外, 如果你压缩代码, 例如, Uglify 的 dead-code 删除仅用于开发的代码和注释, 它会大大减小你的包裹的尺寸。

73. ### 什么是CRA及其好处?

    `create-react-app` CLI 工具允许你快速穿件并运行React 程序而不需要配置的过程.

    让我们使用 *CRA* 创建 TODO app:

    ```console
    # Installation
    $ npm install -g create-react-app

    # Create new project
    $ create-react-app todo-app
    $ cd todo-app

    # Build, test and run
    $ npm run build
    $ npm run test
    $ npm start
    ```
    它包含了我们建立一个React app 需要的所有事情:

    1. React, JSX, ES6, 和异步流的支持.
    2. ES6之外的语言附加项，如对象扩展运算符.
    3. 自动添加 CSS 前缀,所以不需要 -webkit- 或其他的前缀.
    4. 一个快速交互的单元测试运行程序，内置了对覆盖率报告的支持.
    5. 对常见错误发出警告的实时开发服务器.
    6. 一个构建脚本，用于打包JS、CSS和用于生产的图像，以及hashes 和sourcemaps.

74. ###  挂载阶段生命周期方法的顺序是什么?

    当一个组件的实例被创建并插入到DOM中，生命周期方法按照下面的顺序被调用。
    1. `constructor()`
    2. `static getDerivedStateFromProps()`
    3. `render()`
    4. `componentDidMount()`

75. ### React v16 什么生命周期方法不赞同使用?

    下面的生命周期方法将是不安全的编码实践，并且在异步呈现方面会有更多的问题。

    1. `componentWillMount()`
    2. `componentWillReceiveProps()`
    3. `componentWillUpdate()`

    从react v16.3开始，这些方法的别名是“unsafe”前缀，未修复的版本将在react v17中删除。

76. ### `getDerivedStateFromProps()` 生命周期的目的是什么?

    新的静态生命周期方法 `getDerivedStateFromProps()`，在实例化组件之后以及重新渲染组件之前调用. 它可以返回一个对象来更新state, 或 `null` 表示新 props 不需要任何状态更新。

    ```javascript
    class MyComponent extends React.Component {
      static getDerivedStateFromProps(props, state) {
        // ...
      }
    }
    ```

    此生命周期方法与 `componentdidUpdate()` 一起涵盖 `componentwillReceiveProps()` 的所有使用场景。

77. ### `getSnapshotBeforeUpdate()` 生命周期方法的目的是什么 ?

    新的生命周期方法 `getSnapshotBeforeUpdate()` 在 DOM 更新之前调用. 从这个方法返回的值，将会被传递到 `componentDidUpdate()` 第三个参数中.

    ```javascript
    class MyComponent extends React.Component {
      getSnapshotBeforeUpdate(prevProps, prevState) {
        // ...
      }
    }
    ```

    此生命周期方法与 `componentDidUpdate()` 一起涵盖 `componentWillUpdate()`的所有使用场景。

78. ### createElement() 和 cloneElement() 不同?

    在JSX中，react元素被转换为 `react.createElement()`，表示一个UI元素。而`react.clonelement()`用于克隆元素并传递新的属性。

79. ### 推荐的命名组件的方法是什么?

    建议通过引用来命名组件，而不是使用 `displayname`。

    将 `displayname`用于命名组件：

    ```javascript
    export default React.createClass({
      displayName: 'TodoApp',
      // ...
    })
    ```

    **建议的** 方法:

    ```javascript
    export default class TodoApp extends React.Component {
      // ...
    }
    ```

80. ### 组件类中方法的推荐顺序是什么？

    *建议* 从 *挂载* 到 *渲染阶段* 的方法顺序:

    1. `static`方法
    2. `constructor()`
    3. `getChildContext()`
    4. `componentWillMount()`
    5. `componentDidMount()`
    6. `componentWillReceiveProps()`
    7. `shouldComponentUpdate()`
    8. `componentWillUpdate()`
    9. `componentDidUpdate()`
    10. `componentWillUnmount()`
    11. 事件处理方法 `onClickSubmit()` 或 `onChangeDescription()`
    12. 渲染的 getter 方法 `getSelectReason()` 或 `getFooterContent()`
    13. 可选渲染方法 `renderNavigation()` 或 `renderProfilePicture()`
    14. `render()`
