

### JavaScript:

#### What does it mean by Javascript is single threaded language?

JS is a single threaded which means only one statement is executed at a time. Before we dive into what it means by it runs on single thread.
I would want to first go over the terminology that will help you in understanding.

Synchronous (or sync) execution usually refers to code executing in sequence. In sync programming, the program is executed line by line,
one line at a time. Each time a function is called, the program execution waits until that function returns before continuing to the next
line of code.

const one = () => {
 const two = () => {
    console.log('5');
 }
 two();
}
one();

Javascript is a single threaded language that can be non-blocking. Single threaded means it has only one call stack.
Whatever is on the top of the call stack is run first.

const one = () => {
      console.log("Hello");
}
const two = () => {
    for(i=0; i<= 1000; i++){ }
}
const three = () => {
       console.log("World");
}

one()
two()
three()

what if our second function has to loop through huge numbers. Does this means three() has to wait till two() is executed. Technically, Yes!

#### 
