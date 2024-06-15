
*Phase 2:*
- Practical Excercise in [[Javascript]]
```
const metals = [
	{ 
	id: 1, 
	name: "Coppper",
	price: 0.42, 
	unit: g
    },
	id: 2, 
	name: "Steel",
	price: 0.35, 
	unit: g
    },
	id: 3, 
	name: "Aluminum",
	price: 0.69, 
	unit: kg
    },
]

const purchases = [
	{
	metalId: 1,
	ammount: 200,
	}, 
	{
	metalId: 1,
	ammount: 33,
	}, 
	{
	metalId: 1,
	ammount: 1,
	}, 
	{
	metalId: 3,
	ammount: 22,
	}, 
	{
	metalId: 1,
	ammount: 333,
	}, 
	{
	metalId: 2,
	ammount: 201,
	}, 
]

function totalBought(){
/// Display total cost, total ammount bought with its unit, and metal name, for each metal
}
```

Was pretty easy, just needed to solve with [[Array.Reduce]] , there was not much complexity or "tricky stuff".  Solved in O(n + n)