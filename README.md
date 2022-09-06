# React Js  Freshers

# 1.What is React?

React is a front-end and open-source JavaScript library which is useful in developing user interfaces specifically for applications with a single page.
It is helpful in building complex and reusable user interface(UI) components of mobile and web applications as it follows the component-based approach.

The important features of React are:

* It supports server-side rendering.
* It will make use of the virtual DOM rather than real DOM (Data Object Model) as RealDOM manipulations are expensive.
* It follows unidirectional data binding or data flow.
* It uses reusable or composable UI components for developing the view.

# 2. What are the advantages of using React?

* MVC is generally abbreviated as Model View Controller.

Use of Virtual DOM to improve efficiency: React uses virtual DOM to render the view. As the name suggests, virtual DOM is a virtual representation of the real DOM.
Each time the data changes in a react app, a new virtual DOM gets created.
Creating a virtual DOM is much faster than rendering the UI inside the browser. 
Therefore, with the use of virtual DOM, the efficiency of the app improves.

SEO friendly: React allows developers to develop engaging user interfaces that can be easily navigated in various search engines. 
It also allows server-side rendering, which boosts the SEO of an app.

Reusable components: React uses component-based architecture for developing applications. Components are independent and reusable bits of code. 
These components can be shared across various applications having similar functionality. The re-use of components increases the pace of development.

Huge ecosystem of libraries to choose from: React provides you with the freedom to choose the tools, libraries, 
and architecture for developing an application based on your requirement.

# 3. What are the limitations of React?

The few limitations of React are as given below:

* React is not a full-blown framework as it is only a library.

* The components of React are numerous and will take time to fully grasp the benefits of all.

* It might be difficult for beginner programmers to understand React.

* Coding might become complex as it will make use of inline templating and JSX.


# 4 What is useState() in React?

The useState() is a built-in React Hook that allows you for having state variables in functional components. It should be used when the DOM has something that is dynamically manipulating/controlling.

In the below-given example code, The useState(0) will return a tuple where the count is the first parameter that represents the counter’s current state and the second parameter setCounter method will allow us to update the state of the counter.

...
const [count, setCounter] = useState(0);
const [otherStuffs, setOtherStuffs] = useState(...);
...
const setCount = () => {
   setCounter(count + 1);
   setOtherStuffs(...);
   ...
};

We can make use of setCounter() method for updating the state of count anywhere. In this example, we are using setCounter() inside the setCount function where various other things can also be done. The idea with the usage of hooks is that we will be able to keep our code more functional and avoid class-based components if they are not required.

