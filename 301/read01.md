Component-based architecture focuses on the decomposition of the design into individual functional or logical components that represent well-defined communication interfaces containing methods, events, and properties. It provides a higher level of abstraction and divides the problem into sub-problems, each associated with component partitions.

What is a Component?

A component is a modular, portable, replaceable, and reusable set of well-defined functionality that encapsulates its implementation and exporting it as a higher-level interface.

A component is a software object, intended to interact with other components, encapsulating certain functionality or a set of functionalities. It has an obviously defined interface and conforms to a recommended behavior common to all components within an architecture.

A software component can be defined as a unit of composition with a contractually specified interface and explicit context dependencies only. That is, a software component can be deployed independently and is subject to composition by third parties.

Characteristics of Components
Reusability− Components are usually designed to be reused in different situations in different applications. However, some components may be designed for a specific task.
Replaceable− Components may be freely substituted with other similar components.
Not context specific− Components are designed to operate in different environments and contexts.
Extensible− A component can be extended from existing components to provide new behavior.
Encapsulated− A component depicts the interfaces, which allow the caller to use its functionality, and do not expose details of the internal processes or any internal variables or state.
Independent− Components are designed to have minimal dependencies on other components.




Principles of Component−Based Design

A component-level design can be represented by using some intermediary representation (e.g. graphical, tabular, or text-based) that can be translated into source code. The design of data structures, interfaces, and algorithms should conform to well-established guidelines to help us avoid the introduction of errors.

The software system is decomposed into reusable, cohesive, and encapsulated component units.
Each component has its own interface that specifies required ports and provided ports; each component hides its detailed implementation.
A component should be extended without the need to make internal code or design modifications to the existing parts of the component.
Depend on abstractions component do not depend on other concrete components, which increase difficulty in expendability.
Connectors connected components, specifying and ruling the interaction among components. The interaction type is specified by the interfaces of the components.
Components interaction can take the form of method invocations, asynchronous invocations, broadcasting, message driven interactions, data stream communications, and other protocol specific interactions.
For a server class, specialized interfaces should be created to serve major categories of clients. Only those operations that are relevant to a particular category of clients should be specified in the interface.
A component can extend to other components and still offer its own extension points. It is the concept of plug-in based architecture. This allows a plugin to offer another plugin API.


  




What is Props?

React is a component-based library which divides the UI into little reusable pieces. In some cases, those components need to communicate (send data to each other) and the way to pass data between components is by using props.




“Props” is a special keyword in React, which stands for properties and is being used for passing data from one component to another.

But the important part here is that data with props are being passed in a uni-directional flow. (One way from parent to child)




Using Props in React

I will be explaining how to use Props step by step.

Firstly, define an attribute and its value(data)
Then pass it to child component(s) by using Props
Finally, render the Props Data

In my previous article, I’ve shown how to create & call a React component inside another component. So in this example, we have a ParentComponent including another component (child):

class ParentComponent extends Component {  
  render() {
    return (
      <h1>
        I'm the parent component.
        <ChildComponent />
      </h1>
    );
  }
}

And this is our ChildComponent:

const ChildComponent = () => {  
  return <p>I'm the 1st child!</p>;
};

The problem here is that, when we call the ChildComponent multiple times:

class ParentComponent extends Component {  
  render() {
    return (
      <h1>
        I'm the parent component.
        <ChildComponent />
        <ChildComponent />
        <ChildComponent />
      </h1>
    );
  }
}

It always renders the same string again and again:

  

But what we like to do here is to get dynamic outputs, because each child component may have different data and let’s see how we can solve this issue by using props…

1st Step: Defining Attribute & Data

We already know that we can assign attributes and values to HTML tags:

<a href="www.google.com">Click here to visit Google</a>;

Likewise, we can do the same for React components. We can define our own attributes & assign values with interpolation { }:

<ChildComponent someAttribute={value} anotherAttribute={value}/>

Here I’m declaring a “text” attribute to the ChildComponent and then assign a string value: “I’m the 1st child”.

<ChildComponent text={“I’m the 1st child”} />

Now the ChildComponent has a property and a value. Next, we need to pass it via Props.

2nd Step: Passing Data using Props

OK, now let’s take the “I’m the 1st child!” string and pass it by using props.

Passing props is very simple. Like we pass arguments to a function, we pass props into a React component and props bring all the necessary data.

Arguments passed to a function:

const addition = (firstNum, secondNum) => {  
  return firstNum + secondNum;
};

Arguments passed to a React component:

const ChildComponent = (props) => {  
  return <p>I'm the 1st child!</p>;
};

Props are arguments passed into React components. — w3schools.com

Final Step: Rendering Props Data

Alright so far, we have created an attribute and its value, then we passed it through props but we still can’t see it because we haven’t rendered it yet.




et’s render our text property with interpolation:

const ChildComponent = (props) => { 
  return <p>{props.text}</p>;
};

  

class ParentComponent extends Component {
render() {
return (
<h1>
I'm the parent component.
<ChildComponent text={"I'm the 1st child"} />
<ChildComponent text={"I'm the 2nd child"} />
<ChildComponent text={"I'm the 3rd child"} />
</h1>
);
}
}

  

As we can see, each ChildComponent renders now its own prop data. So this is how we can use Props for passing data and converting static components into dynamic ones.