[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-718a45dd9cf7e7f842a935f5ebbe5719a5e09af4491e668f4dbf3b35d5cca122.svg)](https://classroom.github.com/online_ide?assignment_repo_id=11755556&assignment_repo_type=AssignmentRepo)
# Mystery Function

What does the `mystery()` function in the following piece of code do? Add your
answer to this markdown file.

```javascript
function mystery(a) {
    if(a.length == 1) return a[0];
    var foo = mystery(a.slice(1, a.length))
    if(foo > a[0]) return foo;
    else return a[0];
}
```

If the length of the array is 1 then it returns the 1 element.
it then makes a shallow copy of the array, starting after the first element, to the end of the array, and stores it in variable foo. 
If foo is greater than the first element of the array then it returns array foo.
if the first element is greater then it returns the first element. 

It appears that the comparison will always return false, so it will always return a slice of the array, removing the first element, if it is not length 1. 

