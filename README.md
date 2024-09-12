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

## JSON PLACEHOLDER
JSONPlaceholder is a free, fake online REST API used for testing and prototyping front-end applications. It provides placeholder data in JSON format, allowing developers to quickly test HTTP requests like GET, POST, PUT, DELETE, etc., without needing to set up a real back-end server.

## Types of Body in Postman

When making `POST`, `PUT`, or `PATCH` requests in Postman, you can send different types of bodies with your requests. Below are the common types of body options available:

## 1. form-data
- Used to send key-value pairs, where values can be text or files.
- Often used when submitting forms (e.g., uploading files).
- Content-Type: `multipart/form-data`.

## 2. x-www-form-urlencoded
- Sends data as key-value pairs but URL-encoded (encoded as a query string).
- Commonly used in `POST` requests for submitting HTML forms.
- Content-Type: `application/x-www-form-urlencoded`.

## 3. raw
- Used to send arbitrary data such as JSON, XML, plain text, etc.
- You can specify the format for raw data (e.g., JSON, XML, HTML, plain text).
- Example content types: `application/json`, `text/xml`.

## 4. binary
- Used to send binary data, such as files (e.g., images, documents).
- You select the file you want to upload.

## 5. GraphQL
- Supports sending GraphQL queries.
- You define the query and variables directly in the request body.

Each body type is suited for different use cases based on the API's requirements.

## How to integrate API'S

In flutter the API's are integraated using the package called HTTP


## Dart API Fetch Example

This repository contains a Dart function to fetch posts from an API using the `http` package. It demonstrates how to make an asynchronous HTTP GET request and convert a URL string into a `Uri` object.

## Function Overview

The function `getPostApi()` sends an HTTP GET request to fetch data from the JSONPlaceholder API. This is an online fake API commonly used for testing and prototyping.

### Function Code:

```dart
import 'package:http/http.dart' as http;
import 'dart:convert';

Future<List<PostsModel>> getPostApi() async {
  final response = await http.get(Uri.parse('https://jsonplaceholder.typicode.com/posts'));
  
  if (response.statusCode == 200) {
    // Parse the JSON response and return the list of PostsModel
    List jsonResponse = jsonDecode(response.body);
    return jsonResponse.map((post) => PostsModel.fromJson(post)).toList();
  } else {
    throw Exception('Failed to load posts');
  }
}
```

### Explanation:

1. **`Future<List<PostsModel>> getPostApi() async {`**  
   - This function returns a `Future` that will eventually hold a list of `PostsModel` objects.
   - The `async` keyword allows for asynchronous operations, enabling the use of `await`.

2. **`final response = await http.get(Uri.parse('https://jsonplaceholder.typicode.com/posts'));`**  
   - This line sends a GET request to the API.  
   - `await` pauses the function until the response is received.
   - `Uri.parse()` converts the string URL into a `Uri` object, which the `http.get()` function requires.

3. **`if (response.statusCode == 200)`**  
   - This checks if the server responded with a status code of 200, meaning the request was successful.

4. **`jsonDecode(response.body)`**  
   - The `jsonDecode()` function is used to convert the JSON response body into a Dart list or map.

5. **`return jsonResponse.map((post) => PostsModel.fromJson(post)).toList();`**  
   - The JSON data is mapped to a list of `PostsModel` objects using the `fromJson` factory method (assumed to be in the `PostsModel` class).

### Required Packages

To run this function, you need to include the `http` package in your `pubspec.yaml` file:

```yaml
dependencies:
  http: ^0.13.3
```

### `Uri.parse()` Explanation:

`Uri.parse()` converts a string URL into a `Uri` object. Dart's HTTP functions (like `http.get()`) require the URL to be a `Uri`, not a plain string.

For example:

```dart
Uri uri = Uri.parse('https://jsonplaceholder.typicode.com/posts');
```

This `Uri` object will be used in HTTP requests like this:

```dart
final response = await http.get(uri);
```

### Model Class Example

Assuming you have a `PostsModel` class to represent the post data:

```dart
class PostsModel {
  final int id;
  final String title;
  final String body;

  PostsModel({required this.id, required this.title, required this.body});

  factory PostsModel.fromJson(Map<String, dynamic> json) {
    return PostsModel(
      id: json['id'],
      title: json['title'],
      body: json['body'],
    );
  }
}
```

### How to Run

1. Add the `http` package to your `pubspec.yaml`.
2. Use `getPostApi()` to fetch posts from the JSONPlaceholder API.
3. Handle the fetched data by converting it into a list of `PostsModel`.

### Sample Response:

The JSONPlaceholder API will return a JSON array of posts. Here's a sample of the response:

```json
[
  {
    "userId": 1,
    "id": 1,
    "title": "Sample Title",
    "body": "Sample Body"
  },
  {
    "userId": 1,
    "id": 2,
    "title": "Another Title",
    "body": "Another Body"
  }
]
```







