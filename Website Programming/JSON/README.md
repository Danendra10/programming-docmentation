# JSON

## What is JSON?
1. JSON stands for JavaScript Object Notation
2. JSON is a lightweight data-interchange format
3. JSON is plain text written in JavaScript object notation
4. JSON is used to send data between computers

## JSON Data Types
- a string
```
{"name":"Alex"}
```
- a number
```
{"age":69}
```
- an object
```
{
"student":{"name":"John", "age":30, "city":"New York"}
}
```
- an array
```
{
"students":["Alex", "Dion", "Peter"]
}
```
- a boolean
```
{"sold":true}
```
- null
```
{"middlename":null}
```

## How to write JSON?

You can write json this way
```
{"Name":"Alex"}
```
You can also make an object in JSON, for example
```
{
    "students":[
        {"FirstName":"Jhonny", "LastName":"Deep"},
        {"FirstName":"Jhonny", "LastName":"Neck"},
        {"FirstName":"Jhonny", "LastName":"Kenny"}
    ]
}
```

## Parsing Data JSON
Its common to display or get data from or to web server using JSON, we could use 
```
JSON.parse()
```
for this specific task

For example, we're getting a data from a website
```
'{"name":"Nichole", "age":60, "alive":true}'
```
we can use JS function to convert it to a JS Object

```
const obj = JSON.parse('{"name":"Nichole", "age":60, "alive":true}')
```

How about an array?

For example

```
const text = '["Alex", "Junaedi", "Robert", "Agus"]';
const myArr = JSON.parse(text);
```

How can you display it?

It just a normal array, when you call "myArr[0]" it will simply display "Alex"