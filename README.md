# Pre-requisite
   - JS Fundamentals
   - TS
   - Promise async/await

# What is REACT
   - It is a library that is developed by facebook back in 2013 to achieve more dynamic and responsive user interface that is fast and highly performant. Basicaly react is created to build more complex web applications that is hard to achieve with vanilla js. And keep in mind that react is a library not a framework.

# Why use REACT
   - Using vanilla javascript is like building a house with just a hammer but using react its like building a house using heavy machinery to get the work much faster.

# Set up
   - install node js
   - npm create vite@latest
   - select react as framework
   - select either typescript or javascript
   - cd yourProjectName
   - npm install
   - npm run dev
#### Note: You don't need a separate live server to quickly see the changes because theres already built in live server in vite + react setup

# What is JSX
   - It is a javascript inside html and denoted by `{}` and using camelCasing in all css and html attributes
   - Example:
   ```
      <img src={yourImage} className="" />
   ```

# What is component
   - Component is just your customized html element that you can use anywhere in the app with the notation of `<ComponentName />`
   - Also you can think of this just typical function and always has 2 parts your method boody and the jsx return type
   - Example:
   ```
      function ComponentName() {
         // method body
         return (
            <>
               <h1>{dynamicVariable}</h1>
            </>
         );
      }
   ```

# React hooks
`useState`
   - Always returns 2 variables
   - First is the variable/state
   - Second is the setter function that set the variable/state
   ###### its like getter and setter but the difference is inside the setter function there magic happening to update the dom
   - Example:
   ```
      const [count, setCount] = useState(initialValue);
   ```
`useEffect`
   - always have 2 parameters
   - First is the functionEffect to run when the specified variable/state is updated and the return of this method is the clean up code.
   - Second is the dependency array this where you will specify the variable/state you want to listen when that variable is updated it will run the functionEffect.
   - Example:
   ```
      const [count, setCount] = useState(0);

      // useEffect(functionEffect, dependencyArray);
      // functionEffect will run everytime the count is updated, changed, deleted anything
      useEffect(() => {
         // method body
         return () => {
            // clean up code
         }
      }, [count]);
   ```
   ###### Note: don't use a setter function of the variable/state that is declared in dependency array because it will causing infinite loop
