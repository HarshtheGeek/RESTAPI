# RESTAPI
`This repository will contain the notes of RESTAPI`

# SERVER and CLIENT
A server is a computer or a system that provides resources and data, servies to other computer know as client

`Google`
`Panda`
`Food express`
`Whatsapp`

Are some of the examples


# What is an API?

An **API** (Application Programming Interface) is a set of rules that allows one software application to talk to another. It defines how different systems can request and send information to each other.

It focuses on client server approach.

## Key Points:

- **Interface**: An API acts like a bridge between two systems, making it easier for them to interact.
  
- **Endpoints**: These are specific URLs where requests are made. For example, `https://api.example.com/users` could be an endpoint to get a list of users.
  
- **Requests and Responses**:
  - **GET**: Get (retrieve) data from the API.
  - **POST**: Send (create) data to the API.
  - **PUT**: Update existing data via the API.
  - **DELETE**: Remove data using the API.
  - **Update**: Update the data in the API.
  
- **Data Formats**: APIs commonly exchange data in formats like:
  - **JSON** (JavaScript Object Notation)
  - **XML** (Extensible Markup Language)

- **Authentication**: APIs often need keys or tokens to ensure secure access.
  
## Types of APIs:

1. **REST**: A popular type of API that uses HTTP requests like GET, POST, PUT, and DELETE.
2. **SOAP**: An older protocol that sends data using XML.
3. **GraphQL**: A newer API format that lets you request specific data.

APIs help different apps or services work together. For example, a weather app might use an API to get data from a weather service.

## Technologies used to build API

- NodeJs
- Lavarel

## UNDERSTANDING JSON STRUCTURE

-JSON Stands for JavaScript Object Notation
-It is a lightweight data interchange format
-Its is primirarly used to send data between computers
-It is Language Independent

## JSON STRUCTURE

```
markdown
# JSON Structure and Syntax

**JSON** (JavaScript Object Notation) is a lightweight data format for exchanging information between a server and a web application. It is easy for humans to read and write, and easy for machines to parse and generate.

## Basic JSON Structure
JSON represents data using **objects** and **arrays**.

### 1. Objects
- Defined with curly braces `{}`.
- Contain key-value pairs where the **key** is always a string, and the **value** can be a string, number, boolean, array, or another object.

Example:
```json
{
  "name": "John Doe",
  "age": 30,
  "isStudent": false
}
```

## 2. Arrays
- Defined with square brackets `[]`.
- Contain a list of values, which can be of any data type: strings, numbers, booleans, objects, or arrays.

Example:
```
json
{
  "students": ["John", "Jane", "Jim"],
  "grades": [85, 90, 92]
}
```

## JSON Syntax Rules

## 1. Key-Value Pairs
- Each key-value pair is written as `"key": value`.
- **Keys** must be strings enclosed in double quotes `""`.
- **Values** can be:
  - String: `"John Doe"`
  - Number: `30`
  - Boolean: `true` or `false`
  - Array: `[ ]`
  - Object: `{ }`
  - Null: `null`

## 2. Strings
- Strings must be enclosed in double quotes `""`. Single quotes are **not allowed**.
  
Example:
```
json
"name": "John"
```

## 3. Numbers
- Numbers are written without quotes.
  
Example:
```
json
"age": 25
```

## 4. Booleans
- Booleans are written as `true` or `false` (without quotes).

Example:
```
json
"isStudent": true
```

## 5. Null
- Null values are represented by `null` (without quotes).

Example:
```
json
"middleName": null
```

## 6. Commas
- Key-value pairs inside an object or values inside an array are separated by commas.
- **No trailing commas** after the last item.

Example:
```
json
{
  "name": "John",
  "age": 30
}
```

## Example of a Complex JSON Structure
A JSON structure combining objects and arrays:

```
json
{
  "name": "John Doe",
  "age": 30,
  "isStudent": false,
  "courses": [
    {
      "name": "Math",
      "grade": "A"
    },
    {
      "name": "Science",
      "grade": "B+"
    }
  ],
  "address": {
    "street": "123 Main St",
    "city": "Springfield",
    "zipCode": "12345"
  }
}
```

## Key Points to Remember
- JSON is made up of **key-value pairs**.
- **Objects** `{}` contain key-value pairs.
- **Arrays** `[]` contain lists of values.
- Strings must always be enclosed in double quotes.
- JSON values can be **strings**, **numbers**, **booleans**, **arrays**, **objects**, or **null**.





