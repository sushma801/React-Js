<li><a href="#coreRedux">Core principle of Redux</a></li>
<li><a href="#reduxApp">Explain the structure of redux application</a></li>
<li><a href="#actions">What is the role of actions in Redux? Can you provide an example?</a></li>
<li><a href="#connectFunction">What is the purpose of connect() in Redux?</a></li>
<li><a href=""></a></li>
<li><a href=""></a></li>
<li><a href=""></a></li>
<li><a href=""></a></li>
<li><a href=""></a></li>
<li><a href=""></a></li>
<li><a href=""></a></li>
<li><a href=""></a></li>
<li><a href=""></a></li>
<li><a href=""></a></li>
<li><a href=""></a></li>
<li><a href=""></a></li>




<div id="coreRedux">

# Core Principle Of Redux

The core principles of Redux are foundational concepts that guide its design and usage. 
They ensure state management is predictable, scalable, and easy to debug. Here are the key principles:

1. **Single Source of Truth**
The state of the entire application is stored in a single JavaScript object tree (the store).
This centralized state ensures that the application state is consistent and easily accessible.
**Benefits**:
Simplifies debugging.
Provides a single point to inspect and manipulate state.
Enables features like time-travel debugging.

2. **State is Read-Only**
The state can only be changed by dispatching actions.
Actions are plain JavaScript objects that describe what happened (e.g., { type: 'INCREMENT' }).
**Benefits**:
Ensures state changes are predictable and controlled.
Makes the application easier to test and debug.
Prevents accidental state mutations.

3. **Changes are Made with Pure Functions**
To specify how the state changes in response to actions, you write reducers.
A reducer is a pure function that takes the current state and an action as arguments and returns a new state.
**Characteristics of Pure Functions**:
No side effects (e.g., API calls or modifying the arguments).
Returns the same output for the same input.
Does not modify the original state; instead, it creates a new state object.
**Benefits**:
Predictable state transitions.
Easy to test individual reducers.

</div>



<div id="reduxApp">

# Structure of redux Application
A Redux application typically follows a well-defined structure that organizes its 
components and logic into specific layers. This structure promotes scalability, 
maintainability, and readability. Here's a breakdown of the common structure:

1. **Store**
The store is the central hub of the Redux application, holding the entire application's state tree.
It is created using the createStore function (or configureStore in Redux Toolkit).
The store also integrates middleware and enhancers for additional functionality, such as 
logging, handling asynchronous actions, and debugging.

<img src="./images/redux/store.png">

2. **Reducers**
Reducers are pure functions that specify how the state should change in response to actions.
They take the current state and an action as arguments and return a new state.
Reducers are usually organized by feature and combined using the Reducers function.

<img src="./images/redux/reducer.png">

3. **Actions**
Actions are plain JavaScript objects that describe events or intentions to change the state.
They must have a type property (a string) and can optionally include a payload for additional data.

4. **Action Creators**
Functions that return action objects to encapsulate the creation of actions.
They make code more reusable and readable.

5. **Middleware**
Middleware is used to extend Redux with custom functionality, such as logging, 
asynchronous operations (e.g., API calls), or analytics.
Examples: redux-thunk, redux-saga.

<img src="./images/redux/middleware.png">

6. **Selectors**
Functions to encapsulate and reuse logic for accessing specific parts of the state.
They help keep components clean by abstracting state access logic.

<img src="./images/redux/store.png">


</div>

<div id="actions">

# Actions in Redux
In Redux, **actions** are plain JavaScript objects that represent an intention to change the state of the
application. They are dispatched to the Redux store to indicate that something has happened 
(e.g., user interaction, API response).

## Key Features of Actions:
1. **Plain Object**: Actions are plain JavaScript objects.
2. **Mandatory type Field**: Every action must have a type property, which is a string that describes the action.
3. **Payload (Optional)**: Actions can include additional data (payload) required to update the state.

<img src="./images/redux/actions.png">
</div>

<div id="connectFunction">

# Connect()

In Redux, the **connect()** function is used to link React components with the Redux store. 
It allows components to access the state and dispatch actions to update the state. 
This is done by connecting the component to specific slices of the Redux state 
and providing it with functions to dispatch actions.

## Key Purposes of connect():
1. **Access State**: Enables components to read specific pieces of state from the Redux store.
2. **Dispatch Actions**: Provides components with functions to dispatch actions to the store.
3. **Separate Concerns**: Keeps the component logic separate from the Redux store, 
making the component more reusable and easier to test.

**Syntax**
<img src="./images/redux/connect.png">

</div>




