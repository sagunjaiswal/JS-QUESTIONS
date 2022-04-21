- Guess the output?
let x = true
setTimeout (()=>{
x= false
})
while (x)
{
console.log(“hello”)
}

O/P : 
Hello ….will go on printing

REASON : 
In this case, the value of x is true in the global scope and as we know that javascript is a single thread language, 
the setTimeout is an asynchronous operation so it will go in the task queue and wait for its chance for execution so 
now we go to “while loop “ the value of x is true so it satisfies the given condition in the while loop now it will 
print continuously “hello” and after 2 seconds the setTimeout is ready for execution but the call stack is not empty, 
it is already running the while loop so setTimeout will not get any chance of execution.

- Guess the ouput?
let x = true
let count =0;
setTimeout(()=>{
x= false;
},2000)
setInterval(()=>{
if(x)
{
console.log(count++)
}
},200)

O/P:

0
1
2
3
4
5
6
7
8
the cursor will be not free on the output screen

REASON :

In this case, the setTimeout and setInterval is an asynchronous operations so first, it calls the setInterval
,setInterval will print the value of count every 200 milliseconds and then after 2-second setTimeout
will invoke and setInterval condition get dissatisfied, it will print up to 8 and execution will continue
