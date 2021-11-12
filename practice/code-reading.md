# Code reading

## Question 1

Take a look at the following code:

```
1    let x = 1;
2    function f1()
3    {
4        let x = 2;
5        console.log(x);
6    }
7    console.log(x);
```

Explain why line 4 and line 6 output different numbers.

ANSWER:
Console.log(x) inside the function will print 2 because value of x = 2 is local to this function.
Console.log(x) outside will print 1 because that's the value of global variable x.
Result : 1

## Question 2

Take a look at the following code:

```
let x = 10

function f1()
{
    console.log(x)
    let y = 20
}

console.log(f1())
console.log(y)
```

What will be the output of this code. Explain your answer in 50 words or less.

ANSWER:
Because X is global variable then we can access to it.
console.log(f1()) will Output: 10
But Y is a local variable inside the function.
console.log(y) will Output: undefined.

Result: 10 , undefined

## Question 3

Take a look at the following code:

```
const x = 9;

function f1(val) {
  val = val + 1;
  return val;
}

f1(x);
console.log(x);

const y = { x: 9 };

function f2(val) {
  val.x = val.x + 1;
  return val;
}

f2(y);
console.log(y);
```

What will be the output of this code. Explain your answer in 50 words or less.

ANSWER:
Object Values are selected by Object manipulation which adds 1 to the value of Y.
So,
Result : 10
