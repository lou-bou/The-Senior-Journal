- Triangulation: most conservative/orthodox way
- Obvious implementation: write the code for the obvious implementation of the function to pass the test
- Fake it 'till you make it: just get green at all costs, then improve tests as needed

# Triangulation

You write multiple tests for the same function.
Best to stick to triangulation as a beginner.

# Obvious implementation

If you write a function like `calculateOrderTotal`, you obviously need to implement a function that takes all the orders and sums them up. So you do that and then add more tests as needed.

# Fake it 'till you make it

For `calculateOrderTotal`, if the test checks for a return value of `808`, you just write the implementation code `return 808`, then you add more tests and improve them as needed.
