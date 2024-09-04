# React-Js
<li><a href="#reconciliation">Reconciliation</a></li>

### Details about React js

**React** is a popular JavaScript library for building user interfaces, particularly for single-page applications
where you need a dynamic, responsive, and interactive experience. 
Developed and maintained by Facebook, React allows developers to create large web applications
that can update and render efficiently in response to data changes without reloading the page.

#### Key Features of React:
1. **Component-Based Architecture**: React encourages developers to break down the UI into reusable components.
    Each component is like a small, self-contained piece of the UI that can be composed to form complex UIs

2. **JSX (JavaScript XML)**: React uses JSX, a syntax extension that allows you to write HTML-like code 
    directly within JavaScript. JSX makes the code easier to understand and allows for seamless
    integration of HTML with JavaScript logic.

    <img src="./images/simple_code.png">

3. **Virtual DOM**: React uses a Virtual DOM, which is a lightweight representation of the actual DOM.
4. **Unidirectional Data Flow**: In React, data flows in a single direction, from parent to child components. 
    This makes it easier to debug the application.
5. **React Hooks**: Hooks are functions that let you use state and other React features in functional components.
    Hooks like useState and useEffect allow you to add state management and side effects to functional 
    components without writing classes.

   <img src="./images/Hooks_example.png" alt="Hooks Example">


#### Use Cases for React:
1. Single-page applications (SPAs)
2. Mobile applications (using React Native)
3. Complex and dynamic web interfaces
4. Building reusable UI components

Overall, React has become a standard tool in modern web development due to its flexibility, performance, and ease of use.





### Stateful component and Stateless component:
If the component depends on the state of the component, it is called a **stateful component**.
**Features:**
    1. **Manages State:** Uses useState, useReducer, or other hooks that manage state in functional components. 
        In class components, state is managed using this.state and this.setState.
    2. **Lifecycle Methods:** In class components, stateful components often use lifecycle methods 
        (e.g., componentDidMount, componentDidUpdate, componentWillUnmount). In functional components, 
        you can achieve similar effects with the useEffect hook.
    3. **Dynamic:** Since the component's state can change, the rendered output can also change over time,
        making it dynamic.

<img src="./images/statefull_component.png">

If the component is independent of the state of the component then it is called a **stateless component**.
**Features:**
    1. **No State:** Stateless components don't manage or store state internally.
    2. **Pure Components:** Often implemented as pure functions, meaning they always produce the same output given 
        the same input (props).
    3. **Simpler and Reusable:** Since they don't manage state, they're generally simpler and more reusable.

<img src="./images/stateless_component.png">

**Controlled Component**: those components that are controlled by input elements within the form or user input.
1. At first we initialize a state using useState
2. Set the value of the form using props
3. Write an handler function to update the state
4. Attach the handle function with the input element.
**Uncontrolled Component:**  thoses component which has its own store for handling event. Like ref.
1. At first we create a ref using useRef.
2. Attached that ref to the form.
3. Ref will have an internal handle which update the value of current on changing the value.

**React fiber** is the new implementation or core algorithm of React v16. Which is used to increase the suitability 
areas like gesture, animation, ability to pause, abort work, prioritize the work and divide the work into chunks.


**React Fiber** is a complete rewrite of React's core algorithm, introduced in React v16. It was designed to address 
    limitations in the previous reconciliation algorithm and to improve various aspects of React's performance and 
    capabilities.
#### Key Features of React Fiber
1. **Concurrency**: React Fiber enables React to pause, abort, or re-prioritize work. This allows React to handle 
    complex user interactions (like gestures and animations) more smoothly by breaking work into smaller units and 
    prioritizing critical updates.
2. **Incremental Rendering**: Fiber allows React to divide the work into chunks and spread it out over multiple frames. 
    This improves the responsiveness of the UI by making rendering more interruptible and ensuring that updates do not 
    block the main thread for too long.
3. **Priority-Based Updates**: React Fiber introduces the concept of prioritizing updates based on their importance. 
    For instance, user interactions (such as clicks or typing) can be given higher priority than background data 
    fetching, ensuring a smoother and more responsive user experience.
4. **Error Handling**: Fiber improves error handling by enabling better recovery mechanisms and making it easier to 
    catch errors within components.
5. **Flexible Rendering**: Fiber provides the ability to render asynchronously, allowing React to adjust and optimize 
    rendering based on the current state of the application and user interactions.


# Virtual DOM
The Virtual DOM (VDOM) is an in-memory representation of the real DOM elements. It acts as an intermediary between 
the application and the browser's actual DOM, helping to optimize updates and rendering for performance.

**Here's how it works:**

1. **Initial Render**: When a React component is rendered for the first time, a Virtual DOM tree is created that 
    mirrors the structure of the actual DOM.

2. **Changes and Updates**: When changes occur in the component state or props, a new Virtual DOM tree is created.

3. **Reconciliation**: React then compares this new Virtual DOM tree with the previous one using a process called 
    "reconciliation". This comparison is efficient due to React's use of a diffing algorithm that identifies the
    minimum number of changes needed.

4. **Patching the Real DOM**: After identifying the changes, React updates the actual DOM only where necessary, 
    ensuring minimal manipulation and improving performance.


**Here's a step-by-step summary of the process:**

1. **State/Prop Change**: A change in state or props triggers a re-render in React.
2. **Virtual DOM Update**: React creates a new Virtual DOM tree based on the updated state/props.
3. **Diffing Algorithm**: React compares the new Virtual DOM tree with the previous one to identify differences.
4. **Batch Updates**: React efficiently updates the real DOM by applying only the necessary changes.

This approach minimizes direct DOM manipulations, making updates more efficient and improving the 
overall performance of the application.


<div id="reconciliation">

# Reconciliation

**Reconciliation** is the step that happens between the render function being called and the final elements displayed
on the screen. This entire process is known are reconciliation. It involves comparing the new Virtual DOM with the
previous one and efficiently updating the real DOM to reflect any changes. This ensures optimal performance 
by minimizing direct DOM manipulations.

</div>

