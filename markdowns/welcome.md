# Call(), Apply() and Bind() Methods in JavaScript.

Working with JavaScript “this” keyword can be tricky. Not knowing the background rules may end up with the famous “it works, but I don’t know why” or worse: “it doesn’t work and I don’t know why”. It’s good to know the theory before putting things into practice. Call(), Apply() and Bind() methods can come in handy when setting the “this” value.

###Basic rules worth remembering:
1.“this” always refers to an object.
2.“this” refers to an object which calls the function it contains.
3.In the global context “this” refers to either window object or is undefined if the ‘strict mode’ is used.
I would like to focus on the first two rules specifically.


