# Build Tree

In JavaScript objects are passed by reference. Given a flat array of objects your task is to build a nested tree from them in O(N) time without using recursion. The root node will have a `parentId` of `null`. There will always be one and only one root node.

**Input:**

The input will be an array of objects where each object will have the keys `id`, `parentId` and `value`.

**Output:**

The output should be a nested object of the tree formed from the list. Each object in the tree should contain the keys `id`, `value` and `children` where `children` is an array.

**Example input:**

```js
[
  { id: 1, parentId: null, value: 5 },
  { id: 2, parentId: 3, value: 2 },
  { id: 3, parentId: 1, value: 8 },
  { id: 4, parentId: 1, value: 13 },
  { id: 5, parentId: 3, value: 10 },
  { id: 6, parentId: 4, value: 200 },
  { id: 7, parentId: 6, value: 51 },
  { id: 8, parentId: 7, value: 12 }
]
```

**Example output:**

```json
{
  "id": 1,
  "value": 5,
  "children": [
    {
      "id": 3,
      "value": 8,
      "children": [
        {
          "id": 2,
          "value": 2,
          "children": []
        },
        {
          "id": 5,
          "value": 10,
          "children": []
        }
      ]
    },
    {
      "id": 4,
      "value": 13,
      "children": [
        {
          "id": 6,
          "value": 200,
          "children": [
            {
              "id": 7,
              "value": 51,
              "children": [
                {
                  "id": 8,
                  "value": 12,
                  "children": []
                }
              ]
            }
          ]
        }
      ]
    }
  ]
}
```
