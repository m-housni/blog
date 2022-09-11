# Delayed Messages
Implementation of a delayed message with javascript using promise object and async/await function

``` javascript
function sleep(ms) {
  // The Promise object represents the eventual completion (or failure) of an asynchronous operation and its resulting value.
  // In this case setTimeout is an asynchronous aperation
  return new Promise(resolve => setTimeout(resolve, ms));
}

async function delayedMessage() {
  console.log("I am"); // logs "I am" immediately
  await sleep(2000); // wait for 2 secs
  console.log("a delayed"); // log "a delayed"
  await sleep(2000); // wait for 2 more secs 
  console.log("message!"); // then log "message!"
}

delayedMessage(); // execute the function
```
