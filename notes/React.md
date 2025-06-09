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
