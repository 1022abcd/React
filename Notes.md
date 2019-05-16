# Sections
- [Let's Dive](#lets-dive)
- [Building Content with JSX](#building-content-with-jsx)
- [Communicating with Probs](#communicating-with-probs)
#Let's Dive
**React** is a single JavaScript library
Its ultimate purpose is to show content(HTML) to users and handle user interaction

React 'Components' are made using either JavaScript function or classes

###Why using both 'React' and 'ReactDom'
- 'React' knows what a component is and how to make components work together.
- 'ReactDOM' knows how to take a component and make it show up in the DOM. 

###What is a 'npm'?
- npm stands for 'Node Package Manager' which allows you to download and use many useful packages

###Babel
- Babel is a command line tool that takes any versions of JavaScript and spit out newer version 
- Ex: ES2015(Not supportive for all browser) -> Babel(Chages to ES5) -> ES5(Supportive for all) -> Works on All Browsers

###Project Directories
- src: Folder where we put all the source code we write
- public: Folder that stores static files, like images
- node-modules: Folder that contains all of our project dependencies
- pacakge.json: Records our project Dependencies and configures our project
- package-lock.json: Records the exact version of packages that we install
- README.MD: Instructions on how to use this project

###import vs require
- import : ES2015 Modules
- require : CommonJS Modules

###What is a React Component
- It is a **Function** or **Class** 
- It produces HTML to show the user (Using JSX)
- It handles feedback from the user (Using Event Handlers)

---

#Building Content with JSX

###InLine Style in JSX
- html : 
```HTML
 <button style="bakground-color: blue; color: white'">Submit</button> 
 ```
- JSX :  
```JSX
 <button style={{backgroundColor: 'blue', color: 'white'}}> 
 ```

###Class vs ClassName
- class : Javascript keyword
    - Ex: ``` class App extends React.Component ```
- className : JSX keyword
    - Ex: ``` <label className="label" for="name"> ```

###Referencing JavaScript variables as JSX
- 
``` Javascript
 const App2 = () => {
        const buttonText = 'Click Me!';

        return (
            <div>
                <label className="label" for="name">
                    Enter name:
                </label>
                <input id="name" type="text" />
                <button style={{ backgroundColor: 'blue', color: 'white'}}>
                    {buttonText}
                </button>
            </div>
        );
    }
```

---

#Communicating with Probs

### Three Tenets
- Component Nesting
    - A component can be shown inside of another
- Component Resuability
    - We want to make components that can be easily reused through out application
- Component Configuration
    - We should be able to configure a component when it is created 

## The Probs
- System for passing data from a parent component to a child component
- Goal is to customize or configure a child component
