# Strong tests - recap

[Separation of forming from printing](https://github.com/clean-code-craft-tcq-4/test-failer-in-c-deepasn08/blob/4a093441acf91f1100ba220c57ac93f542ac5bd1/misaligned.c)

[Expression of requirement in failure condition](https://github.com/clean-code-craft-tcq-4/test-failer-in-c-deepasn08/blob/4a093441acf91f1100ba220c57ac93f542ac5bd1/misaligned.c): invalid size would return empty string

Which is right? 
`assert(size(38) == 'S');` or `assert(size(38) == 'M');`

- Reason out. Confirm assumptions with stakeholders
- It doesn't matter... let's do something and wait for someone to shout
- Don't make me think... tell me what to do

[Self-test the test stub](https://github.com/clean-code-craft-tcq-4/test-failer-in-cpp-POOJASHREE-G/blob/572909d3e8ffffbff0ba84d20973ac790bb9b300/alerter.cpp)

[Split a piece of the functionality](https://github.com/clean-code-craft-tcq-4/test-failer-in-c-pprathi/blob/2f8cb5314e3780cfe1127f4fd758ef93b6873e85/misaligned.c) and test piece-by-piece (see `GetPairNumberFromColor`)

## Consider off-the-shelf functionality

When tests are tough to write, see if you can use off-the-shelf functionality.
E.g., why not use comma-separated values? Import it into excel for alignment and printing.
