# String calculator kata template for node.js
This is a testing template for students who are learning TDD with node.js
## Dependencies:
* node.js

Practicing the String Calculator Kata
1. Run ```npm install```
2. Run ```git checkout -b {name}-attempt-1 master```
3. Run ```npm test```, this should give you the output from fig.1
4.   Write a test first in the .\src\calculator.spec.js file, run ```npm test```, then write the implementation in .\src\calculator.js. Rinse and repeat. (I have included the first test that is failing for demonstration purposes).
5. For ease, you can run ```npm run test -- --watch```. This will rerun the test whenever you save either file.
6. After 15 minutes, run ```git add ./``` then ```git commit -m "Attempt {n}"``` and finally ```git checkout -b {name}-attempt-{n+1} master```
7. Start from step 3

## fig.1
```
    FAIL  src/calulator.spec.js
      string calculator
      ✕ should return 0 if string is empty (13ms)

      ● string calculator › should return 0 if string is empty

    expect(received).toBe(expected) // Object.is equality

    Expected: 0
    Received: undefined

    Difference:

      Comparing two different types of values. Expected number but received undefined.

       6 |         let calculator = new Calculator();
       7 |         let calculatorResult = calculator.add('');
    >  8 |         expect(calculatorResult).toBe(0);
         |                                  ^
       9 |     });
      10 | });

      at Object.toBe (src/calulator.spec.js:8:34)
      ```

## String Calculator Kata from: http://osherove.com/tdd-kata-1/

1. Create a simple String calculator with a method int Add(string numbers)
2. The method can take 0, 1 or 2 numbers, and will return their sum (for an empty string it will return 0) for example “” or “1” or “1,2”
3. Start with the simplest test case of an empty string and move to 1 and two numbers
4. Remember to solve things as simply as possible so that you force yourself to write tests you did not think about
5. Remember to refactor after each passing test
6. Allow the Add method to handle an unknown amount of numbers
7. Allow the Add method to handle new lines between numbers (instead of commas).
8. the following input is ok: “1\n2,3” (will equal 6)
the following input is NOT ok: “1,\n” (not need to prove it - just clarifying)
9. Support different delimiters
to change a delimiter, the beginning of the string will contain a separate line that looks like this: //[delimiter]\n[numbers…] for example “//;\n1;2” should return three where the default delimiter is “;” .
the first line is optional. all existing scenarios should still be supported
10. Calling Add with a negative number will throw an exception “negatives not allowed” - and the negative that was passed.if there are multiple negatives, show all of them in the exception message
###Stop here if you are a beginner. Continue if you can finish the steps so far in less than 30 minutes.

11. Numbers bigger than 1000 should be ignored, so adding 2 + 1001 = 2
12. Delimiters can be of any length with the following format: //[delimiter]\n for example: //[***]\n1***2***3 should return 6
Allow multiple delimiters like this: //[delim1][delim2]\n for example //[*][%]\n1*2%3 should return 6.
make sure you can also handle multiple delimiters with length longer than one char
