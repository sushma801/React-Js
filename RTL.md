# RTL (React Testing Library)

<li><a href="#RTL">About React Testing Library</a></li>

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

<div id="RTL">

# React Testing Library
<p> RTL in the context of React development typically refers to React Testing Library (RTL),
a popular tool for testing React components.
</p>

## Key Features of React Testing Library (RTL)

<li><b>Focus on user behavior:</b>  RTL encourages writing tests that mimic how a user interacts 
with the application. It promotes testing the component as it is used in the browser 
rather than testing implementation details.</li>
<li><b>No shallow rendering:</b> Unlike other testing libraries like Enzyme, RTL doesn't support 
shallow rendering. It renders components in the DOM to better simulate the actual application behavior.</li>
<li><b>Selectors based on accessibility:</b> RTL promotes selecting elements using methods like getByText, 
getByRole, and getByLabelText, which align with how users and screen readers interact with the app.</li>
<li><b>Encourages best practices:</b> It pushes developers toward writing maintainable tests that can survive
refactoring since the tests focus on the output of the component rather than internal details.</li>
    
####
<img src="./images/RTL/RTL_Example.png"/>

#### In this example:

<li><b>render:</b> Renders the component into a virtual DOM.</li>
<li><b>screen:</b> Allows access to various query methods for finding elements in the DOM.</li>
<li><b>fireEvent:</b> Simulates user actions like clicking.</li>
<li><b>expect:</b> Part of Jest, used to assert that the component behaves as expected.</li>

Since you use Vitest with React Testing Library, RTL would be your main tool for testing React components in a user-centric way.


</div>