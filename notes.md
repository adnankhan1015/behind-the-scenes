#### How Does React Update the DOM?

#### And how are component functions excuted?

### Ways to avoid unnecessaruy components re-rendering.

#### 1. Memo

- Memo only prevents function executions that are triggered by the parent component.
- You should use it with care only on components, where you can actually prevent re-renders and as high up in the component tree as possible.

#### Don't Overuse memo() !!!

- Use it **as high up in the component tree as possible**.
  - Blocking a component execuyion there will also block all child component executions.
- Checking Props with memo() **costs performance**
  - Don't wrap it around all your components -- it will just add a lot of unnecessary checks.
- **Don't** use it on components where **props will change frequently**
  - memo() would just perform a meaningless check in such cases(which costs performance)

#### 2. Clever Component Composition in your Application

#### Understaing the useCallback() hook

-

#### WHy keys Matter When Managing State!!

- State is scoped to a component, if you use the same component function to create multiple component instances based on thta function every instance has its own isolated state.
- However, that is not the entire truth. Instead state is also tracked by position by REACT.

- State belongs to the position as well as the component type, the component here in the HistoryItem jumps from one component to another component
