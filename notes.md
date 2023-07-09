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

2.  When passing props, use double quotes to wrap Strings and curly braces to wrap Numbers, Arrays, Objects and Variables.

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

4.  Export/Import

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