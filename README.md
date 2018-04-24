# Binary search

Implement a binary search algorithm that takes in two parameters, `list` and `searchValue`, and returns a boolean value indicating whether the input `searchValue` exists in the input `list`. For example:

```js
const nameList = [
    'Aaron',
    'Andy',
    'Batman',
    'Boba',
    'Bonnie',
    'Betsy',
    'Clarence',
    'Daisy',
    'Elektra',
    'Flash'
];

binarySearch(nameList, 'Daisy'); //=> true
binarySearch(nameList, 'Bruce'); //=> false
```

Notice that this function signature is exactly the same as any other __search algorithm__ - it has a target value to search within a list, and if that value is found in that list, it returns either a boolean value indicating its existence, or the found value itself (eg. an object).

Binary search is one of the most commonly used and practical search algorithms out there because of its simplicity and efficiency.

The beauty in binary search is the fact that you've probably used in your life before, but you just may not have noticed it. The classic illustration is searching through a phone book.

### How binary search works

Pretend you have a thick phone book. Each page has several entries of names, followed by the person's phone number next to it on the same line, and all the names are sorted by alphabetical order, so "Aaron" appears before "Andy". How would you go about searching for someone named "Steve"?

Naturally, you'll start by flipping the book to the middle and see what the first alphabet of the first name on the left page is. It turns out that it's a "G". And because you know that "S" happens later in the alphabetical system than "G", what you'll naturally do next is flip to the middle of the right-half of the book, and repeat the same evaluation again until you find a page with names starting with "S". 

That, in essence, is the binary search algorithm. You half a list, discard one half and continue searching through the remaining half, until you arrive (or not) at the value you're searching for. Voila! You found what you wanted without iterating from the first item through to the last in the list - spending much less time for the same result.

Now try and implement this algorithm in code!

__Note__: The only drawback of binary search is that it only works if the array is sorted. Remember to always only feed a sorted array into the algorithm, or else it will very likely return an erroneous result!

## Further - with objects

Create a new `phonebook` array that holds objects instead of strings. Each object should have 3 key-value pairs: `name`, `phone`, and `id`.

Modify your binary search algorithm to search for a given `id` (not `name`) value stored in the object, and return the object itself instead of a boolean value.

For example, `binarySearch(phonebook, 44)` should return `{ name: 'Daisy', phone: 12345678, id: 44 }` (example) instead of `true`. It should still return `false` if no matches were found.

Hint: remember, binary search only works on sorted arrays. In this case, ensure your array is sorted by `id` value before passing it into your algorithm.

You can use the included `phonebook.json` data to save time and focus on writing your algorithm.

### Resources

Mock JSON data generated using https://mockaroo.com/