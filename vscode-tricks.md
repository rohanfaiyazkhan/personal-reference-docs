# VS Code Tricks

## Regex find replace  
  
  To replace for example `<h3>Name</h3>` with `### Name` use a normal regex with the variable portion enclosed in braces for the search term. Then use `$Number` in your replace term (Number is the occurence of the variable)
    

 Find: `<h3>(.*)</h3>`  
 Replace: `### $1`