Hey awesome programmer!

You've got much data to manage and of course you use zero-based and non-negative ID's to make each data item unique!

Therefore you need a method, which returns the smallest unused ID for your next new data item...

Note: The given array of used IDs may be unsorted. For test reasons there may be duplicate IDs, but you don't have to find or remove them!

Go on and code some pure awesomeness!


https://www.codewars.com/kata/55eea63119278d571d00006a/train/javascript

**my solution:**

```js 
function nextId(ids){
  ids = ids.sort((a, b) => a - b);
  ids = [...new Set(ids)]
  for (let i = 0; i < ids.length; i++)
    if (ids[i] !== i) {
      return i
    } if (Number(ids.slice(-1)) === ids.length -1) {
      return ids.length
    }
} 

``
