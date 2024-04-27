## 1.Write short notes on below array methods with code examples
## => reverse()
## => sort()
## => fill()
## => filter()
## => some()
## => every()
## => map()
## => forEach()
## => reduce()
## => indexOf()

## Ans: + Reverse() method reverses the order of the element in an array.
```js
let arr=[1,2,3,4,5]
console.log(arr.reverse());

output -[5,4,3,2,1]
```
## + sort() metthod is useed to sort the elemennts of an array.
```js
let arr=[2,3,1,8,6]
console.log(arr.sort());

output-[1,2,3,6,8]
```
##  + fil() method fills spceified elements in an array with a value
```js
let arr=[1,2,3,4,5];
console.log(arr.fill("z",3))

output-[1,2,3,'z','z']
```
## + filter() performs a function on each elements of the array and returns only those elements that passes the test implemented thee function.
```js
let arr=[1,2,3,4,5];
let output=arr.filter((item)=>{
    return item%2==0
})
console.log(output);

output-[2,4]
```
## + some() checks if some of the elements in the array passes the test (atleast one)
```js
let arr=[1,2,3,4,5];
let output=arr.some((item)=>{
    return item%2==0
})
console.log(output);

output- true
```
## + every() tests if all the elements in the array passes the test and returns a boolean value.
```js
let arr=[1,2,3,4,5];
let output=arr.every((item)=>{
    return item%2==0
})
console.log(output);

output- false
```
## + map() creates a new array populate with the function on every elements.
```js
let arr=[1,2,3,4,5];
let output=arr.map((item)=>{
return item*2
})
console.log(output);

output-[2,4,6,8,10]
```
## + foreach() method calls a function for each element in an array 
```js
let arr=[1,2,3,4]
let output=arr.forEach((item)=>{
    console.log(item*3);
})
``` 

## + reduce() Takes in an array ,perform a function  that provide on each element in that array and returns on single value.
```js
let arr=[100,10,3];
let MyFunc=(total,num)=>{
    return total-num
}
let output=arr.reduce(MyFunc)
console.log(output);

output- 87
```
## + indexOf() returns the first index at which a given element can be found in the array. or -1 if it does not present.
```js
let arr=[1,2,3,4]
console.log(arr.indexOf(4));

output- 3
```
## 2.write a function that takes an array of numbers as an argument and returns the sum of its elements.
```js
let arr=[1,2,3,4]
let SumofArray=(total,num)=>{
    return total+num
}
let result=arr.reduce(SumofArray)
console.log(result);

output-10
```

## 3.Create a function that filters strings in an array by their length

## Ans:
```js
let arr=["red","yellow","blue","white"]
let output=arr.filter((item)=>{
    return item.length<5
})
console.log(output);

output-['red','blue']
```

## 4.Create a function that returns a new array containing the square roots of each number in the original array [1,4,9,16,25] (Math.sqrt())

## Ans:
```js
let arr=[4,49,9,64,80]
let  result=arr.map((number)=>{
    return Math.sqrt(number)
})
console.log(result);
```

## 5.Write a function that prints the number 1 to 100. But for multiples of 3, print Fizz instead of the number, and for multiples of 5, print Buzz. For the numbers that are multiples of both 3 and 5, print FizzBuzz(write the code in the browser’s snippet and invoke the function inside the console)

## Ans:
```js
let number=1
let output=[]
let result=()=>{
    while(number<=100){
    if(number%5==0&&number%3==0){
        output.push("FizzBuzz")
    }
    else if(number%5==0){
        output.push("Buzz")
    }
    else if(number%3==0){
        output.push("Fizz")
    }
    else{
        output.push(number)
    }

    number++
}
    console.log(output);
}
result()
```