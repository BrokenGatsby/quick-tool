### 假设有一个包含对象的数组，而 我们想按照任意对象属性对数组进行排序

```javascript
function objArrSort (propertyName, type = 'asc') {
	return function (object1, object2) {
		const a = object1[propertyName]
		const b = object2[propertyName]
		if (type === 'asc') {
			return a - b
		} else if (type === 'desc') {
			return b - a
		} else {
			return 0
		}
	}
}

let data = [
	{name: "Zachary", age: 29},
	{name: "Nicholas", age: 28}
]
data.sort(objArrSort('age'))
```
