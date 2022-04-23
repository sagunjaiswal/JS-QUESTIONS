- Can you write code for this function: sum(a)(b)(c)….( n)(). This should return the sum of all the numbers a+b+c+..+n.;:

SOLUTION :

const sum =(a)=>(b)=>(c)=>(d)=>(e)=>()=>a+b+c+d+e
console.log(sum(1)(2)(3)(4)(5)())


- Explain Closures with snippet?

SOLUTION : 

A closure gives you access to an outer function’s scope from an inner function
function Outer(){
function Inner(){
console.log(“hello”)
}
return Inner;}
var getValue = Outer
getValue()();


- How can you call a function as soon as it defines?


SOLUTION :

(function hello()
{ console.log(“hello”)
})();

An IIFE (Immediately Invoked Function Expression) is a JavaScript function that runs as soon as
it is defined. … It is a design pattern which is also known as a Self-Executing Anonymous Function
and contains two major parts: The first is the anonymous function with lexical scope enclosed within
the Grouping Operator ()
