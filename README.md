# Lab 06 - Basics of React

## Tasks
### 1. Create and run basic app
1. Init a new react application. There is multiple ways how to work with react, but we will be using "CREATE REACT APP" toolchain. Read what it does [here](https://reactjs.org/docs/create-a-new-react-app.html#create-react-app)
    - Run command `npx create-react-app my-app` 
    - This command will run for a while. (PRO tip: Windows - if you feel funky, you can pause your anti-virus which will speed up things. Linux/Mac users are fine)
1. Verify that the application is correctly installed by running the commands
    - `cd my-app` enter the correct folder
    - `npm start` which will start a local **development** server which does automatic rebuilds of your app when you change files

1. Edit `App.js` and observe the changes in your browser

### 2. Basic modifications
1. Edit a return on function app in `app.js` to say:
    - Remove the `<header>`, your return should look like this:
      ```
      return (
        <div className="App">
         //.. your new code
        </div>
      );
      ```     
    - `Hello` wrapped in h1 element
    - `From the React world!` as h2 element
    - ![image](https://user-images.githubusercontent.com/8086995/137988976-6b1177f1-013a-4b66-ae2a-fb2508d428f3.png)


1. Move the h2 element with text `From the React world!` into variable. As per variable [declaration](https://reactjs.org/docs/introducing-jsx.html)
   - Use this variable inside your return function using `{myVariable}` on the place where h2 element was previously created. 
   - The rendered output should stay the same! 

### 3. Create a new component - MainContent
 - Create new function which will be called MainContent - components should start with upper case. https://reactjs.org/docs/components-and-props.html
 - This component(function) should return <div> with text This is my body, with bold text
 - Use the component in the return function of the app function. Components are used the same way as other elements - like this `<MyComponent></MyComponent>` or `<MyComponent/>` if we don't want to have any element childs. 
 - ![image](https://user-images.githubusercontent.com/8086995/137989728-3d90dda5-ea77-408b-b2cf-c67562841b36.png)

### 4. Create a new component with props
 - Create a new function which will be called RenderNumber, this function will accept parameter `props` as described here https://reactjs.org/docs/components-and-props.html
 - The property which it will accept will be called `number` 
 - The component should return the div with text: `{number} is a great number!`
 - Add random number to the App function `const randomNumber = Math.floor(Math.random() * 100);`
 - Add component `RenderNumber` to the App and as a props pass the `randomNumber` https://reactjs.org/docs/components-and-props.html#rendering-a-component
 - When you refresh the site - you should get always a different number 
 - ![image](https://user-images.githubusercontent.com/8086995/137991141-f4fa3646-25d5-4674-b1f3-45cc42fb0b7e.png)

### 5. Conditional rendering
 - Modify the component `RenderNumber` in a way that it will render  `{number} is small number` in case the number is smaller than 50, otherwise `{number} is big number!`
 - Hint: You can sovle this by using 2x return in your function or inline operators. More here https://reactjs.org/docs/conditional-rendering.html
 - ![image](https://user-images.githubusercontent.com/8086995/137991936-ad8bbe6e-30a5-4294-9d95-43a7eae8c164.png)

  
### 6. Burger time
 - Create new file called `burger-time.js`
 - Create a new component in this file, called BurgerTime, this component will accept 2 props: `name` and `count`
 - The component will return a list using `ul` and `li` elements https://www.w3schools.com/html/html_lists_unordered.asp
 - Each element of this list will be text `{name} is the best burger!` the name shoudl be bold 
 - It's going to have as many elements in the list as the prop count 
 - Export the component from the file (the same way we did on the past labs) 
 - Import the component int he app.js and use it! 
 - ![image](https://user-images.githubusercontent.com/8086995/137993508-db87d7c4-f9a5-4112-a662-4e5286bfaff7.png)
