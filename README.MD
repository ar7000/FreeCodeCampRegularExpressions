Revisiting Regular Expressions via FreeCodeCamp resources and copying passed code to Git repo as I go through each task. Documenting below anything new I learn, or anything I am reminded of that I may have forgotten.

- Reminded how to use regular expressions to match literals in strings. Example:
    ```
    let waldoIsHiding = "Somewhere Waldo is hiding in this text.";
    let waldoRegex = /Waldo/;
    let result = waldoIsHiding.match(waldoRegex); //Returns ["Waldo"]
    ```
    - Letters can also be replaced with the wildcard character '.' in order to find matches, e.g. /W.ldo/ would return same result in the above.

- Reminded of use of 'flags' in order to set conditions of finding a match within a string. Must be placed after the closing '/' within the regex. Example 'i' will tell the regex to ignore case and find all matches of the given string:

    ```
    let waldoIsHiding = "Somewhere Waldo is hiding in this text.";
    let waldoRegex = /HiDiNg/i;
    let result = waldoIsHiding.match(waldoRegex); //Returns ["hiding"];
    ```