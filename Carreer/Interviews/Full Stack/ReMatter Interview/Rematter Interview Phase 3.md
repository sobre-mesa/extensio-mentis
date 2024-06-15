- [[CAP Theorem]]
	- Didnt know about it, but answered intuitively, was a correct answer
- [[Race Conditions]] a [[Concurrency]] problem
	- Couldnt answer great, but the idea is avoiding [[Race Conditions]] so you dont have to deal with [[Concurrency]] issues later on
- [[TDD Test Driven Development]]
	- Answered fine
- [[Event Loop]]
	- Answered fine
- A question about the [[Virtual DOM]], but not directly, the question went as followed: 
`Theres a financial app with a bunch of stocks in a table and they all have to update individually, how do I prevent the whole DOM from rendering?`
The answer was meant to make you reproduce the idea of the [[Virtual DOM]], by assigning the dom elements a unique key based on their data, or holding a reference, and then specifically updating the ones referenced in a list of changes. 
- An [[Asynchronous Javascript]] excercise, I will try to remember best I can the problem and solution: , 2 parts

Part 1:
```
let count = 0;

function doSomething(){
	const currentCount = count;
	setTimeOut(() => {
		count = currentCount + 1;
		console.log(count)
	}
	100)
}

for(let i = 0; i < 5; i++){
	doSomething()
}

//What will be printed on the screen?

```

The solution was they would all input 1, because the non async part of the function resolves first 

Part 2:
```
let count = 0;

const sleep = () => setTimeOut(()=>{}, 100)

function doSomething(){
	setTimeOut(() => {
		const currentCount = count;
		console.log(count)
		await sleep(); //rest of funct is asnyc
		count = currentCount + 1;
		console.log(count)
	}
	100)
}

for(let i = 0; i < 5; i++){
	doSomething()
}

//What will be printed on the screen?
```

same result here, but the nuance and what they tried to tests here is that the code will become async after the await call, making count always 0