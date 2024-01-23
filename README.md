This utility is useful to add, retrieve an information in Local Storage, it can merge arrays, delete from array by key etc.

Utility is in the mjs file and can be used with ES6 code. to include the utility to the other file do the following:

    import {LocalStorage} from './Storage.mjs';

**How to retrieve data from the storage:**

    // send this a key - returns JSON
    await LocalStorage.get(key, isRaw, callback)

**How to add new data from the storage:**

    // send this a key and a JSON object
    await LocalStorage.set(key, valueJSON, saveRaw, callback)

**How to add multiple data to the storage:**

    // send this an array of hashes
    await LocalStorage.multiSet(arrayOfArrays, callback)

**How to delete data from the storage:**

    // send this a key to remove the data
    await LocalStorage.delete(key, callback)

**How to add new data to existing array:**

    // send this valueJson to add it to existing array behind the key
    await LocalStorage.addToArray(key, valueJSON, callback)

**How to merge arrays in the Storage:**

    // send this an array to merge it's contents with existing array
    await LocalStorage.mergeArrayToArray(key, inputArray, callback)

**How to remove item from the array:**

    // send this a key and a JSON object with an ID value - removes item at that ID if it's present
    await LocalStorage.removeFromArray(key, removeId, callback)
