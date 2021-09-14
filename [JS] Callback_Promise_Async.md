## Callback
------------------
* Callback is a function that can be an argument in another function.
```
function test() {
    console.log("This is callback function.");
}

function main(callback) {
    console.log("This is main function.");
    callback();
}

main(test);
```
## Promise
------------------
* Promise is the solution to resolve callback hell.
* Promise is a returned object to which you attach callback, instead of passing callback into a function.
* We can use `.then()` to chain other callback(promise)
```
const promise = new Promise(resolve, reject) => {
    // call some api to get result

    if (!res) {
        return reject(null)
    }

    resolve(res)
}

promise
    // If the api result is successfully    
    returned.
    .then(data => {console.log(data)})
    // If the api is failed.
    .catch(error => console.log(error))

```
* We can use `Promise.all()` to save time when several promise have the same callback.
```
const promise1
const promise2

Promise.all(promise1, promise2)
    // When promise1 and promise2 are all    
    resolved
    .then()
    // When promise1 or promise2 is rejected
    .catch()
```
## Async / Await
------------------
* When a function is declared with `async` keyword, it means we can use `await` in this function, and it will return a Promise object.
* `await` means we have to stop the async function until some works are done.
* `await` is more readable and maintainable then `.then()`
* Use `await` with `Promise.all()` can send several request at same time to complete asynchony.
```
function test1() {}
function test2() {}

async function main() {
    const res1 = test1()
    const res2 = test2()

    const [data1, data2] = await Promise.all(res1, res2)
    
    return [data1, data2]
}
```