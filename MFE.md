<li><a href="mfe">What is Micro front end?</a></li>
<li><a href=""></a></li>
<li><a href=""></a></li>
<li><a href=""></a></li>
<li><a href=""></a></li>
<li><a href=""></a></li>
<li><a href=""></a></li>
<li><a href=""></a></li>
<li><a href=""></a></li>
<li><a href=""></a></li>


<div id="mfe">

# Micro-front End: 
Micro frontends (MFE) is an architectural style in frontend development where a large, monolithic 
application is divided into smaller, independently developed, tested, and deployed frontend 
components or applications. These smaller applications, often referred to as "micro apps," work together
to form a cohesive user experience, similar to the microservices architecture in backend development.

## Key Features of Micro Frontends:
1. **Independence**: Each micro frontend is developed and deployed independently by different teams.
2. **Technology Agnostic**: Teams can use different frameworks, libraries, or tools for their micro 
apps as long as they adhere to agreed integration contracts.
3. **Decentralized Ownership**: Different teams own specific features or functionalities of the application.
4. **Resilience**: Issues in one micro frontend typically do not affect others, improving fault tolerance.

## Benefits:
1. **Scalability**: Teams can work on different parts of the application simultaneously.
2. **Flexibility**: Teams can adopt the best tools and technologies for their specific needs.
3. **Faster Deployment**: Micro apps can be updated independently, leading to quicker releases.
4. **Maintainability**: Smaller codebases are easier to manage and debug.

<img src="./images/MFE/mfe.jpg">

<img src="./images/MFE/mfe_example1.jpg">

## Challenges:
a. **Complexity**: Managing multiple repositories, deployments, and integrations can increase complexity.
b. **Performance**: Combining multiple micro apps on the client-side or server-side can impact performance.
c. **Consistency**: Ensuring a uniform look and feel across micro apps requires additional effort.

## Integration Techniques:
a. **Client-Side Composition**: Each micro app is loaded dynamically in the browser 
(e.g., using iframes or JavaScript frameworks).
b. **Server-Side Composition**: The server combines micro apps into a single HTML page before sending
it to the browser.
c. **Build-Time Composition**: Micro apps are integrated during the build process into 
a single deployable artifact.

## Popular Tools & Frameworks:
1. **Module Federation (Webpack)**: Enables sharing and dynamic loading of modules across applications.
2. **Single-SPA**: A framework for orchestrating multiple micro frontends.
3. **Qiankun**: A micro frontend framework built on top of Single-SPA.
4. **Web Components**: Standardized browser APIs to create reusable, encapsulated components.
</div>