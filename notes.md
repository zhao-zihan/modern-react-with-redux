1. React doesn't print or render objects in curly braces

   ```react
   function App() {
    const config = { color: 'red' }
   
     return (
       <div>
         {config} 
       </div>
     ) 
     // react will throw error for displaying objects inside curly braces
   }
   
   ```

2. When passing props, use double quotes to wrap Strings and curly braces to wrap Numbers, Arrays, Objects and Variables.

   ```react
   function App() {
    	return (
       <input type="number" min={5}/>
     ) 
   }
   ```

3. Five rules:

   - All prop names follow camelCase ('placeholder')
   - Number attributes use curly braces
   - Boolean true can be omitted, false needs to be specified
   - class is written as className
   - in-line styles are provided as objects, if the style name contains any dashes, remove them and capitalize the next word

4. Export/Import

   ```react
   function App() {
     return <h1>Hi</h1>
   }
   
   export default App
   
   const message1 = 'hi'
   export { message }
   
   // or
   
   export default function App2() {
     return <h1>Hello</h1>
   }
   
   export const message2 = 'hello'
   ```

   ```react
   import MyApp from './App'
   
   // default exports can be renamed in the importing file
   
   import App, {message} from './App'
   
   // named exports can't be renamed
   ```

5. Images that are smaller than 9.7kb will be included in-line instead of be treated as a sperate file

6. Sibling components in React cannot directly communicate without the help from a third party library

7. If you wrap an input element inside a form element, whenever you enter the enter key, it will submit the result and refresh the page, but don't forget to prevent the default behavior of onSubmit event of the form, because it will automatically collect form values and submit requests to a different urls

   ```react
   <form>
     <input></input>
   </form>
   ```

8. Common error: 

   > A component is changing an uncontrolled input to be controlled.

   happens when you update code inside the browser without refreshing the page

9. Using index as list keys in React is a fallback, you will get bugs since each time when you change the original order of the list, the indexes change as well, so you cannot guarantee the uniqueness of the keys

10. When you update state like an array state, if you modify the existing array instead of making a copy of it, React is "smart" enough to detect that you are manipulating the same array based on its reference thus no state update is triggered.

11. slice cheatsheet

    ![image-20230710213459460](notes.images/image-20230710213459460.png)

12. Add element at the middle of an array

    ![image-20230710213933285](notes.images/image-20230710213933285.png)

13. Modify an element based on a property

    ![image-20230710214944317](notes.images/image-20230710214944317.png)

    

14. Adding properties to an object

    ![image-20230716170000497](notes.images/image-20230716170000497.png)

15. Removing properties from an object

    ![image-20230716170053081](notes.images/image-20230716170053081.png)

16. When does the callback function get called when useEffect is used?

    ![image-20230716175752677](notes.images/image-20230716175752677.png)

    