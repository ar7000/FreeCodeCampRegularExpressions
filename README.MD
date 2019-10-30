Revisiting Regular Expressions via FreeCodeCamp resources and copying passed code to Git repo as I go through each task. Documenting below anything new I learn, or anything I am reminded of that I may have forgotten.

- Reminded how to use regular expressions to match literals in strings. Example:
    ```
    let waldoIsHiding = "Somewhere Waldo is hiding in this text.";
    let waldoRegex = /Waldo/;
    let result = waldoIsHiding.match(waldoRegex); //Returns ["Waldo"]
    ```
    - Letters can also be replaced with the wildcard character '.' in order to find matches, e.g. /W.ldo/ would return same result in the above.
    - Letters can also be replaced with multiple possibilites in order to find matches, e.g. /Wa[lmnop]do/ would return same result in the above.

- Reminded of use of 'flags' in order to set conditions of finding a match within a string. Must be placed after the closing '/' within the regex. Example 'i' will tell the regex to ignore case and find all matches of the given string:

    ```
    let waldoIsHiding = "Somewhere Waldo is hiding in this text.";
    let waldoRegex = /HiDiNg/i;
    let result = waldoIsHiding.match(waldoRegex); //Returns ["hiding"];
    ```

- Reminded how to use character sets to match ranges of characters. Done by surrounding character set with square brackets. Example:
    ```
    let quoteSample = "The five boxing wizards jump quickly.";
    let alphabetRegexV2 = /[f-j]/gi;
    let result = quoteSample.match(testRegex); //Returns ["h","f","i","i","g","i","j","i"]
    ```

    - Shorthands for particular character sets are available. These are a letter preceeded by backslash:

    ```
    let quoteSample = "The five boxing wizards jump quickly.";
    let alphabetRegexV2 = /[\w]/gi; //Letter 'w' is shorthand for alphanumeric characters.
    let result = quoteSample.match(testRegex).length; //Returns 32 (count of all characters that are not a space or period)
    ```

        - Reversible by using capital letter, i.e. using 'W' in the above would make the 'result' variable return 6 (count of spaces and period)

- Remembered how to stipulate that a string must start or end with a particular character using ^ and *. Example:
    ```
    let someRegex = /^[a-z]/ //Ensures string begins with a letter.
    let someOtherRegex = /[0-9]$/ ////Ensures string ends with a number.
    ```

    - Works with shorthand character sets. Example:

    ```
    let someOtherRegex = /\d$/ ////Ensures string ends with a number.
    ```