# Code Review and Practices

## Before you begin
- [IMPORTANT: JavaScript Best Practices](https://www.slideshare.net/cheilmann/javascript-best-practices-1041724/25-Problem_Repetition_ofmodule_name_leads)

## Few basics. 
- `console.log` is a very bad idea. Never push this in. If you're using this for debugging - please stop doing that and use a standard debugger instead. 
- Never push commented code in. Comments are fine, commented code is not. 
- Always use `SVG` for icons because it scales really really well. Never use `PNG, GIF, JPEGS`. 

## General
- If you're new to Code base. Ask your manager for a quick walk-through. Before you ask for this. Make sure Codebase and the project is installed on your system and is running properly.
- If you're new to codebase. Get your code reviewed everyday even when you're in the middle of the task.
- We use Bitbucket for closed sourced repos and GitHub for open source repos.
- Fork the repo you want to work on to your local account.
- Please create feature branches if you're working on a feature. For example, if you're working on signup feature create a branch from master called `feature-signup`
- If you're working on a bug then create a new branch form master called `bug-signup`.
- **Important:** Send a PR to staging and not to master.
- Only send a PR to staging when you're completely done with your feature with tests.
- Push changes in everyday. Its important to push changes in when you're done with your work everyday. Doing this would create backup of your work on the server. If your machine goes down, your work doesn't.
- When you send a PR to staging. It's YOUR responsibility to get it merged in. Contact your manager for review and merge.
- When your work is on staging. Test it manually on the staging server. When everything looks good. Go to your staging branch and send in a PR to master. Your task is ONLY done when your work is merged to master.
- Function names should be a verb. Functions do something. Example: save(), delete(), testConnection(), etc. If you're writing JavaScript, function names should be camelCase (The first letter of the function should be lower case, the next subsequent word should be upper case). If you're writing code in any other language then follow the best practices of that language. For example: In C# function names are PascalCase  (The first letter of the function is upper case, the next subsequent word is also upper case).
- If you're copy pasting code, then this is a very clear indication you're on the wrong path. Make the code you want to copy paste into module / component / function  / class  and reuse that.
When you're starting to write a new function think twice (No. thrice!, seriously!). Think about:
- Is the same functionality is already implemented in another function, then use that instead of the new one.
- Think twice about the function name. Do you get what the function does if you read the function name.
- Write quick documentation before the function.


```
FunctionName: One quick sentence of what this fucntion does.
Parameters:
<Param1> |  <Type>  | <One quick sentence on what this param does>
<Param2> |  <Type>  | <One quick sentence on what this param does>
<ParamN> |  <Type>  | <One quick sentence on what this param does>
Returns:
What does this function returns, If this function is a promise. Then say what the it returns when the promise resolves and what it returns when the promise rejects.  
```


- Class names should be a noun. Classes are something. Example: Student, CloudObject, etc. If you're wrting JavaScript, class names should be PascalCase  (The first letter of the class is upper case, the next subsequent word is also upper case). If you're writing code in any other language then follow the best practices of that language.
- Write quick documentation before the Class.


```
ClassName: One quick sentence of what this class does.
```


### JavaScript
- Never use == operator. Always use ===. This will save you from few hours of bug fixing.

### React
- DO NOT use jQuery in any of your REACT CODE to modify DOM Elements. Once the DOM is modified outside of React control, React Virtual DOM update doesn't update actual DOM element.
