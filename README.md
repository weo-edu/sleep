# sleep

Sleep is a simple library that emulates the behavior of `sleep(n)` in synchronous languages, using generators or promises.  You can use it on its own with promises, but it's designed to be used with a generator based flow control library such as tj/co.

## Usage

`sleep(n)`:

  * `n` - time to wait, in milliseconds

Returns a promise.

## Example

```javascript
yield request.put('/user/1/follow')
yield sleep(100)
yield request.get('/user/1/followers')
```