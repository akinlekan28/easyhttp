# easyhttp
<strong>A minimal library for making http requests built with vanilla javascript</strong>

<h4>HTTP Methods</h4>
<p>get</p>
<p>post</p>
<p>put</p>
<p>delete</p>

<h4>Usage</h4>
<strong>Include the easyhttp library into your source file before your custom javascript file.</strong>
  <body>
    <h1>EasyHTTP Example</h1>

    <script src="easyhttp.js"></script>
    <script src="app.js"></script>

<h4>Instantiate the library</h4>

<h5>const http = new EasyHTTP;</h5>


<h4>To make get request {api used in this example is Jsonplaceholder, a fake rest api} </h4>

-Basic barebone
http.get('API ENDPOINT'){}

```javascript
//Get posts
  http.get('https://jsonplaceholder.typicode.com/posts')
   .then(data => console.log(data))
   .catch(err => console.log(err));

//Get single post
 http.get('https://jsonplaceholder.typicode.com/posts/1')
   .then(data => console.log(data))
   .catch(err => console.log(err));
```

 <h4>To make a post request</h4>

-Basic barebone
http.post('API ENDPOINT', DATA){}
```javascript
 //Create Data
const data = {
  title: 'Custom Post',
  body: 'This is a custom post'
};

//Create Post
  http.post('https://jsonplaceholder.typicode.com/posts', data)
   .then(data => console.log(data))
   .catch(err => console.log(err));
```

<h4>To make a put request</h4>

-Basic barebone
http.put('API ENDPOINT', DATA, CALLBACK FUNCTION){}

```javascript
//Update post
 http.put('https://jsonplaceholder.typicode.com/posts/5', data)
   .then(data => console.log(data))
   .catch(err => console.log(err));
```


<h4>To make a delete request</h4>

Basic barebone
http.delete('API ENDPOINT'){}

```javascript
//Delete post
http.delete('https://jsonplaceholder.typicode.com/users/2')
  .then(data => console.log(data))
  .catch(err => console.log(err));