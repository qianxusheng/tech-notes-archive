## React是UI库，专注于显示和交互，如组件化管理，状态管理，虚拟DOM(Document Object Model，网页的文件树模型)渲染等
## Next.js是基于React的前端框架，集成了更多功能，如路由，API等

- **compenent**: a piece of UI that has its own logic and appearance. Range from a small button to a entire page.
- **JSX**: JavaScript XML. The markup syntax. 
- **displaying data**: {user.name}
- **conditional rendering**: if, else
- **rendering list**: for loop or map function. (need id to distinguish different elements.) 
- **events handling**: <button onClick={handleClick}>  -- not button onClick={handleClick()}> , because we don't want to call the function for now.
- **state, props**: 组件属性和组件参数
- **hook**: functions start with use, like useState. react的hook要在function顶层，用于状态管理等
- **sharing data between components**: 通过统一参数传递到组件

## **basics**
**1**.DOM(document object model)是游览器解析静态HTML后生成的树形结构（动态的），在页面加载后javaScript可以随时操作它  
**2**.react比较虚拟DOM和游览器的DOM，only update differences  
**3**.react中，每个组件就是一个piece的UI，包含js和html，通常return JSX(javascript XML, eXtensible Markup Langauge)；  
- React的export每个js只能export一个default export，其他都是named export
- JSX是一种更严格的XML，可以写js（用curly brace）和html liked markup langauge，只能返回一个root tag；{{}}传入的是js object
- component传参；props或整个JSX
- conditional rendering(if-else;&&shortcut representation前者必须是boolean，不能是数字，会渲染0;?:ternary operation) and list rendering(filter, map)
- keeping component pure:尽可能保证组件独立，same input same output，便于safe cache，可以用于不同的环境（same input same output）；strictMode可以检查purity
- UI是一个tree结构；
- react的render tree就是组件树，代表组件之间的父子关系
- module dependency tree就是包依赖tree
- 游览器解析HTML，CSS(cascading style sheets)得到DOM、CSSOM，根据DOM生成render tree，然后根据render tree计算layout然后paint，整个过程就是rendering
